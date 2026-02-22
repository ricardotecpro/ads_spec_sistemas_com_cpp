# Aula 03 - Operadores e Expressões ➕

---

## O que são Operadores?
- Símbolos que instruem o compilador a realizar manipulações matemáticas ou lógicas. { .fragment }

---

## Operadores Aritméticos
- `+` (Adição) { .fragment }
- `-` (Subtração) { .fragment }
- `*` (Multiplicação) { .fragment }
- `/` (Divisão) { .fragment }
- `%` (Módulo - Resto da divisão) { .fragment }

---

## Divisão Inteira vs Real
- `10 / 3` resulta em `3` (inteiro) { .fragment }
- `10.0 / 3.0` resulta em `3.333` (double) { .fragment }

---

## O Operador de Módulo (%)
- Funciona apenas com **inteiros** { .fragment }
- Exemplo: `7 % 2` é `1` { .fragment }
- Muito usado para verificar se um número é par/ímpar { .fragment }

---

## Incremento e Decremento
- `x++` (Pós-incremento) { .fragment }
- `++x` (Pré-incremento) { .fragment }
- `x--` / `--x` { .fragment }

---

## Diferença do Pré/Pós
```cpp
int a = 5;
int b = a++;  // b=5, a=6
int c = ++a;  // c=7, a=7
```

---

## Operadores de Atribuição Composta
- `x += 5` (x = x + 5) { .fragment }
- `x -= 2` { .fragment }
- `x *= 3` { .fragment }
- `x /= 4` { .fragment }

---

## Operadores Relacionais (Comparação)
- `==` (Igual a) { .fragment }
- `!=` (Diferente de) { .fragment }
- `>` / `<` { .fragment }
- `>=` / `<=` { .fragment }

---

## Cuidado com `=` vs `==`
- `=` atribui valor { .fragment }
- `==` compara igualdade { .fragment }
- Um erro comum é usar `=` dentro de um `if` { .fragment }

---

## Operadores Lógicos
- `&&` (AND / E) { .fragment }
- `||` (OR / OU) { .fragment }
- `!` (NOT / NÃO) { .fragment }

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
- No `&&`, se o primeiro for `false`, o segundo nem é testado. { .fragment }
- No `||`, se o primeiro for `true`, o segundo nem é testado. { .fragment }

---

## Operador Ternário
- `condição ? valor_se_verdadeiro : valor_se_falso` { .fragment }
- `string status = (nota >= 7) ? "Aprovado" : "Reprovado";` { .fragment }

---

## Casting (Conversão de Tipo)
- **Implícito**: O compilador faz sozinho (ex: int -> double) { .fragment }
- **Explícito**: Nós forçamos a barra. { .fragment }

---

## static_cast (C++ Moderno)
```cpp
double resultado = static_cast<double>(total) / 5;
```
- Mais seguro que o cast estilo C `(double)total`. { .fragment }

---

## Precedência de Operadores
1. Parentêses `()` { .fragment }
2. Multiplicação/Divisão `* / %` { .fragment }
3. Soma/Subtração `+ -` { .fragment }
4. Comparação `< > <= >=` { .fragment }
5. Igualdade `== !=` { .fragment }

---

## Expressões Matemáticas Complexas
```cpp
float x = (a + b) * c / (d - e);
```

---

## Manipulação de Bits (Bitwise)
- `&` (AND), `|` (OR), `^` (XOR), `~` (NOT) { .fragment }
- Usado em sistemas embarcados e drivers. { .fragment }

---

## Shift de Bits
- `<<` (Left shift) { .fragment }
- `>>` (Right shift) { .fragment }

---

## Resumo da Aula
- Entender a divisão inteira é crucial. { .fragment }
- O operador ternário limpa o código. { .fragment }
- Cuidado com a precedência! { .fragment }

---

## Fim da Aula 03
- Próxima aula: Estruturas de Controle!