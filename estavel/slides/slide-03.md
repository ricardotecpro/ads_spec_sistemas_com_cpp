# Aula 03 - Operadores e Expressões ➕

---

## O que são Operadores?
- Símbolos que instruem o compilador a realizar manipulações matemáticas ou lógicas. <!-- .element: class="fragment" -->

---

## Operadores Aritméticos
- `+` (Adição) <!-- .element: class="fragment" -->
- `-` (Subtração) <!-- .element: class="fragment" -->
- `*` (Multiplicação) <!-- .element: class="fragment" -->
- `/` (Divisão) <!-- .element: class="fragment" -->
- `%` (Módulo - Resto da divisão) <!-- .element: class="fragment" -->

---

## Divisão Inteira vs Real
- `10 / 3` resulta em `3` (inteiro) <!-- .element: class="fragment" -->
- `10.0 / 3.0` resulta em `3.333` (double) <!-- .element: class="fragment" -->

---

## O Operador de Módulo (%)
- Funciona apenas com **inteiros** <!-- .element: class="fragment" -->
- Exemplo: `7 % 2` é `1` <!-- .element: class="fragment" -->
- Muito usado para verificar se um número é par/ímpar <!-- .element: class="fragment" -->

---

## Incremento e Decremento
- `x++` (Pós-incremento) <!-- .element: class="fragment" -->
- `++x` (Pré-incremento) <!-- .element: class="fragment" -->
- `x--` / `--x` <!-- .element: class="fragment" -->

---

## Diferença do Pré/Pós
```cpp
int a = 5;
int b = a++;  // b=5, a=6
int c = ++a;  // c=7, a=7
```

---

## Operadores de Atribuição Composta
- `x += 5` (x = x + 5) <!-- .element: class="fragment" -->
- `x -= 2` <!-- .element: class="fragment" -->
- `x *= 3` <!-- .element: class="fragment" -->
- `x /= 4` <!-- .element: class="fragment" -->

---

## Operadores Relacionais (Comparação)
- `==` (Igual a) <!-- .element: class="fragment" -->
- `!=` (Diferente de) <!-- .element: class="fragment" -->
- `>` / `<` <!-- .element: class="fragment" -->
- `>=` / `<=` <!-- .element: class="fragment" -->

---

## Cuidado com `=` vs `==`
- `=` atribui valor <!-- .element: class="fragment" -->
- `==` compara igualdade <!-- .element: class="fragment" -->
- Um erro comum é usar `=` dentro de um `if` <!-- .element: class="fragment" -->

---

## Operadores Lógicos
- `&&` (AND / E) <!-- .element: class="fragment" -->
- `||` (OR / OU) <!-- .element: class="fragment" -->
- `!` (NOT / NÃO) <!-- .element: class="fragment" -->

---

## Tabela Verdade (AND)
| A | B | A && B |
|---|---|--------|
| T | T | T |
| T | F | F |
| F | F | F |

---

## Tabela Verdade (OR)
| A | B | A \|\| B |
|---|---|----------|
| T | F | T |
| F | F | F |

---

## Circuitos Curtos (Short-circuit)
- No `&&`, se o primeiro for `false`, o segundo nem é testado. <!-- .element: class="fragment" -->
- No `||`, se o primeiro for `true`, o segundo nem é testado. <!-- .element: class="fragment" -->

---

## Operador Ternário
- `condição ? valor_se_verdadeiro : valor_se_falso` <!-- .element: class="fragment" -->
- `string status = (nota >= 7) ? "Aprovado" : "Reprovado";` <!-- .element: class="fragment" -->

---

## Casting (Conversão de Tipo)
- **Implícito**: O compilador faz sozinho (ex: int -> double) <!-- .element: class="fragment" -->
- **Explícito**: Nós forçamos a barra. <!-- .element: class="fragment" -->

---

## static_cast (C++ Moderno)
```cpp
double resultado = static_cast<double>(total) / 5;
```
- Mais seguro que o cast estilo C `(double)total`. <!-- .element: class="fragment" -->

---

## Precedência de Operadores
1. Parentêses `()` <!-- .element: class="fragment" -->
2. Multiplicação/Divisão `* / %` <!-- .element: class="fragment" -->
3. Soma/Subtração `+ -` <!-- .element: class="fragment" -->
4. Comparação `< > <= >=` <!-- .element: class="fragment" -->
5. Igualdade `== !=` <!-- .element: class="fragment" -->

---

## Expressões Matemáticas Complexas
```cpp
float x = (a + b) * c / (d - e);
```

---

## Manipulação de Bits (Bitwise)
- `&` (AND), `|` (OR), `^` (XOR), `~` (NOT) <!-- .element: class="fragment" -->
- Usado em sistemas embarcados e drivers. <!-- .element: class="fragment" -->

---

## Shift de Bits
- `<<` (Left shift) <!-- .element: class="fragment" -->
- `>>` (Right shift) <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Entender a divisão inteira é crucial. <!-- .element: class="fragment" -->
- O operador ternário limpa o código. <!-- .element: class="fragment" -->
- Cuidado com a precedência! <!-- .element: class="fragment" -->

---

## Fim da Aula 03
- Próxima aula: Estruturas de Controle!