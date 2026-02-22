# Aula 05 - Funções 🧩

Nesta aula, aprenderemos como organizar e reutilizar nosso código criando blocos funcionais chamados de **Funções**.

---

## 🏗️ Anatomia de uma Função

Uma função no C++ precisa de um tipo de retorno, um nome e, opcionalmente, parâmetros.

```cpp
// Declaração (Protótipo)
int somar(int a, int b);

// Definição
int somar(int a, int b) {
    return a + b;
}
```

### 🔁 Tipos de Retorno
- `int`, `float`, `string`, etc. (Retornam um valor)
- `void` (Não retorna nada)

---

## 🔗 Passagem de Parâmetros

No C++, existem duas formas principais de enviar dados para uma função:

### Passagem por Valor
Cria uma **cópia** da variável. Alterações dentro da função não afetam a original.
```cpp
void dobrar(int x) { x = x * 2; }
```

### Passagem por Referência
Usa o endereço da variável original através do operador `&`. Alterações **afetam** a variável original.
```cpp
void dobrar(int &x) { x = x * 2; }
```

---

## 🧬 Sobrecarga de Funções (Overloading)

C++ permite criar várias funções com o **mesmo nome**, desde que seus parâmetros sejam diferentes (em tipo ou quantidade).

```cpp
void imprimir(int n) { std::cout << "Inteiro: " << n << std::endl; }
void imprimir(std::string s) { std::cout << "Texto: " << s << std::endl; }
```

---

## 💡 Funções Inline

Funções pequenas podem ser marcadas como `inline`. Isso sugere ao compilador substituir a chamada da função pelo código dela, economizando tempo de processamento.

```cpp
inline int quadrado(int x) { return x * x; }
```

---

## 🧠 Hierarquia de Escopo

!!! info "Variáveis Locais vs Globais"
    Variáveis declaradas dentro de uma função são **locais** e só existem ali. Variáveis declaradas fora de todas as funções são **globais**, mas devem ser evitadas para manter a organização.

!!! tip "Protótipos"
    É uma boa prática declarar as funções no topo do arquivo (ou em um header `.h`) e definí-las após a função `main`.

---

## 💻 Exemplo Prático: Calculadora Modular

```cpp
#include <iostream>

// Protótipos
void exibirMenu();
float calcular(float a, float b, char op);

int main() {
    float x, y;
    char o;

    exibirMenu();
    std::cout << "Número 1: "; std::cin >> x;
    std::cout << "Operação (+, -, *, /): "; std::cin >> o;
    std::cout << "Número 2: "; std::cin >> y;

    std::cout << "Resultado: " << calcular(x, y, o) << std::endl;

    return 0;
}

void exibirMenu() {
    std::cout << "--- Calculadora Modular ---" << std::endl;
}

float calcular(float a, float b, char op) {
    switch (op) {
        case '+': return a + b;
        case '-': return a - b;
        case '*': return a * b;
        case '/': return b != 0 ? a / b : 0;
        default: return 0;
    }
}
```

---

## 📝 Exercício de Fixação

1. **Básico**: Crie uma função que receba um número e retorne `true` se ele for par.
2. **Referência**: Crie uma função `trocar(int &a, int &b)` que inverta o valor de duas variáveis.
3. **Desafio**: Implemente uma função recursiva para calcular o fatorial de um número.

---

## 🚀 Mini-Projeto da Aula

**Sistema de Conversão de Temperatura**:
Crie um programa com funções separadas para converter: Celsius para Fahrenheit, Fahrenheit para Celsius e Celsius para Kelvin. Use um menu para o usuário escolher a conversão desejada.