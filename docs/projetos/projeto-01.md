# Mini-Projeto 01: Meu Primeiro Sistema C++ 🛠️

---

### 📝 Descrição
Neste primeiro contato prático, você deve criar um programa que simula a tela de inicialização de um sistema operacional antigo (CLI).

### 🎯 Requisitos
- Exibir um cabeçalho estilizado usando caracteres ASCII.
- Informar a versão do sistema (v1.0.0).
- Simular o carregamento de módulos (apenas texto).
- Solicitar que o usuário pressione uma tecla para continuar.

### 💡 Dicas
- Use `std::cout` com `\n` e `\t` para organizar o texto.
- Use `std::cin.get()` para pausar o programa até o usuário apertar Enter.

```cpp
// Exemplo de cabeçalho
cout << "############################" << endl;
cout << "#      OPERA-CPP v1.0      #" << endl;
cout << "############################" << endl;
```

---

### 🚀 Desafio Extra
Tente alinhar o texto perfeitamente no centro de uma caixa de 30 caracteres.