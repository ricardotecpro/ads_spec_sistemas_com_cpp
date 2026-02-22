# Aula 02 - Tipos de Dados e Variáveis 📦

---

## O que é uma Variável?
- Um espaço reservado na memória RAM <!-- .element: class="fragment" -->
- Possui um **Tipo**, um **Nome** e um **Valor** <!-- .element: class="fragment" -->

---

## Tipos Primitivos
- `int`: Números inteiros <!-- .element: class="fragment" -->
- `float` / `double`: Números reais <!-- .element: class="fragment" -->
- `char`: Caractere único <!-- .element: class="fragment" -->
- `bool`: Verdadeiro ou Falso <!-- .element: class="fragment" -->

---

## Tabela de Tamanhos (Típico)
| Tipo | Tamanho | Faixa |
|------|---------|-------|
| char | 1 byte | -128 a 127 |
| int | 4 bytes | ~2 bilhões |
| double | 8 bytes | Alta precisão |

---

## Modificadores
- `signed` / `unsigned` <!-- .element: class="fragment" -->
- `short` / `long` <!-- .element: class="fragment" -->
- Exemplo: `unsigned int` (apenas positivos) <!-- .element: class="fragment" -->

---

## Declaração e Inicialização
```cpp
int idade = 20;       // Inicialização direta
int ano(2023);        // Inicialização funcional
int pontos{100};      // Brace initialization (C++11)
```

---

## Por que usar { } ?
- Evita conversões perigosas (narrowing conversion) <!-- .element: class="fragment" -->
- Exemplo: `int x{3.14};` gera erro de compilação! <!-- .element: class="fragment" -->

---

## Nomenclatura (Boas Práticas)
- Use **camelCase** para variáveis <!-- .element: class="fragment" -->
- Nomes significativos (`idade` em vez de `i`) <!-- .element: class="fragment" -->
- Evite abreviações obscuras <!-- .element: class="fragment" -->

---

## Entrada de Dados (std::cin)
```cpp
int numero;
std::cout << "Digite um valor: ";
std::cin >> numero;
```
- `>>` é o operador de extração <!-- .element: class="fragment" -->

---

## O Problema do Espaço em Branco
- `std::cin` para no primeiro espaço <!-- .element: class="fragment" -->
- Para frases, use `std::getline(std::cin, variavel)` <!-- .element: class="fragment" -->

---

## Constantes
- Use `const` para valores que não mudam <!-- .element: class="fragment" -->
```cpp
const double PI = 3.14159;
```

---

## Constexpr (C++11)
- Avaliado em tempo de compilação <!-- .element: class="fragment" -->
- Muito mais eficiente para cálculos fixos <!-- .element: class="fragment" -->

---

## Auto (Dedução de Tipo)
```cpp
auto x = 10;      // x é int
auto y = 3.14;    // y é double
```
- Facilita tipos complexos <!-- .element: class="fragment" -->

---

## Booleans
- `true` (1) e `false` (0) <!-- .element: class="fragment" -->
- Úteis para sinalizações (flags) <!-- .element: class="fragment" -->

---

## Caracteres (char)
- Usa aspas simples: `'A'` <!-- .element: class="fragment" -->
- Baseado na tabela ASCII <!-- .element: class="fragment" -->

---

## Inteiros Grandes
- `long long int` para números astronômicos <!-- .element: class="fragment" -->

---

## Debugging: Visualizar Memória
```cpp
std::cout << "Endereço: " << &idade << std::endl;
std::cout << "Tamanho: " << sizeof(idade) << " bytes" << std::endl;
```

---

## Overflow e Underflow
- O que acontece se passar do limite? <!-- .element: class="fragment" -->
- O valor "dá a volta" (Circular) <!-- .element: class="fragment" -->

---

## Resumo da Aula
1. Escolha o tipo correto <!-- .element: class="fragment" -->
2. Prefira `{}` para inicializar <!-- .element: class="fragment" -->
3. Use `const` sempre que possível <!-- .element: class="fragment" -->

---

## Exercício Rápido
- Declare uma variável para sua altura e outra para seu peso. <!-- .element: class="fragment" -->
- Calcule algo simples e imprima. <!-- .element: class="fragment" -->

---

## Fim da Aula 02
- Próxima aula: Operadores e Expressões!