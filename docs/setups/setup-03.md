# Setup 03: Web Moderno (JS/TS) 🌐

## 1. Node.js
O motor que roda JavaScript fora do navegador.
1.  Baixe a versão **LTS** em [nodejs.org](https://nodejs.org/).
2.  Instale (Next, Next, Finish).
3.  Teste no terminal: `node -v` e `npm -v`.

## 2. Visual Studio Code
O editor padrão da indústria.
1.  Baixe em [code.visualstudio.com](https://code.visualstudio.com/).
2.  Instale extensões úteis:
    *   **Live Server**: Para rodar HTML localmente.
    *   **Prettier**: Para formatar código.
    *   **ESLint**: Para encontrar erros.

## 3. TypeScript
Após instalar o Node.js, instale o compilador TS globalmente:
```bash
npm install -g typescript
```
Teste com `tsc -v`.

## 4. Solução de Problemas Comuns ⚠️

*   **cmd 'node' não encontrado**: Reinicie seu terminal ou computador após instalar o Node.js.
*   **Erro de Permissão no npm**: Tente executar o terminal como Administrador ou use o `nvm` para gerenciar versões.
*   **Code Runner não funciona**: Verifique se o Node está no PATH. Tente rodar manualmente no terminal: `node arquivo.js`.