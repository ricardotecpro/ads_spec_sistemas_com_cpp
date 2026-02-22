# Quiz 04 - Estruturas de Controle 🚦

1. Qual a principal diferença entre `while` e `do-while`?
    - [ ] Nenhuma, são iguais
    - [ ] while executa pelo menos uma vez
    - [x] do-while executa pelo menos uma vez, mesmo que a condição seja falsa
    - [ ] do-while é mais rápido
    > Explicação: No `do-while`, a condição é testada no FINAL do bloco.

2. Qual estrutura é mais recomendada quando sabemos o número exato de repetições?
    - [ ] if
    - [ ] while
    - [x] for
    - [ ] switch
    > Explicação: O `for` agrupa inicialização, condição e incremento de forma clara.

3. Para que serve o comando `break` dentro de um `switch`?
    - [ ] Para quebrar o computador
    - [x] Para interromper a execução e sair do switch
    - [ ] Para pular para o próximo case
    - [ ] Para reiniciar o programa
    > Explicação: Sem o `break`, o código continuaria executando os cases abaixo (fall-through).

4. O que o comando `continue` faz dentro de um loop?
    - [ ] Para o loop completamente
    - [x] Pula a iteração atual e vai para a próxima
    - [ ] Reinicia o loop do zero
    - [ ] Sai da função
    > Explicação: `continue` ignora o restante do código do loop apenas naquela volta.

5. Qual o valor final de `soma` no código: `for(int i=0; i<3; i++) soma += i;` (inicial: soma=0)?
    - [ ] 0
    - [ ] 1
    - [x] 3
    - [ ] 6
    > Explicação: As iterações adicionam 0, 1 e 2. (0+1+2 = 3).

6. Qual estrutura é usada para selecionar um de muitos blocos de código baseados em uma variável?
    - [ ] if-else
    - [x] switch
    - [ ] for
    - [ ] while
    > Explicação: O `switch` é ideal para múltiplas condições baseadas em um único valor constante.

7. O que constitui um "Loop Infinito"?
    - [ ] Um erro de sintaxe
    - [ ] Um loop que dura 1 hora
    - [x] Um loop onde a condição de parada nunca é atingida
    - [ ] Um loop que usa muita memória
    > Explicação: Se a condição for sempre `true`, o programa ficará travado nele.

8. Podemos usar `float` no `switch` (case)?
    - [ ] Sim
    - [x] Não, apenas tipos integrais (int, char, enum)
    - [ ] Apenas se for convertido
    - [ ] Sim, no C++20
    > Explicação: O `switch` exige valores que possam ser comparados de forma exata e constante.

9. Qual a saída de `if(0) cout << "A"; else cout << "B";`?
    - [ ] A
    - [x] B
    - [ ] AB
    - [ ] Erro
    > Explicação: Em C++, 0 é `false`, logo o bloco `else` é executado.

10. Como representamos "Diferente de" em uma condição?
    - [ ] <>
    - [ ] #
    - [x] !=
    - [ ] !==
    > Explicação: O operador de desigualdade em C++ é `!=`.