# Aula 14 - Memória Moderna 🧠

---

## O Pesadelo do C++ Antigo
- `new` sem `delete`. <!-- .element: class="fragment" -->
- Ponteiros soltos apontando para lixo. <!-- .element: class="fragment" -->
- Memory Leaks que travam servidores. <!-- .element: class="fragment" -->

---

## O Mundo Moderno (Modern C++)
- O objetivo é **zerar** o uso de `new` e `delete` manuais. <!-- .element: class="fragment" -->

---

## Smart Pointers (Ponteiros Inteligentes)
- Objetos que se comportam como ponteiros, mas limpam a memória sozinhos! <!-- .element: class="fragment" -->
- Baseados em **RAII**. <!-- .element: class="fragment" -->

---

## std::unique_ptr
- **Posse Exclusiva**. <!-- .element: class="fragment" -->
- Apenas um dono para o recurso. <!-- .element: class="fragment" -->
- Não pode ser copiado, apenas movido (`std::move`). <!-- .element: class="fragment" -->

---

## Criando um unique_ptr
```cpp
auto p = make_unique<Pizza>("Calabresa");
```
- Destruído automaticamente ao fim do escopo. <!-- .element: class="fragment" -->

---

## std::shared_ptr
- **Posse Compartilhada**. <!-- .element: class="fragment" -->
- Vários ponteiros apontam para o mesmo objeto. <!-- .element: class="fragment" -->
- Usa **Contador de Referências**. <!-- .element: class="fragment" -->

---

## Como funciona o Shared?
- Cada novo ponteiro incrementa o contador. <!-- .element: class="fragment" -->
- Cada destruição decrementa. <!-- .element: class="fragment" -->
- Quando chega a **Zero**, o objeto é deletado. <!-- .element: class="fragment" -->

---

## Criando um shared_ptr
```cpp
auto p1 = make_shared<int>(42);
auto p2 = p1; // Ambos apontam para o mesmo lugar
```

---

## std::weak_ptr
- O "Observador". <!-- .element: class="fragment" -->
- Aponta para um objeto gerenciado por `shared_ptr`, mas não impede que ele seja deletado. <!-- .element: class="fragment" -->

---

## Quando usar Weak?
- Para quebrar **Ciclos de Referência** (A aponta pra B, B aponta pra A). <!-- .element: class="fragment" -->
- Sem o weak, eles nunca seriam deletados! <!-- .element: class="fragment" -->

---

## Make Functions vs New
- Use `make_unique` e `make_shared`. <!-- .element: class="fragment" -->
- Mais seguros contra exceções e mais rápidos. <!-- .element: class="fragment" -->

---

## Custom Deletters
- Smart pointers podem ser usados para gerenciar outros recursos (como fechar sockets ou arquivos) automaticamente. <!-- .element: class="fragment" -->

---

## Move Semantics (Semântica de Movimentação)
- Em vez de copiar dados caros, "roubamos" os dados de um objeto temporário. <!-- .element: class="fragment" -->
- Transformamos Cópia em Transferência. <!-- .element: class="fragment" -->

---

## Lvalues vs Rvalues
- **Lvalue**: Variável com nome e endereço fixo. <!-- .element: class="fragment" -->
- **Rvalue**: Valor temporário (ex: resultado de uma conta). <!-- .element: class="fragment" -->

---

## std::move
- Transforma um Lvalue em um Rvalue, permitindo a movimentação. <!-- .element: class="fragment" -->

---

## Rule of Five
- Se sua classe gerencia memória, você precisa de: <!-- .element: class="fragment" -->
1. Destrutor <!-- .element: class="fragment" -->
2. Copy Constructor <!-- .element: class="fragment" -->
3. Copy Assignment <!-- .element: class="fragment" -->
4. Move Constructor <!-- .element: class="fragment" -->
5. Move Assignment <!-- .element: class="fragment" -->

---

## Rule of Zero
- Tente usar containers e smart pointers para que você **não precise** escrever nenhuma das 5 funções acima! <!-- .element: class="fragment" -->

---

## Prevenção de Memory Leaks
- Ferramentas como **Valgrind** ou **Sanitizers** ajudam a encontrar erros. <!-- .element: class="fragment" -->

---

## O Futuro: Garbage Collection no C++?
- C++ prefira o determinismo do RAII sobre o custo do GC. <!-- .element: class="fragment" -->

---

## Melhores Práticas de Memória
1. Use a Stack por padrão. <!-- .element: class="fragment" -->
2. Use `unique_ptr` se precisar de Heap. <!-- .element: class="fragment" -->
3. Use `shared_ptr` apenas se a posse for realmente dividida. <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Esqueça o `new` e o `delete`. <!-- .element: class="fragment" -->
- RAII é a lei. <!-- .element: class="fragment" -->
- Smart pointers tornam o C++ tão seguro quanto linguagens modernas. <!-- .element: class="fragment" -->

---

## Fim da Aula 14
- Próxima aula: Multiplataforma e Build (CMake)!