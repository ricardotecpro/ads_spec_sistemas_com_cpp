# Quiz 07 - Ponteiros e Referências 👆

1. O que um ponteiro armazena?
    - [ ] Um número inteiro
    - [x] Um endereço de memória
    - [ ] Um texto longo
    - [ ] Uma cópia da variável
    > Explicação: Ponteiros são variáveis que "apontam" para locais físicos na memória RAM.

2. Qual operador usamos para obter o endereço de uma variável?
    - [ ] *
    - [x] &
    - [ ] ->
    - [ ] @
    > Explicação: O operador `&` (address-of) retorna o local onde a variável reside.

3. O que faz o operador `*` quando aplicado a um ponteiro (ex: `*ptr`)?
    - [ ] Multiplica o endereço
    - [x] Acessa o valor armazenado no endereço (Desreferência)
    - [ ] Deleta o ponteiro
    - [ ] Cria um novo ponteiro
    > Explicação: O operador de desreferência permite ler ou alterar o valor real apontado.

4. O que é um "Null Pointer" (`nullptr`)?
    - [ ] Um erro fatal
    - [x] Um ponteiro que não aponta para nenhum lugar válido
    - [ ] Um ponteiro que aponta para o número zero
    - [ ] Um ponteiro fantasma
    > Explicação: `nullptr` é a forma moderna e segura de indicar que um ponteiro está "vazio".

5. Qual a principal diferença entre Ponteiro e Referência?
    - [ ] Ponteiros são mais novos
    - [x] Referências não podem ser nulas nem reatribuídas
    - [ ] Referências ocupam mais memória
    - [ ] Não há diferença técnica
    > Explicação: Uma referência atua como um alias constante para um objeto já existente.

6. Onde a memória alocada com `new` é guardada?
    - [ ] Na Stack
    - [x] No Heap
    - [ ] No cache do processador
    - [ ] No HD
    > Explicação: O Heap é a região de memória para alocações dinâmicas gerenciadas manualmente.

7. O que acontece se você usar `new` e esquecer de usar `delete`?
    - [ ] O computador reinicia
    - [x] Vazamento de Memória (Memory Leak)
    - [ ] O C++ limpa sozinho depois de 5 minutos
    - [ ] Erro de compilação
    > Explicação: A memória continuará marcada como "em uso", mesmo que o programa não precise mais dela.

8. Para que serve o operador `->`?
    - [ ] Para fazer uma seta no código
    - [x] Acessar membros de uma struct/classe através de um ponteiro
    - [ ] Comparar se um número é menor que outro
    - [ ] Alocar memória
    > Explicação: `ptr->membro` é um atalho para `(*ptr).membro`.

9. O que é "Aritmética de Ponteiros"?
    - [ ] Somar dois ponteiros (ptr1 + ptr2)
    - [x] Somar ou subtrair inteiros de um ponteiro para navegar na memória
    - [ ] Calcular o logaritmo de um ponteiro
    - [ ] Dividir endereços de memória
    > Explicação: Ao somar 1 a um ponteiro, ele pula para o próximo endereço baseado no tamanho do tipo.

10. Como liberamos um array alocado dinamicamente (ex: `int* a = new int[10]`)?
    - [ ] delete a;
    - [x] delete[] a;
    - [ ] free(a);
    - [ ] remove a;
    > Explicação: O uso dos colchetes `[]` informa ao compilador que ele deve destruir múltiplos elementos.