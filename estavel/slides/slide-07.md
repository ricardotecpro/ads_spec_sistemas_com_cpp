# Aula 07 - Ponteiros e Referências 👆

---

## O que é um Ponteiro?
- Uma variável que armazena um **endereço de memória**. <!-- .element: class="fragment" -->
- "Aponta" para onde um dado está guardado na RAM. <!-- .element: class="fragment" -->

---

## Memória RAM (Abstração)
| Endereço | Descrição | Valor |
|----------|-----------|-------|
| 0x100 | Variável 'x'| 42 |
| 0x104 | Ponteiro 'p'| 0x100 |

---

## Declaração de Ponteiros
```cpp
int x = 10;
int* p = &x; // p aponta para o endereço de x
```
- `int*`: Tipo ponteiro para inteiro. <!-- .element: class="fragment" -->
- `&`: Operador de endereço (Address-of). <!-- .element: class="fragment" -->

---

## Desreferenciamento (`*`)
- Acessar o valor que está no endereço apontado. <!-- .element: class="fragment" -->
```cpp
cout << *p;  // Imprime 10
*p = 20;     // Altera x para 20!
```

---

## O Perigo de Ponteiros Não Inicializados
- Ponteiros "selvagens" (wild pointers) apontam para lugares aleatórios. <!-- .element: class="fragment" -->
- Podem causar erros de segmentação (crash). <!-- .element: class="fragment" -->

---

## nullptr (C++11)
- Sempre inicialize ponteiros vazios com `nullptr`. <!-- .element: class="fragment" -->
- Indica claramente que o ponteiro não aponta para nada válido. <!-- .element: class="fragment" -->

---

## Aritmética de Ponteiros
- `p++`: Pula para o próximo endereço do tipo. <!-- .element: class="fragment" -->
- Se `p` é `int*` (4 bytes), `p+1` pula 4 bytes. <!-- .element: class="fragment" -->

---

## Arrays e Ponteiros
- O nome de um array é, na prática, um ponteiro para o primeiro elemento. <!-- .element: class="fragment" -->
- `*(arr + 1)` é o mesmo que `arr[1]`. <!-- .element: class="fragment" -->

---

## O que é uma Referência?
- Um **apelido (alias)** para uma variável existente. <!-- .element: class="fragment" -->
- Diferente do ponteiro, não pode ser nula e nem mudar de alvo. <!-- .element: class="fragment" -->

---

## Declaração de Referências
```cpp
int x = 10;
int &ref = x; // ref é outro nome para x
```

---

## Quando usar Referências?
- Passagem de parâmetros em funções (Performance). <!-- .element: class="fragment" -->
- Retorno de objetos grandes. <!-- .element: class="fragment" -->
- Manter o código mais "limpo" que com ponteiros. <!-- .element: class="fragment" -->

---

## Stack vs Heap
- **Stack (Pilha)**: Memória automática, rápida, pequena. <!-- .element: class="fragment" -->
- **Heap (Monte)**: Memória dinâmica, manual, grande. <!-- .element: class="fragment" -->

---

## Alocação Dinâmica (new)
```cpp
int* p = new int; // Aloca no Heap
*p = 100;
```

---

## Liberação de Memória (delete)
- Todo `new` deve ter um `delete`. <!-- .element: class="fragment" -->
```cpp
delete p; // Libera o espaço no Heap
p = nullptr; // Boa prática
```

---

## Vazamento de Memória (Memory Leak)
- Quando perdemos o endereço de uma memória alocada sem dar `delete`. <!-- .element: class="fragment" -->
- O programa consome RAM até travar o sistema. <!-- .element: class="fragment" -->

---

## Arrays Dinâmicos
```cpp
int* arr = new int[tamanho];
delete[] arr; // Use colchetes para arrays!
```

---

## Ponteiro de Ponteiro (**)
- Um ponteiro que aponta para outro ponteiro. <!-- .element: class="fragment" -->
- Usado em matrizes dinâmicas complexas. <!-- .element: class="fragment" -->

---

## Operador -> (Seta)
- Atalho para acessar membros através de um ponteiro. <!-- .element: class="fragment" -->
- `ptr->nome` em vez de `(*ptr).nome`. <!-- .element: class="fragment" -->

---

## Passagem de Ponteiro para Funções
- Permite alterar o valor original (como referência). <!-- .element: class="fragment" -->
- Permite passar "nada" (`nullptr`). <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Ponteiros oferecem poder total sobre a máquina. <!-- .element: class="fragment" -->
- Com grandes poderes vêm grandes responsabilidades (Gestão de RAM). <!-- .element: class="fragment" -->
- Use referências sempre que puder; use ponteiros só quando precisar. <!-- .element: class="fragment" -->

---

## Fim da Aula 07
- Próxima aula: Estruturas e Arquivos!