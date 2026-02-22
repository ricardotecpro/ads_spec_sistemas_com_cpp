# Quiz 13 - STL (Standard Template Library) ⚙️

1. O que significa a sigla STL?
    - [ ] System Total Library
    - [x] Standard Template Library (Biblioteca de Templates Padrão)
    - [ ] Sequential Text Logic
    - [ ] Static Tool Language
    > Explicação: É a biblioteca fundamental do C++ que fornece containers, algoritmos e iteradores.

2. Qual o container mais utilizado na STL para armazenar sequências dinâmicas?
    - [ ] std::list
    - [ ] std::stack
    - [x] std::vector
    - [ ] std::map
    > Explicação: O `vector` é um array dinâmico contíguo na memória, sendo o mais eficiente para a maioria dos casos.

3. Como adicionamos um elemento ao final de um `std::vector`?
    - [ ] v.add()
    - [ ] v.insert_end()
    - [x] v.push_back() ou v.emplace_back()
    - [ ] v.append()
    > Explicação: `push_back` insere uma cópia, enquanto `emplace_back` constrói o objeto diretamente no vetor.

4. Para que serve um "Iterador"?
    - [ ] Para contar números
    - [x] Para navegar e acessar elementos de containers de forma padronizada
    - [ ] Para deletar o container
    - [ ] Para acelerar o loop
    > Explicação: Iteradores agem como ponteiros inteligentes que funcionam com qualquer tipo de container da STL.

5. Qual a função do container `std::map`?
    - [ ] Desenhar mapas geográficos
    - [ ] Armazenar apenas números
    - [x] Armazenar pares de Chave-Valor (Dicionário)
    - [ ] Criar listas ligadas
    > Explicação: O `map` associa uma chave única a um valor de forma ordenada.

6. Qual biblioteca (`#include`) devemos usar para o comando `std::sort()`?
    - [ ] <iostream>
    - [ ] <vector>
    - [x] <algorithm>
    - [ ] <math>
    > Explicação: O cabeçalho `algorithm` contém as funções genéricas de manipulação de coleções.

7. O que é um "Template" no C++?
    - [ ] Um código pronto para copiar
    - [x] Uma forma de criar funções ou classes genéricas que funcionam com qualquer tipo de dado
    - [ ] Um estilo visual de código
    - [ ] Uma regra de indentação
    > Explicação: Templates permitem o Polimorfismo Paramétrico, evitando a repetição de código para diferentes tipos.

8. Qual a vantagem de `std::list` sobre `std::vector`?
    - [ ] É mais rápida para acesso aleatório
    - [ ] Consome menos memória
    - [x] É mais eficiente para inserções e remoções no meio da sequência
    - [ ] É mais fácil de usar
    > Explicação: Por ser uma lista duplamente ligada, ela não precisa mover elementos ao inserir/remover.

9. O que o algoritmo `std::find()` retorna se não encontrar o elemento?
    - [ ] NULL
    - [ ] 0
    - [x] O iterador para o fim do container (`end()`)
    - [ ] Um erro fatal
    > Explicação: Na STL, o insucesso de uma busca é sinalizado pelo iterador `end()`.

10. O que significa o `auto` no C++ moderno?
    - [ ] Carros autônomos
    - [x] Dedução automática do tipo da variável pelo compilador
    - [ ] Variável global
    - [ ] Loop automático
    > Explicação: `auto` simplifica o código, especialmente ao lidar com tipos complexos de iteradores da STL.