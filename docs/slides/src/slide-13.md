# Aula 13 - STL ⚙️

---

## O que é a STL?
- **Standard Template Library**. { .fragment }
- Conjunto de ferramentas prontas e altamente otimizadas. { .fragment }

---

## Os 3 Pilares da STL
1. **Containers**: Guardam os dados (vector, map, list). { .fragment }
2. **Algoritmos**: Processam os dados (sort, find, count). { .fragment }
3. **Iteradores**: Fazem a ponte entre ambos. { .fragment }

---

## Containers Sequenciais
- `std::vector`: Array dinâmico (O mais comum). { .fragment }
- `std::list`: Lista duplamente ligada. { .fragment }
- `std::deque`: Fila de duas extremidades. { .fragment }

---

## Containers Associativos
- `std::map`: Chave-Valor ordenado. { .fragment }
- `std::set`: Conjunto de valores únicos e ordenados. { .fragment }
- `std::unordered_map`: Tabela Hash (Muito rápido). { .fragment }

---

## Por que usar std::vector?
- Acesso rápido (O(1)). { .fragment }
- Cache-friendly (dados contíguos). { .fragment }
- Gerencia a memória sozinho. { .fragment }

---

## Métodos Essenciais do Vector
- `push_back()` / `emplace_back()` { .fragment }
- `size()` / `capacity()` { .fragment }
- `at()` (acesso com checagem de erro) { .fragment }

---

## O container std::map
```cpp
map<int, string> usuarios;
usuarios[1] = "Ricardo";
```
- Busca por chave em O(log n). { .fragment }

---

## Iteradores: Aponte para o Sucesso
- Agem como ponteiros genéricos. { .fragment }
- `v.begin()`: Primeiro elemento. { .fragment }
- `v.end()`: **Depois** do último elemento. { .fragment }

---

## Percorrendo com Iteradores
```cpp
for (auto it = v.begin(); it != v.end(); ++it) {
    cout << *it;
}
```

---

## Algoritmos Genéricos (#include <algorithm>)
- Funcionam com qualquer container da STL. { .fragment }
- `std::sort()` { .fragment }
- `std::find()` { .fragment }
- `std::count()` { .fragment }

---

## Lambda Functions e Algoritmos
- Personalize buscas e ordenações na hora! { .fragment }
```cpp
sort(v.begin(), v.end(), [](int a, int b) {
    return a > b; // Ordem decrescente
});
```

---

## Templates: A Mágica por trás
- Permitem escrever código que funciona com qualquer tipo. { .fragment }
```cpp
template <typename T>
T maior(T a, T b) { return (a > b) ? a : b; }
```

---

## Template de Classe
```cpp
template <class T>
class Caixa { T item; };
```

---

## Complexidade Algorítmica (Notação Big-O)
- STL é desenhada para garantir limites de performance. { .fragment }

---

## Stack (Pilha) e Queue (Fila)
- Adaptadores de containers que restringem o acesso (LIFO / FIFO). { .fragment }

---

## Performance: Reservando Memória
- Reallocations são custosas. Use `reserve()` em vectors se souber o tamanho. { .fragment }

---

## Modern C++: as funções std::all_of, std::any_of
- Verificam condições em coleções inteiras em uma linha. { .fragment }

---

## Namespaces
- Quase tudo na STL está dentro do `std::`. { .fragment }
- Evite `using namespace std;` em projetos grandes e headers. { .fragment }

---

## STL vs Performance Crítica
- Em 99% dos casos, a STL é mais rápida que sua própria implementação. { .fragment }

---

## Benefícios da STL
- Segurança. { .fragment }
- Padronização (qualquer programador C++ entende). { .fragment }
- Portabilidade. { .fragment }

---

## Resumo da Aula
- Comece sempre pelo `std::vector`. { .fragment }
- Use `std::map` para cadastros. { .fragment }
- Explore a bibioteca `algorithm`. { .fragment }

---

## Fim da Aula 13
- Próxima aula: Gerenciamento de Memória (Smart Pointers)!