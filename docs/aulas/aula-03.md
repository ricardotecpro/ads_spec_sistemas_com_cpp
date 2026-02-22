# Aula 03 - Operadores e Expressões ➕

Nesta aula, exploraremos como manipular dados usando operadores matemáticos, lógicos e relacionais.

---

## 🧮 Operadores Aritméticos

Servem para realizar cálculos matemáticos básicos.

| Operador | Operação | Exemplo (`a=10, b=3`) | Resultado |
| :--- | :--- | :--- | :--- |
| `+` | Adição | `a + b` | `13` |
| `-` | Subtração | `a - b` | `7` |
| `*` | Multiplicação | `a * b` | `30` |
| `/` | Divisão | `a / b` | `3` (inteira) |
| `%` | Módulo (Resto) | `a % b` | `1` |

---

## ⚖️ Operadores Relacionais e Lógicos

Esses operadores sempre retornam um valor booleano (`true` ou `false`).

### Relacionais
- `==` : Igual a
- `!=` : Diferente de
- `>`  : Maior que
- `<`  : Menor que
- `>=` : Maior ou igual
- `<=` : Menor ou igual

### Lógicos
- `&&` : AND (E)
- `||` : OR (OU)
- `!`  : NOT (NÃO)

---

## 🧬 Conversão de Tipos (Casting)

Às vezes precisamos tratar um tipo como se fosse outro.

### Casting Implícito
O compilador faz automaticamente (ex: `int` para `float`).

### Casting Explícito (C++ Style)
```cpp
int a = 10, b = 3;
float resultado = static_cast<float>(a) / b; // Força a divisão decimal
```

---

## 💡 Operador Ternário

Uma forma compacta de fazer um `if-else`.

```cpp
string resultado = (nota >= 6) ? "Aprovado" : "Reprovado";
```

---

## 🧠 Precedência de Operadores

Assim como na matemática, o C++ segue uma ordem:
1. Parênteses `()`
2. Multiplicação, Divisão e Módulo `* / %`
3. Adição e Subtração `+ -`

!!! tip "Use Parênteses"
    Sempre use parênteses para deixar clara a intenção da sua expressão, mesmo que a precedência padrão resolva. Isso melhora muito a legibilidade.

---

## 💻 Exemplo Prático: Média Ponderada

```cpp
#include <iostream>

int main() {
    float n1, n2, media;
    
    std::cout << "Nota 1: ";
    std::cin >> n1;
    std::cout << "Nota 2: ";
    std::cin >> n2;
    
    // Peso 4 para nota 1 e Peso 6 para nota 2
    media = (n1 * 4 + n2 * 6) / 10;
    
    std::cout << "Média Final: " << media << std::endl;
    std::cout << "Status: " << (media >= 6 ? "Aprovado" : "Reprovado") << std::endl;
    
    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Aritmética**: Crie um programa que receba dois números e exiba a soma, diferença, produto e quociente.
2. **Par ou Ímpar**: Use o operador `%` para determinar se um número é par ou ímpar.
3. **Desafio**: Verifique se um ano informado é bissexto (divisível por 4 e não por 100, ou divisível por 400).

---

## 🚀 Mini-Projeto da Aula

**Conversor de Medidas**:
Crie um programa que receba um valor em metros e exiba-o convertido para centímetros, milímetros e quilômetros, utilizando expressões matemáticas e formatação de saída.