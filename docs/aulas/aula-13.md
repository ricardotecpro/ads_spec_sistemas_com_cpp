# Aula 13 - STL (Standard Template Library) ⚙️

Nesta aula, descobriremos o verdadeiro poder do C++ Moderno: a **STL**. Ela fornece uma coleção de algoritmos e estruturas de dados prontos para uso.

---

## 📦 Containers (Coleções)

Containers são objetos que armazenam outros objetos.

### `std::vector` (Array Dinâmico)
O container mais usado. Expande automaticamente conforme necessário.
```cpp
#include <vector>
std::vector<int> v = {1, 2, 3};
v.push_back(4); // Adiciona ao final
```

### `std::list` (Lista Ligada)
Ideal para inserções e remoções rápidas em qualquer posição.

### `std::map` (Dicionário/Chave-Valor)
Armazena pares ordenados.
```cpp
#include <map>
std::map<std::string, int> idades;
idades["Ricardo"] = 30;
```

---

## ↖️ Iteradores

Iteradores funcionam como "ponteiros inteligentes" para navegar pelos elementos de um container de forma padronizada.

```cpp
std::vector<int> numeros = {10, 20, 30};
for (auto it = numeros.begin(); it != numeros.end(); ++it) {
    std::cout << *it << " ";
}
```

---

## 🧮 Algoritmos (`<algorithm>`)

A STL oferece centenas de algoritmos otimizados que funcionam com qualquer container.

| Algoritmo | Função |
| :--- | :--- |
| `std::sort()` | Ordena os elementos |
| `std::find()` | Busca um elemento |
| `std::reverse()` | Inverte a ordem |
| `std::count()` | Conta ocorrências |

```cpp
std::sort(v.begin(), v.end());
```

---

## 🧬 Introdução a Templates

Templates permitem escrever código que funciona com **qualquer tipo de dado**, sem repetição.

```cpp
template <typename T>
T maior(T a, T b) {
    return (a > b) ? a : b;
}
```

---

## 🧠 Dica de Performance

!!! tip "Use `emplace_back`"
    Em vez de `push_back`, use `emplace_back` ao inserir objetos complexos em um vetor. Isso constrói o objeto diretamente dentro do vetor, evitando cópias desnecessárias.

!!! warning "Invalidate Iterators"
    Cuidado ao remover elementos de um vetor enquanto o percorre com um iterador. Isso pode "invalidar" o iterador e causar erros. Use o retorno de `erase()` para atualizar o iterador.

---

## 💻 Exemplo Prático: Gerenciador de Notas com Vector

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<float> notas;
    float n;

    while (true) {
        std::cout << "Digite a nota (ou -1 para sair): ";
        std::cin >> n;
        if (n == -1) break;
        notas.push_back(n);
    }

    if (!notas.empty()) {
        std::sort(notas.begin(), notas.end());
        std::cout << "Notas ordenadas: ";
        for (float nota : notas) std::cout << nota << " ";
        std::cout << std::endl;
    }

    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Vector**: Crie um programa que receba nomes de alunos e os armazene em um `std::vector`, exibindo-os em ordem alfabética.
2. **Map**: Crie um dicionário de tradução simples (Português -> Inglês) usando `std::map`.
3. **Desafio**: Use `std::count` para contar quantas vezes um número específico aparece em uma lista aleatória.

---

## 🚀 Mini-Projeto da Aula

**Sistema de Estoque Simples**:
Use um `std::map<std::string, int>` para representar um estoque (Nome do Produto -> Quantidade). O sistema deve permitir: Adicionar produtos, vender (reduzir quantidade) e exibir o relatório completo de itens em falta.