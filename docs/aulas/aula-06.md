# Aula 06 - Arrays e Strings 🧵

Nesta aula, aprenderemos a trabalhar com coleções de dados do mesmo tipo e mergulharemos no mundo das Strings.

---

## 📊 Arrays (Vetores e Matrizes)

Arrays permitem armazenar múltiplos valores sob um único nome, acessados por um índice (começando em **0**).

### Unidimensionais (Vetores)
```cpp
int notas[5] = {10, 8, 9, 7, 6};
std::cout << notas[0]; // Imprime 10
```

### Multidimensionais (Matrizes)
```cpp
int grade[2][3] = { {1, 2, 3}, {4, 5, 6} };
std::cout << grade[1][0]; // Imprime 4
```

---

## 🔡 Manipulação de Texto

C++ oferece duas formas de trabalhar com texto:

### 1. C-Style Strings
Arrays de caracteres terminados em `\0`.
```cpp
char nome[] = "C++";
```

### 2. Classe `std::string` (Recomendado)
Muito mais poderosa e segura que a forma antiga.
```cpp
#include <string>
std::string frase = "Olá, C++ Moderno!";
std::cout << frase.length(); // Retorna o tamanho
```

---

## 🛠️ Operações Comuns com Strings

| Operação | Exemplo |
| :--- | :--- |
| Concatenação | `s1 + s2` |
| Comparação | `s1 == s2` |
| Substring | `s.substr(0, 5)` |
| Busca | `s.find("C++")` |
| Limpeza | `s.clear()` |

---

## 🧠 Percorrendo Coleções

!!! info "Range-based for (C++11)"
    Uma forma moderna e elegante de percorrer arrays:
    ```cpp
    int numeros[] = {1, 2, 3, 4, 5};
    for(int n : numeros) {
        std::cout << n << " ";
    }
    ```

!!! warning "Cuidado com os Limites"
    O C++ **não verifica** se você está tentando acessar um índice fora do array (ex: `notas[10]` num array de 5). Isso pode causar travamentos ou comportamentos imprevisíveis.

---

## 💻 Exemplo Prático: Média de Notas com Vetor

```cpp
#include <iostream>
#include <string>

int main() {
    std::string nome;
    float notas[3];
    float soma = 0;

    std::cout << "Nome do aluno: ";
    std::getline(std::cin, nome); // getline lê a linha toda (incluindo espaços)

    for (int i = 0; i < 3; i++) {
        std::cout << "Digite a nota " << i+1 << ": ";
        std::cin >> notas[i];
        soma += notas[i];
    }

    std::cout << "\nAluno: " << nome << std::endl;
    std::cout << "Média: " << soma / 3 << std::endl;

    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Vetor**: Crie um programa que leia 10 números e mostre qual é o maior deles.
2. **String**: Receba uma frase do usuário e conte quantas vogais ela possui.
3. **Desafio**: Implemente uma matriz 3x3 que represente um tabuleiro de Jogo da Velha simples.

---

## 🚀 Mini-Projeto da Aula

**Analisador de Texto**:
Desenvolva um programa que peça um parágrafo ao usuário e exiba: Total de caracteres, total de palavras (baseado nos espaços) e a versão do texto em caixa alta (uppercase).