# Mini-Projeto 10: Gerenciador de Log de Sistema 📜

---

### 📝 Descrição
Crie uma classe que gerencia mensagens de log e usa construtores e destrutores para garantir a integridade dos dados.

### 🎯 Requisitos
- O construtor deve receber o nome do arquivo de log e abri-lo automaticamente.
- O destrutor deve fechar o arquivo automaticamente.
- Criar um método `registrar(mensagem)` que escreve no arquivo com um prefixo "[LOG]".

### 💡 Dicas
- Use a lista de inicialização do construtor para configurar o arquivo.
- O destrutor garante que o arquivo não fique aberto caso o programa trave ou termine inesperadamente (padrão RAII).

---

### 🚀 Desafio Extra
Use um membro estático (`static int contadorLogs`) para contar quantas mensagens foram registradas em uma única execução do sistema.