# Mini-Projeto 04: Jogo de Adivinhação 🎲

---

### 📝 Descrição
Desenvolva um jogo onde o computador escolhe um número secreto e o jogador deve tentar adivinhar qual é.

### 🎯 Requisitos
- O número secreto deve estar entre 1 e 100.
- O programa deve dar dicas: "Muito alto" ou "Muito baixo".
- O loop deve continuar até o jogador acertar.
- Ao final, mostre quantas tentativas foram necessárias.

### 💡 Dicas
- Use o cabeçalho `<cstdlib>` e `<ctime>` para gerar números aleatórios.
- Use um loop `do-while` para garantir que o jogo rode pelo menos uma vez.

```cpp
srand(time(NULL)); // Inicializa a semente aleatória
int secreto = rand() % 100 + 1; // Número entre 1 e 100
```

---

### 🚀 Desafio Extra
Limite o número de tentativas para 7. Se o jogador não acertar, ele perde o jogo!