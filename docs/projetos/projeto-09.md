# Mini-Projeto 09: Simulador de Conta Bancária (POO) 🏦

---

### 📝 Descrição
Migre o sistema de struct para uma classe real, aplicando o conceito de encapsulamento.

### 🎯 Requisitos
- Criar a classe `ContaBancaria`.
- Tornar o atributo `saldo` privado.
- Criar métodos públicos: `depositar(valor)`, `sacar(valor)` e `getSaldo()`.
- Impedir saques maiores que o saldo disponível e depósitos negativos.

### 💡 Dicas
- Use métodos *getters* e *setters* para controlar o acesso aos dados sensíveis.
- Lembre-se de validar se o valor do saque é positivo antes de processar.

---

### 🚀 Desafio Extra
Adicione um atributo `titular` e um método `exibirExtrato()` que mostre o nome do dono e o saldo atual formatado.