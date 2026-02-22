# Quiz 12 - Sobrecarga de Operadores ⚖️

1. O que é a Sobrecarga de Operadores?
    - [ ] Quando usamos "+" muitas vezes
    - [ ] Um erro de memória
    - [x] Atribuir novos comportamentos aos operadores nativos (+, -, <<) para nossas classes
    - [ ] Mudar o sentido da matemática
    > Explicação: Ela permite que usemos símbolos matemáticos intuitivos em nossos próprios objetos.

2. Qual palavra-chave é usada para sobrecarregar um operador?
    - [ ] function
    - [ ] overload
    - [x] operator
    - [ ] sym
    > Explicação: Usamos `operator+`, `operator<<`, etc., como nome da função.

3. Qual operador é comumente sobrecarregado para facilitar a impressão com `cout`?
    - [ ] >>
    - [x] <<
    - [ ] +
    - [ ] ()
    > Explicação: Sobrecargar o operador de inserção em fluxo `<<` permite `cout << meuObjeto;`.

4. Podemos sobrecarregar TODOS os operadores do C++?
    - [ ] Sim
    - [x] Não (ex: . , :: , sizeof , ?: não podem ser sobrecarregados)
    - [ ] Apenas os de matemática
    - [ ] Apenas se a classe for pública
    > Explicação: Alguns operadores básicos são protegidos pela linguagem para manter a consistência da sintaxe.

5. O que é uma "Friend Function" no contexto de sobrecarga?
    - [ ] Uma função amigável ao usuário
    - [x] Uma função externa que tem permissão para acessar membros privados da classe
    - [ ] Uma função que não retorna nada
    - [ ] Uma função rápida
    > Explicação: Frequentemente usada na sobrecarga de `<<`, onde a função não pertence à classe mas precisa ler seus dados privados.

6. Qual o benefício principal da sobrecarga de operadores?
    - [ ] Deixar o código mais rápido
    - [x] Maior legibilidade e intuitividade do código
    - [ ] Economia de memória
    - [ ] Proteção contra vírus
    > Explicação: É mais fácil ler `vetorA + vetorB` do que `vetorA.somar(vetorB)`.

7. Podemos criar novos operadores (ex: ** para potência) no C++?
    - [ ] Sim
    - [x] Não, apenas sobrecarregar os existentes
    - [ ] Apenas se o compilador for o GCC
    - [ ] Sim, usando macros
    > Explicação: C++ não permite a criação de novos símbolos de operadores.

8. Qual o tipo de retorno comum para a sobrecarga do operador `<<`?
    - [ ] void
    - [ ] int
    - [x] std::ostream&
    - [ ] bool
    > Explicação: Retornar a referência do fluxo permite o encadeamento (ex: `cout << a << b << c;`).

9. O que acontece se você sobrecarregar o operador `+` para fazer uma subtração?
    - [ ] O compilador gera erro
    - [ ] O computador explode
    - [x] O código funciona, mas causa extrema confusão lógica
    - [ ] O programa trava
    > Explicação: O C++ permite, mas viola o princípio da menor surpresa e é uma péssima prática.

10. O que é a sobrecarga do operador de atribuição (`operator=`)?
    - [ ] Definir o valor inicial
    - [x] Controlar como os dados são copiados de um objeto para outro já existente
    - [ ] Deletar o objeto
    - [ ] Comparar se são iguais
    > Explicação: Crucial para gerenciar corretamente a cópia de objetos que possuem memória dinâmica.