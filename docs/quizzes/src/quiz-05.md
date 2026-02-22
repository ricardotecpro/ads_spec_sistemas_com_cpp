# Quiz 05 - Funções 🧩

1. O que é o "Protótipo" de uma função?
    - [ ] O código final da função
    - [x] Uma declaração antecipada da assinatura da função (antes da main)
    - [ ] O nome da variável de retorno
    - [ ] Um erro de compilação
    > Explicação: O protótipo avisa ao compilador que a função existe, permitindo chamá-la antes de sua definição completa.

2. Qual a diferença de uma função `void`?
    - [ ] Ela só aceita números
    - [x] Ela não retorna nenhum valor
    - [ ] Ela não aceita parâmetros
    - [ ] Ela é executada mais rápido
    > Explicação: O tipo `void` indica que a função executa uma tarefa mas não devolve um resultado numérico ou textual.

3. O que acontece na Passagem por Valor?
    - [x] Uma cópia da variável é enviada para a função
    - [ ] O endereço da variável é enviado
    - [ ] A variável original é alterada pela função
    - [ ] O programa trava se a variável for grande
    > Explicação: Na passagem por valor, as alterações feitas dentro da função ficam restritas ao escopo local da função.

4. Como indicamos uma Passagem por Referência no C++?
    - [ ] Usando o símbolo *
    - [x] Usando o símbolo & no parâmetro
    - [ ] Colocando a palavra "ref"
    - [ ] Usando parênteses duplos
    > Explicação: O operador `&` cria um apelido (referência) para a variável original.

5. O que é a Sobrecarga de Funções (Overloading)?
    - [ ] Quando uma função tem código demais
    - [ ] Quando a função causa erro de memória
    - [x] Ter várias funções com o mesmo nome, mas parâmetros diferentes
    - [ ] Renomear uma função existente
    > Explicação: O compilador diferencia as funções pela quantidade ou tipo dos argumentos passados.

6. Para que serve a palavra-chave `inline`?
    - [ ] Para escrever tudo em uma linha só
    - [x] Sugerir ao compilador trocar a chamada da função pelo seu código interno
    - [ ] Proteger a função contra cópias
    - [ ] Tornar a função global
    > Explicação: `inline` pode acelerar funções muito pequenas, evitando o overhead de uma chamada de função real.

7. Onde as variáveis locais são armazenadas?
    - [ ] No Heap
    - [ ] No disco rígido
    - [x] Na Stack (Pilha)
    - [ ] No processador
    > Explicação: Variáveis locais e parâmetros de funções são alocados e desalocados automaticamente na Stack.

8. O que é uma função recursiva?
    - [ ] Uma função que nunca termina
    - [x] Uma função que chama a si mesma
    - [ ] Uma função que retorna um erro
    - [ ] Uma função matemática complexa
    > Explicação: Recursividade é quando uma função utiliza sua própria definição para resolver subproblemas.

9. Qual o comando usado para devolver um valor de uma função para quem a chamou?
    - [ ] send
    - [ ] give
    - [x] return
    - [ ] output
    > Explicação: O `return` finaliza a execução da função e entrega o valor resultante.

10. Pode-se ter uma função dentro de outra função (Nested Functions) no C++ padrão?
    - [ ] Sim, normalmente
    - [x] Não, todas as funções devem ser declaradas no escopo global ou de classe
    - [ ] Apenas com a palavra-chave "inner"
    - [ ] Sim, se forem void
    > Explicação: C++ não suporta funções aninhadas diretamente, embora permita funções Lambda (desde o C++11).