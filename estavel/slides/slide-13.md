# Aula 13 - STL ⚙️

---

## O que é a STL?
- **Standard Template Library**. <!-- .element: class="fragment" -->
- Conjunto de ferramentas prontas e altamente otimizadas. <!-- .element: class="fragment" -->

---

## Os 3 Pilares da STL
1. **Containers**: Guardam os dados (vector, map, list). <!-- .element: class="fragment" -->
2. **Algoritmos**: Processam os dados (sort, find, count). <!-- .element: class="fragment" -->
3. **Iteradores**: Fazem a ponte entre ambos. <!-- .element: class="fragment" -->

---

## Containers Sequenciais
- `std::vector`: Array dinâmico (O mais comum). <!-- .element: class="fragment" -->
- `std::list`: Lista duplamente ligada. <!-- .element: class="fragment" -->
- `std::deque`: Fila de duas extremidades. <!-- .element: class="fragment" -->

---

## Containers Associativos
- `std::map`: Chave-Valor ordenado. <!-- .element: class="fragment" -->
- `std::set`: Conjunto de valores únicos e ordenados. <!-- .element: class="fragment" -->
- `std::unordered_map`: Tabela Hash (Muito rápido). <!-- .element: class="fragment" -->

---

## Por que usar std::vector?
- Acesso rápido (O(1)). <!-- .element: class="fragment" -->
- Cache-friendly (dados contíguos). <!-- .element: class="fragment" -->
- Gerencia a memória sozinho. <!-- .element: class="fragment" -->

---

## Métodos Essenciais do Vector
- `push_back()` / `emplace_back()` <!-- .element: class="fragment" -->
- `size()` / `capacity()` <!-- .element: class="fragment" -->
- `at()` (acesso com checagem de erro) <!-- .element: class="fragment" -->

---

## O container std::map
```cpp
map<int, string> usuarios;
usuarios[1] = "Ricardo";
```
- Busca por chave em O(log n). <!-- .element: class="fragment" -->

---

## Iteradores: Aponte para o Sucesso
- Agem como ponteiros genéricos. <!-- .element: class="fragment" -->
- `v.begin()`: Primeiro elemento. <!-- .element: class="fragment" -->
- `v.end()`: **Depois** do último elemento. <!-- .element: class="fragment" -->

---

## Percorrendo com Iteradores
```cpp
for (auto it = v.begin(); it != v.end(); ++it) {
    cout << *it;
}
```

---

## Algoritmos Genéricos (#include <algorithm>)
- Funcionam com qualquer container da STL. <!-- .element: class="fragment" -->
- `std::sort()` <!-- .element: class="fragment" -->
- `std::find()` <!-- .element: class="fragment" -->
- `std::count()` <!-- .element: class="fragment" -->

---

## Lambda Functions e Algoritmos
- Personalize buscas e ordenações na hora! <!-- .element: class="fragment" -->
```cpp
sort(v.begin(), v.end(), [](int a, int b) {
    return a > b; // Ordem decrescente
});
```

---

## Templates: A Mágica por trás
- Permitem escrever código que funciona com qualquer tipo. <!-- .element: class="fragment" -->
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
- STL é desenhada para garantir limites de performance. <!-- .element: class="fragment" -->

---

## Stack (Pilha) e Queue (Fila)
- Adaptadores de containers que restringem o acesso (LIFO / FIFO). <!-- .element: class="fragment" -->

---

## Performance: Reservando Memória
- Reallocations são custosas. Use `reserve()` em vectors se souber o tamanho. <!-- .element: class="fragment" -->

---

## Modern C++: as funções std::all_of, std::any_of
- Verificam condições em coleções inteiras em uma linha. <!-- .element: class="fragment" -->

---

## Namespaces
- Quase tudo na STL está dentro do `std::`. <!-- .element: class="fragment" -->
- Evite `using namespace std;` em projetos grandes e headers. <!-- .element: class="fragment" -->

---

## STL vs Performance Crítica
- Em 99% dos casos, a STL é mais rápida que sua própria implementação. <!-- .element: class="fragment" -->

---

## Benefícios da STL
- Segurança. <!-- .element: class="fragment" -->
- Padronização (qualquer programador C++ entende). <!-- .element: class="fragment" -->
- Portabilidade. <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Comece sempre pelo `std::vector`. <!-- .element: class="fragment" -->
- Use `std::map` para cadastros. <!-- .element: class="fragment" -->
- Explore a bibioteca `algorithm`. <!-- .element: class="fragment" -->

---

## Fim da Aula 13
- Próxima aula: Gerenciamento de Memória (Smart Pointers)!