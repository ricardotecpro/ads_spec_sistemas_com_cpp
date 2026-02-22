# 🚀 Configuração de Deploy - GitHub Pages

Este projeto está configurado com **múltiplas opções** para deploy automático no GitHub Pages. Escolha a que melhor atende suas necessidades:

## ✨ Opção 1: Deploy Padrão (Recomendado)
**Arquivo:** [`pages.yml`](pages.yml)

### Características:
- ✅ **Mais moderno** - Usa GitHub Pages Action oficial  
- ✅ **Mais rápido** - Cache otimizado
- ✅ **Mais seguro** - Usa `id-token: write`
- ✅ **Testes incluídos** - Valida antes do deploy
- ✅ **Deploy automático** - Push na branch `main`

### Quando usar:
- Para a maioria dos casos
- Site estático simples
- Não precisa de versionamento

---

## 📚 Opção 2: Deploy com Versionamento (Mike)
**Arquivo:** [`mike-deploy.yml`](mike-deploy.yml)

### Características:
- ✅ **Versionamento** - Múltiplas versões do site
- ✅ **Histórico** - Acesse versões antigas
- ✅ **Aliases** - `latest`, `estável`, etc.
- ⚡ **Branch `gh-pages`** - Deploy direto na branch

### Quando usar:
- Documentação com versões
- Múltiplos ambientes (dev, staging, prod)  
- Histórico importante

### Comandos Mike (lokalmente):
```bash
# Ver versões disponíveis
poetry run mike list

# Deploy nova versão
poetry run mike deploy v1.2.0 latest

# Definir versão padrão  
poetry run mike set-default v1.2.0

# Servidor local com versões
poetry run mike serve
```

---

## 🔧 Como Ativar

### 1. Habilitar GitHub Pages no Repositório:
1. Vá em **Settings** → **Pages**
2. **Source:** "GitHub Actions" (para `pages.yml`)
   - OU "Deploy from branch" → `gh-pages` (para `mike-deploy.yml`)

### 2. Escolher Workflow:
- **Opção 1:** Manter apenas `pages.yml` ativo
- **Opção 2:** Manter apenas `mike-deploy.yml` ativo
- **Importante:** Não ative ambos simultaneamente!

### 3. Desabilitar Workflows Antigos:
Os arquivos `deploy.yml` e `documentation.yaml` foram marcados como backup e desabilitados.

---

## 📊 Comparação Rápida

| Característica | pages.yml | mike-deploy.yml |
|---|---|---|
| **Velocidade** | ⚡⚡⚡ Muito rápida | ⚡⚡ Rápida |
| **Versionamento** | ❌ Não | ✅ Sim |
| **Segurança** | ⭐⭐⭐ Alta | ⭐⭐ Boa |
| **Facilidade** | ⭐⭐⭐ Simples | ⭐⭐ Moderada |
| **Cache** | ✅ Otimizado | ➖ Básico |

---

## 🛠️ Configuração Local

Para ambas as opções, o desenvolvimento local é o mesmo:

```bash
# Instalar dependências
poetry install

# Servidor local
poetry run task docs
# ou: poetry run mkdocs serve

# Gerar conteúdo
poetry run task slides
poetry run task quizzes  

# Build local
poetry run mkdocs build

# Testes
poetry run task test
```

---

## 🐛 Troubleshooting

### Se o deploy falhar:
1. **Verificar permissões:** Settings → Actions → General → Workflow permissions
2. **Verificar GitHub Pages:** Settings → Pages → Source correta
3. **Logs detalhados:** Actions tab → Click no workflow falhado

### Conflitos de workflow:
- Desabilite um dos workflows se ambos estiverem ativos
- Use apenas `pages.yml` OU `mike-deploy.yml`

### Cache issues:
```bash
# Limpar cache do Poetry
poetry env remove --all
poetry install

# Rebuild completo
poetry run task clean
poetry run task build_all
```

---

## 📝 URLs do Site

Após o deploy bem-sucedido:

- **Site principal:** `https://ricardotecpro.github.io/ads_spec_sistemas_com_cpp/`
- **Com Mike:** Adiciona versionamento em `/latest/`, `/estavel/`, etc.

---

> 💡 **Recomendação:** Comece com `pages.yml` para simplicidade. Migre para `mike-deploy.yml` se precisar de versionamento.