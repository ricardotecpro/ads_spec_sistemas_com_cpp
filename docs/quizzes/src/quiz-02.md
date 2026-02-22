# Quiz 02 - Tipos de Dados e Variáveis 📦

1. Qual tipo de dado é usado para armazenar números decimais de precisão dupla?
    - [ ] float
    - [x] double
    - [ ] int
    - [ ] char
    > Explicação: O `double` possui o dobro da precisão do `float` para números reais.

2. O que o modificador `unsigned` faz com um `int`?
    - [ ] Torna o número fracionário
    - [ ] Aumenta a velocidade de processamento
    - [x] Permite apenas valores positivos, dobrando o limite superior
    - [ ] Protege a variável contra escrita
    > Explicação: Ao remover o sinal, o bit de sinal é usado para aumentar a capacidade numérica positiva.

3. Qual a forma correta de receber uma entrada do usuário em C++?
    - [ ] cin << variavel;
    - [x] cin >> variavel;
    - [ ] cout >> variavel;
    - [ ] scan(variavel);
    > Explicação: O operador `>>` (extração) retira dados do fluxo de entrada `std::cin`.

4. O que é o `std::endl`?
    - [ ] Um comando de encerramento
    - [x] Quebra de linha e limpeza do buffer (flush)
    - [ ] Um tipo de variável
    - [ ] Uma estrutura de controle
    > Explicação: Além de pular linha, o `endl` garante que o texto seja exibido imediatamente.

5. Qual o tamanho aproximado de um tipo `char` na memória?
    - [x] 1 byte
    - [ ] 2 bytes
    - [ ] 4 bytes
    - [ ] 8 bytes
    > Explicação: O `char` armazena um único caractere ASCII em 8 bits (1 byte).

6. Para que serve o operador `sizeof()`?
    - [ ] Calcular o logaritmo de um número
    - [x] Retornar o tamanho de um tipo ou variável em bytes
    - [ ] Definir o tamanho de um array
    - [ ] Converter int para float
    > Explicação: `sizeof` é um operador em tempo de compilação que informa o consumo de memória.

7. O que acontece se você tentar armazenar um valor decimal em uma variável `int`?
    - [ ] Erro de compilação
    - [ ] O programa trava
    - [x] O valor é truncado (a parte decimal é perdida)
    - [ ] O valor é arredondado para o mais próximo
    > Explicação: C++ corta a parte decimal sem arredondamento ao converter `float/double` para `int`.

8. Qual o valor booleano padrão para o número 0 em C++?
    - [ ] true
    - [x] false
    - [ ] null
    - [ ] undefined
    > Explicação: Em C++, 0 é avaliado como `false` e qualquer outro valor como `true`.

9. O que é um "CamelCase"?
    - [ ] Um tipo de dado do C++
    - [ ] Uma biblioteca de gráficos
    - [x] Uma convenção de nomenclatura de variáveis (ex: minhaVariavel)
    - [ ] Um erro de sintaxe
    > Explicação: É uma prática comum iniciar a primeira palavra em minúscula e as seguintes em maiúscula.

10. Como declaramos uma constante que não pode ter seu valor alterado?
    - [ ] final int x = 10;
    - [ ] static int x = 10;
    - [x] const int x = 10;
    - [ ] immutable int x = 10;
    > Explicação: A palavra-chave `const` impede modificações na variável após a inicialização.