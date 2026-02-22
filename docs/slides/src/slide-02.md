# Aula 02 - Tipos de Dados e Variáveis 📦

---

## O que é uma Variável?
- Um espaço reservado na memória RAM { .fragment }
- Possui um **Tipo**, um **Nome** e um **Valor** { .fragment }

---

## Tipos Primitivos
- `int`: Números inteiros { .fragment }
- `float` / `double`: Números reais { .fragment }
- `char`: Caractere único { .fragment }
- `bool`: Verdadeiro ou Falso { .fragment }

---

## Tabela de Tamanhos (Típico)
| Tipo | Tamanho | Faixa |
|------|---------|-------|
| char | 1 byte | -128 a 127 |
| int | 4 bytes | ~2 bilhões |
| double | 8 bytes | Alta precisão |

---

## Modificadores
- `signed` / `unsigned` { .fragment }
- `short` / `long` { .fragment }
- Exemplo: `unsigned int` (apenas positivos) { .fragment }

---

## Declaração e Inicialização
```cpp
int idade = 20;       // Inicialização direta
int ano(2023);        // Inicialização funcional
int pontos{100};      // Brace initialization (C++11)
```

---

## Por que usar { } ?
- Evita conversões perigosas (narrowing conversion) { .fragment }
- Exemplo: `int x{3.14};` gera erro de compilação! { .fragment }

---

## Nomenclatura (Boas Práticas)
- Use **camelCase** para variáveis { .fragment }
- Nomes significativos (`idade` em vez de `i`) { .fragment }
- Evite abreviações obscuras { .fragment }

---

## Entrada de Dados (std::cin)
```cpp
int numero;
std::cout << "Digite um valor: ";
std::cin >> numero;
```
- `>>` é o operador de extração { .fragment }

---

## O Problema do Espaço em Branco
- `std::cin` para no primeiro espaço { .fragment }
- Para frases, use `std::getline(std::cin, variavel)` { .fragment }

---

## Constantes
- Use `const` para valores que não mudam { .fragment }
```cpp
const double PI = 3.14159;
```

---

## Constexpr (C++11)
- Avaliado em tempo de compilação { .fragment }
- Muito mais eficiente para cálculos fixos { .fragment }

---

## Auto (Dedução de Tipo)
```cpp
auto x = 10;      // x é int
auto y = 3.14;    // y é double
```
- Facilita tipos complexos { .fragment }

---

## Booleans
- `true` (1) e `false` (0) { .fragment }
- Úteis para sinalizações (flags) { .fragment }

---

## Caracteres (char)
- Usa aspas simples: `'A'` { .fragment }
- Baseado na tabela ASCII { .fragment }

---

## Inteiros Grandes
- `long long int` para números astronômicos { .fragment }

---

## Debugging: Visualizar Memória
```cpp
std::cout << "Endereço: " << &idade << std::endl;
std::cout << "Tamanho: " << sizeof(idade) << " bytes" << std::endl;
```

---

## Overflow e Underflow
- O que acontece se passar do limite? { .fragment }
- O valor "dá a volta" (Circular) { .fragment }

---

## Resumo da Aula
1. Escolha o tipo correto { .fragment }
2. Prefira `{}` para inicializar { .fragment }
3. Use `const` sempre que possível { .fragment }

---

## Exercício Rápido
- Declare uma variável para sua altura e outra para seu peso. { .fragment }
- Calcule algo simples e imprima. { .fragment }

---

## Fim da Aula 02
- Próxima aula: Operadores e Expressões!