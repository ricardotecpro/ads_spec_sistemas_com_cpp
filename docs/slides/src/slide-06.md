# Aula 06 - Arrays e Strings 🧵

---

## O que é um Array (Vetor)?
- Uma coleção de elementos do mesmo tipo. { .fragment }
- Armazenados de forma contígua (vizinhos) na memória. { .fragment }

---

## Declaração e Acesso
```cpp
int notas[5]; // Array de 5 inteiros
notas[0] = 10; // Primeiro elemento
```
- **Lembre-se**: C++ começa a contar no **zero**. { .fragment }

---

## Inicialização
```cpp
int lista[] = {10, 20, 30}; // Tamanho automático
int zeros[10] = {0};        // Tudo zerado
```

---

## Perigos do Array Nativo
- C++ não verifica se você saiu do limite (Out of bounds). { .fragment }
- `arr[10]` em um array de 5 pode causar travamentos! { .fragment }

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
- Forma moderna e segura: { .fragment }
```cpp
for (int x : notas) {
    cout << x << endl;
}
```

---

## Arrays de Caracteres (C-Style Strings)
- `char nome[10] = "Aula";` { .fragment }
- Terminadas pelo caractere nulo `\0`. { .fragment }

---

## A Classe std::string (C++ Standard)
- Muito mais poderosa e segura que o array de char. { .fragment }
- `#include <string>` { .fragment }

---

## Operações com Strings
- **Concatenação**: `s1 + s2` { .fragment }
- **Tamanho**: `s.size()` ou `s.length()` { .fragment }
- **Acesso**: `s[0]` { .fragment }

---

## Métodos Úteis
- `s.empty()`: Verifica se está vazia. { .fragment }
- `s.clear()`: Apaga tudo. { .fragment }
- `s.substr()`: Extrai parte do texto. { .fragment }
- `s.find()`: Procura texto. { .fragment }

---

## Entrada de Strings (cin vs getline)
- `cin >> nome;` (Para no espaço). { .fragment }
- `getline(cin, nome);` (Lê a linha inteira). { .fragment }

---

## Comparação de Strings
- Use `==`, `!=`, `<`, `>`. { .fragment }
- A comparação é feita por ordem alfabética (lexicográfica). { .fragment }

---

## Conversão (String para Número)
- `stoi(s)`: String para Int. { .fragment }
- `stod(s)`: String para Double. { .fragment }
- `to_string(num)`: Número para String. { .fragment }

---

## std::vector (O Array Dinâmico)
- Array que cresce sozinho! { .fragment }
- `#include <vector>` { .fragment }

---

## Uso de vector
```cpp
vector<int> v;
v.push_back(10); // Adiciona ao fim
v.pop_back();    // Remove do fim
```

---

## Performance: Reservando Memória
- `v.reserve(100)` { .fragment }
- Evita múltiplas realocações lentas. { .fragment }

---

## Arrays como Argumentos
- Arrays são passados "como ponteiros" por padrão. { .fragment }
- Alterar o array dentro da função altera o original! { .fragment }

---

## Algoritmos da STL (std::sort)
- `#include <algorithm>` { .fragment }
- `sort(v.begin(), v.end());` { .fragment }

---

## Resumo da Aula
- Use `std::string` em vez de `char[]`. { .fragment }
- Use `std::vector` em vez de `array[]` (sempre que possível). { .fragment }
- Cuidado com os índices! { .fragment }

---

## Desafio: Palíndromo
- Como você verificaria se uma palavra lida é igual de trás para frente? { .fragment }

---

## Fim da Aula 06
- Próxima aula: Ponteiros e Referências!