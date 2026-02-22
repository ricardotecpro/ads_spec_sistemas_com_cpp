# Aula 14 - Memória Moderna 🧠

---

## O Pesadelo do C++ Antigo
- `new` sem `delete`. { .fragment }
- Ponteiros soltos apontando para lixo. { .fragment }
- Memory Leaks que travam servidores. { .fragment }

---

## O Mundo Moderno (Modern C++)
- O objetivo é **zerar** o uso de `new` e `delete` manuais. { .fragment }

---

## Smart Pointers (Ponteiros Inteligentes)
- Objetos que se comportam como ponteiros, mas limpam a memória sozinhos! { .fragment }
- Baseados em **RAII**. { .fragment }

---

## std::unique_ptr
- **Posse Exclusiva**. { .fragment }
- Apenas um dono para o recurso. { .fragment }
- Não pode ser copiado, apenas movido (`std::move`). { .fragment }

---

## Criando um unique_ptr
```cpp
auto p = make_unique<Pizza>("Calabresa");
```
- Destruído automaticamente ao fim do escopo. { .fragment }

---

## std::shared_ptr
- **Posse Compartilhada**. { .fragment }
- Vários ponteiros apontam para o mesmo objeto. { .fragment }
- Usa **Contador de Referências**. { .fragment }

---

## Como funciona o Shared?
- Cada novo ponteiro incrementa o contador. { .fragment }
- Cada destruição decrementa. { .fragment }
- Quando chega a **Zero**, o objeto é deletado. { .fragment }

---

## Criando um shared_ptr
```cpp
auto p1 = make_shared<int>(42);
auto p2 = p1; // Ambos apontam para o mesmo lugar
```

---

## std::weak_ptr
- O "Observador". { .fragment }
- Aponta para um objeto gerenciado por `shared_ptr`, mas não impede que ele seja deletado. { .fragment }

---

## Quando usar Weak?
- Para quebrar **Ciclos de Referência** (A aponta pra B, B aponta pra A). { .fragment }
- Sem o weak, eles nunca seriam deletados! { .fragment }

---

## Make Functions vs New
- Use `make_unique` e `make_shared`. { .fragment }
- Mais seguros contra exceções e mais rápidos. { .fragment }

---

## Custom Deletters
- Smart pointers podem ser usados para gerenciar outros recursos (como fechar sockets ou arquivos) automaticamente. { .fragment }

---

## Move Semantics (Semântica de Movimentação)
- Em vez de copiar dados caros, "roubamos" os dados de um objeto temporário. { .fragment }
- Transformamos Cópia em Transferência. { .fragment }

---

## Lvalues vs Rvalues
- **Lvalue**: Variável com nome e endereço fixo. { .fragment }
- **Rvalue**: Valor temporário (ex: resultado de uma conta). { .fragment }

---

## std::move
- Transforma um Lvalue em um Rvalue, permitindo a movimentação. { .fragment }

---

## Rule of Five
- Se sua classe gerencia memória, você precisa de: { .fragment }
1. Destrutor { .fragment }
2. Copy Constructor { .fragment }
3. Copy Assignment { .fragment }
4. Move Constructor { .fragment }
5. Move Assignment { .fragment }

---

## Rule of Zero
- Tente usar containers e smart pointers para que você **não precise** escrever nenhuma das 5 funções acima! { .fragment }

---

## Prevenção de Memory Leaks
- Ferramentas como **Valgrind** ou **Sanitizers** ajudam a encontrar erros. { .fragment }

---

## O Futuro: Garbage Collection no C++?
- C++ prefira o determinismo do RAII sobre o custo do GC. { .fragment }

---

## Melhores Práticas de Memória
1. Use a Stack por padrão. { .fragment }
2. Use `unique_ptr` se precisar de Heap. { .fragment }
3. Use `shared_ptr` apenas se a posse for realmente dividida. { .fragment }

---

## Resumo da Aula
- Esqueça o `new` e o `delete`. { .fragment }
- RAII é a lei. { .fragment }
- Smart pointers tornam o C++ tão seguro quanto linguagens modernas. { .fragment }

---

## Fim da Aula 14
- Próxima aula: Multiplataforma e Build (CMake)!