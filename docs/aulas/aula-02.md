# Aula 02 - Tipos de Dados e Variáveis 📦

Nesta aula, aprenderemos como o C++ armazena informações na memória e como podemos interagir com o usuário através do console.

---

## 🏗️ Tipos de Dados Primitivos

O C++ é uma linguagem **estaticamente tipada**, o que significa que o tipo de uma variável deve ser declarado e não pode mudar.

| Tipo | Descrição | Exemplo |
| :--- | :--- | :--- |
| `int` | Números inteiros | `10`, `-5` |
| `float` | Números decimais (precisão simples) | `3.14f` |
| `double` | Números decimais (precisão dupla) | `2.71828` |
| `char` | Um único caractere | `'A'` |
| `bool` | Valores lógicos | `true`, `false` |

---

## 🔧 Modificadores de Tipo

Podemos alterar o comportamento e o tamanho dos tipos primitivos usando modificadores:

- **`unsigned`**: Apenas valores positivos (dobra a capacidade positiva).
- **`signed`**: Valores positivos e negativos (padrão).
- **`long`**: Aumenta o tamanho da variável (ex: `long long`).
- **`short`**: Diminui o tamanho da variável.

---

## 📥 Entrada e Saída com std

Diferente do C (`printf`/`scanf`), o C++ usa o conceito de **Streams** (fluxos).

### `std::cout` (Output)
Envia dados para a saída padrão (tela).
```cpp
std::cout << "O valor é: " << variavel << std::endl;
```

### `std::cin` (Input)
Recebe dados da entrada padrão (teclado).
```cpp
int idade;
std::cout << "Digite sua idade: ";
std::cin >> idade;
```

---

## 🧠 Boas Práticas de Declaração

!!! tip "Nomes de Variáveis"
    Use nomes descritivos em **camelCase** (ex: `idadeUsuario`) ou **snake_case** (ex: `idade_usuario`). Evite nomes genéricos como `x` ou `a`.

!!! info "Namespace std"
    Para evitar escrever `std::` o tempo todo, podemos usar `using namespace std;` no início do arquivo, mas isso é considerado uma prática ruim em projetos grandes devido a possíveis conflitos de nomes.

---

## 💻 Exemplo Prático: Calculadora de Área

```cpp
#include <iostream>

int main() {
    float largura, altura, area;

    std::cout << "--- Calculadora de Área ---" << std::endl;
    
    std::cout << "Digite a largura: ";
    std::cin >> largura;
    
    std::cout << "Digite a altura: ";
    std::cin >> altura;
    
    area = largura * altura;
    
    std::cout << "A área total é: " << area << " m2" << std::endl;
    
    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Variáveis**: Crie um programa que declare variáveis de todos os tipos primitivos e as imprima.
2. **Entrada**: Peça ao usuário seu nome (use `std::string`) e idade, e imprima uma mensagem personalizada.
3. **Desafio**: Calcule quantos dias de vida uma pessoa tem aproximadamente com base na idade informada.

---

## 🚀 Mini-Projeto da Aula

**Ficha de Cadastro**:
Desenvolva um programa que solicite: Nome, Idade, Altura, Peso e se é estudante (true/false). Ao final, exiba os dados formatados como uma ficha técnica.