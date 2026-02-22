# Aula 04 - Estruturas de Controle 🚦

Nesta aula, aprenderemos como controlar o fluxo de execução do nosso programa usando tomadas de decisão e laços de repetição.

---

## 🛣️ Estruturas Condicionais

As condicionais permitem que o programa execute diferentes blocos de código com base em condições lógicas.

### `if / else if / else`
```cpp
if (idade >= 18) {
    std::cout << "Maior de idade" << std::endl;
} else if (idade >= 16) {
    std::cout << "Pode votar, mas não dirigir" << std::endl;
} else {
    std::cout << "Menor de idade" << std::endl;
}
```

### `switch`
Ideal para testar uma única variável contra múltiplos valores constantes.
```cpp
switch (opcao) {
    case 1:
        std::cout << "Opção 1 selecionada";
        break;
    case 2:
        std::cout << "Opção 2 selecionada";
        break;
    default:
        std::cout << "Opção inválida";
}
```

---

## 🔄 Estruturas de Repetição (Loops)

Loops são usados para repetir um bloco de código várias vezes.

### `while`
Repete enquanto a condição for verdadeira.
```cpp
int i = 0;
while (i < 5) {
    std::cout << i << " ";
    i++;
}
```

### `do-while`
Garante que o código seja executado **pelo menos uma vez**.
```cpp
char resposta;
do {
    std::cout << "Deseja continuar? (s/n): ";
    std::cin >> resposta;
} while (resposta == 's');
```

### `for`
Ideal quando sabemos o número de repetições.
```cpp
for (int i = 0; i < 10; i++) {
    std::cout << "Contagem: " << i << std::endl;
}
```

---

## 🧠 Boas Práticas e Legibilidade

!!! info "Indentação"
    Manter o código bem indentado é crucial para entender a hierarquia das estruturas de controle. Use sempre 4 espaços ou 1 tab.

!!! warning "Cuidado com Loops Infinitos"
    Certifique-se sempre de que a condição de parada do seu loop será atingida em algum momento, caso contrário seu programa ficará travado.

---

## 💻 Exemplo Prático: Jogo de Adivinhação

```cpp
#include <iostream>

int main() {
    int numeroSecreto = 42;
    int palpite;
    int tentativas = 0;

    std::cout << "--- Adivinhe o Número ---" << std::endl;

    do {
        std::cout << "Digite seu palpite: ";
        std::cin >> palpite;
        tentativas++;

        if (palpite < numeroSecreto) {
            std::cout << "Muito baixo!" << std::endl;
        } else if (palpite > numeroSecreto) {
            std::cout << "Muito alto!" << std::endl;
        }

    } while (palpite != numeroSecreto);

    std::cout << "Parabéns! Você acertou em " << tentativas << " tentativas." << std::endl;

    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Condicional**: Crie um programa que receba a nota de um aluno e diga se ele foi aprovado (>=7), em recuperação (>=5 e <7) ou reprovado (<5).
2. **Loop For**: Imprima a tabuada de um número fornecido pelo usuário.
3. **Desafio**: Crie um programa que exiba todos os números primos entre 1 e 100.

---

## 🚀 Mini-Projeto da Aula

**Simulador de Caixa Eletrônico**:
Desenvolva um menu (usando `switch` dentro de um `do-while`) que permita: 1-Ver Saldo, 2-Depositar, 3-Sacar e 0-Sair. Use condicionais para garantir que o usuário não saque mais do que possui em conta.