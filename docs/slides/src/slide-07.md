# Aula 07 - Ponteiros e Referências 👆

---

## O que é um Ponteiro?
- Uma variável que armazena um **endereço de memória**. { .fragment }
- "Aponta" para onde um dado está guardado na RAM. { .fragment }

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
- `int*`: Tipo ponteiro para inteiro. { .fragment }
- `&`: Operador de endereço (Address-of). { .fragment }

---

## Desreferenciamento (`*`)
- Acessar o valor que está no endereço apontado. { .fragment }
```cpp
cout << *p;  // Imprime 10
*p = 20;     // Altera x para 20!
```

---

## O Perigo de Ponteiros Não Inicializados
- Ponteiros "selvagens" (wild pointers) apontam para lugares aleatórios. { .fragment }
- Podem causar erros de segmentação (crash). { .fragment }

---

## nullptr (C++11)
- Sempre inicialize ponteiros vazios com `nullptr`. { .fragment }
- Indica claramente que o ponteiro não aponta para nada válido. { .fragment }

---

## Aritmética de Ponteiros
- `p++`: Pula para o próximo endereço do tipo. { .fragment }
- Se `p` é `int*` (4 bytes), `p+1` pula 4 bytes. { .fragment }

---

## Arrays e Ponteiros
- O nome de um array é, na prática, um ponteiro para o primeiro elemento. { .fragment }
- `*(arr + 1)` é o mesmo que `arr[1]`. { .fragment }

---

## O que é uma Referência?
- Um **apelido (alias)** para uma variável existente. { .fragment }
- Diferente do ponteiro, não pode ser nula e nem mudar de alvo. { .fragment }

---

## Declaração de Referências
```cpp
int x = 10;
int &ref = x; // ref é outro nome para x
```

---

## Quando usar Referências?
- Passagem de parâmetros em funções (Performance). { .fragment }
- Retorno de objetos grandes. { .fragment }
- Manter o código mais "limpo" que com ponteiros. { .fragment }

---

## Stack vs Heap
- **Stack (Pilha)**: Memória automática, rápida, pequena. { .fragment }
- **Heap (Monte)**: Memória dinâmica, manual, grande. { .fragment }

---

## Alocação Dinâmica (new)
```cpp
int* p = new int; // Aloca no Heap
*p = 100;
```

---

## Liberação de Memória (delete)
- Todo `new` deve ter um `delete`. { .fragment }
```cpp
delete p; // Libera o espaço no Heap
p = nullptr; // Boa prática
```

---

## Vazamento de Memória (Memory Leak)
- Quando perdemos o endereço de uma memória alocada sem dar `delete`. { .fragment }
- O programa consome RAM até travar o sistema. { .fragment }

---

## Arrays Dinâmicos
```cpp
int* arr = new int[tamanho];
delete[] arr; // Use colchetes para arrays!
```

---

## Ponteiro de Ponteiro (**)
- Um ponteiro que aponta para outro ponteiro. { .fragment }
- Usado em matrizes dinâmicas complexas. { .fragment }

---

## Operador -> (Seta)
- Atalho para acessar membros através de um ponteiro. { .fragment }
- `ptr->nome` em vez de `(*ptr).nome`. { .fragment }

---

## Passagem de Ponteiro para Funções
- Permite alterar o valor original (como referência). { .fragment }
- Permite passar "nada" (`nullptr`). { .fragment }

---

## Resumo da Aula
- Ponteiros oferecem poder total sobre a máquina. { .fragment }
- Com grandes poderes vêm grandes responsabilidades (Gestão de RAM). { .fragment }
- Use referências sempre que puder; use ponteiros só quando precisar. { .fragment }

---

## Fim da Aula 07
- Próxima aula: Estruturas e Arquivos!