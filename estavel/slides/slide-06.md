# Aula 06 - Arrays e Strings 🧵

---

## O que é um Array (Vetor)?
- Uma coleção de elementos do mesmo tipo. <!-- .element: class="fragment" -->
- Armazenados de forma contígua (vizinhos) na memória. <!-- .element: class="fragment" -->

---

## Declaração e Acesso
```cpp
int notas[5]; // Array de 5 inteiros
notas[0] = 10; // Primeiro elemento
```
- **Lembre-se**: C++ começa a contar no **zero**. <!-- .element: class="fragment" -->

---

## Inicialização
```cpp
int lista[] = {10, 20, 30}; // Tamanho automático
int zeros[10] = {0};        // Tudo zerado
```

---

## Perigos do Array Nativo
- C++ não verifica se você saiu do limite (Out of bounds). <!-- .element: class="fragment" -->
- `arr[10]` em um array de 5 pode causar travamentos! <!-- .element: class="fragment" -->

---

## Matrizes (Arrays Multidimensionais)
```cpp
int matriz[3][3]; // 3 linhas e 3 colunas
matriz[0][0] = 1;
```

---

## Percorrendo Arrays (Loop for)
```cpp
for (int i = 0; i < 5; i++) {
    cout << notas[i] << endl;
}
```

---

## Range-based for (C++11)
- Forma moderna e segura: <!-- .element: class="fragment" -->
```cpp
for (int x : notas) {
    cout << x << endl;
}
```

---

## Arrays de Caracteres (C-Style Strings)
- `char nome[10] = "Aula";` <!-- .element: class="fragment" -->
- Terminadas pelo caractere nulo `\0`. <!-- .element: class="fragment" -->

---

## A Classe std::string (C++ Standard)
- Muito mais poderosa e segura que o array de char. <!-- .element: class="fragment" -->
- `#include <string>` <!-- .element: class="fragment" -->

---

## Operações com Strings
- **Concatenação**: `s1 + s2` <!-- .element: class="fragment" -->
- **Tamanho**: `s.size()` ou `s.length()` <!-- .element: class="fragment" -->
- **Acesso**: `s[0]` <!-- .element: class="fragment" -->

---

## Métodos Úteis
- `s.empty()`: Verifica se está vazia. <!-- .element: class="fragment" -->
- `s.clear()`: Apaga tudo. <!-- .element: class="fragment" -->
- `s.substr()`: Extrai parte do texto. <!-- .element: class="fragment" -->
- `s.find()`: Procura texto. <!-- .element: class="fragment" -->

---

## Entrada de Strings (cin vs getline)
- `cin >> nome;` (Para no espaço). <!-- .element: class="fragment" -->
- `getline(cin, nome);` (Lê a linha inteira). <!-- .element: class="fragment" -->

---

## Comparação de Strings
- Use `==`, `!=`, `<`, `>`. <!-- .element: class="fragment" -->
- A comparação é feita por ordem alfabética (lexicográfica). <!-- .element: class="fragment" -->

---

## Conversão (String para Número)
- `stoi(s)`: String para Int. <!-- .element: class="fragment" -->
- `stod(s)`: String para Double. <!-- .element: class="fragment" -->
- `to_string(num)`: Número para String. <!-- .element: class="fragment" -->

---

## std::vector (O Array Dinâmico)
- Array que cresce sozinho! <!-- .element: class="fragment" -->
- `#include <vector>` <!-- .element: class="fragment" -->

---

## Uso de vector
```cpp
vector<int> v;
v.push_back(10); // Adiciona ao fim
v.pop_back();    // Remove do fim
```

---

## Performance: Reservando Memória
- `v.reserve(100)` <!-- .element: class="fragment" -->
- Evita múltiplas realocações lentas. <!-- .element: class="fragment" -->

---

## Arrays como Argumentos
- Arrays são passados "como ponteiros" por padrão. <!-- .element: class="fragment" -->
- Alterar o array dentro da função altera o original! <!-- .element: class="fragment" -->

---

## Algoritmos da STL (std::sort)
- `#include <algorithm>` <!-- .element: class="fragment" -->
- `sort(v.begin(), v.end());` <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Use `std::string` em vez de `char[]`. <!-- .element: class="fragment" -->
- Use `std::vector` em vez de `array[]` (sempre que possível). <!-- .element: class="fragment" -->
- Cuidado com os índices! <!-- .element: class="fragment" -->

---

## Desafio: Palíndromo
- Como você verificaria se uma palavra lida é igual de trás para frente? <!-- .element: class="fragment" -->

---

## Fim da Aula 06
- Próxima aula: Ponteiros e Referências!