# Quiz 14 - Gerenciamento de Memória 🧠

1. O que significa a sigla RAII?
    - [ ] Real-time AI Integration
    - [x] Resource Acquisition Is Initialization (Aquisição de Recurso é Inicialização)
    - [ ] Random Access Internal Interface
    - [ ] Redundant Array of Independent Integers
    > Explicação: É o padrão onde o ciclo de vida de um recurso (memória/arquivo) é atrelado à vida útil de um objeto.

2. Por que o uso manual de `new` e `delete` é desencorajado no C++ Moderno?
    - [ ] Porque é muito lento
    - [ ] Porque o C++ vai remover esses comandos
    - [x] Porque é fácil esquecer o delete, causando vazamentos de memória (mem leaks)
    - [ ] Porque as bibliotecas não suportam
    > Explicação: Smart Pointers automatizam esse processo, tornando o código mais seguro.

3. Qual a principal característica do `std::unique_ptr`?
    - [ ] Permite que vários ponteiros apontem para o mesmo lugar
    - [x] Posse exclusiva: apenas um unique_ptr pode ser dono do objeto
    - [ ] Ele deleta o objeto após 10 segundos
    - [ ] Ele converte o objeto em string
    > Explicação: Ao ser destruído ou sair de escopo, ele limpa a memória automaticamente.

4. O que o `std::shared_ptr` utiliza para gerenciar a memória?
    - [ ] Inteligência Artificial
    - [x] Contador de referências (Reference Counting)
    - [ ] Um timer interno
    - [ ] Uma lista de espera
    > Explicação: Ele mantém conta de quantos ponteiros compartilham o objeto; quando chega a zero, deleta o objeto.

5. Qual smart pointer deve ser usado para quebrar ciclos de referência (A aponta pra B e vice-versa)?
    - [ ] unique_ptr
    - [ ] shared_ptr
    - [x] weak_ptr
    - [ ] auto_ptr
    > Explicação: O `weak_ptr` observa o objeto sem aumentar o contador de referências do `shared_ptr`.

6. Qual comando usamos para criar um `unique_ptr` de forma segura?
    - [ ] new unique_ptr
    - [x] std::make_unique<Tipo>(valor)
    - [ ] create_unique(valor)
    - [ ] malloc(ptr)
    > Explicação: `make_unique` é mais seguro contra exceções e mais performático.

7. O que acontece com um `unique_ptr` ao final de um bloco `{}`?
    - [ ] Ele continua existindo
    - [ ] Ele é movido para o topo do programa
    - [x] Ele é destruído e a memória apontada é liberada automaticamente
    - [ ] O programa trava
    > Explicação: Este é o comportamento fundamental do RAII aplicado a ponteiros.

8. Para que serve o comando `std::move()`?
    - [ ] Para mover um arquivo no HD
    - [x] Para transferir a posse de um recurso (ex: unique_ptr) de uma variável para outra
    - [ ] Para animar objetos na tela
    - [ ] Para ordenar um vetor rápido
    > Explicação: O "move" evita a cópia custosa de dados, apenas trocando quem é o "dono".

9. O que é um "Dangling Pointer"?
    - [ ] Um ponteiro que aponta para o infinito
    - [x] Um ponteiro que aponta para um endereço de memória que já foi liberado
    - [ ] Um ponteiro que não tem nome
    - [ ] Um ponteiro muito rápido
    > Explicação: Acessar um dangling pointer causa o erro de "Segmentation Fault".

10. A STL (Standard Template Library) faz uso intensivo de RAII?
    - [x] Sim, containers como vector e string gerenciam sua própria memória usando RAII
    - [ ] Não, eles usam Garbage Collection
    - [ ] Apenas se o programador ativar
    - [ ] Apenas no C++23
    > Explicação: Ao sair de escopo, um `std::vector` limpa automaticamente todos os seus elementos da memória.