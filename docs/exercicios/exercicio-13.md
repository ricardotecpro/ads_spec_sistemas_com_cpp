# Exercícios - Aula 13: STL (Standard Template Library)

Praticando o uso de containers e algoritmos modernos.

### 🟢 Básicos
1. **Vector de Strings**: Peça 5 nomes ao usuário, guarde-os em um `std::vector` e depois os imprima usando um *range-based for*.
2. **Algoritmo de Ordenação**: Use `std::sort()` para ordenar uma lista de 10 números inteiros aleatórios.

### 🟡 Intermediários
3. **Busca em Map**: Crie um `std::map<int, string>` que represente um cadastro de IDs e nomes. Peça um ID ao usuário e informe se ele existe no mapa.
4. **Listas**: Crie uma `std::list` e adicione elementos no início e no fim. Remova o segundo elemento.

### 🔴 Desafio
5. **Template Genérico**: Escreva um template de função `trocar<T>(T &a, T &b)` que funcione para qualquer tipo de dado (int, float, string). Teste a função no `main`.