# Aula 05 - Funções 🧩

---

## O que é uma Função?
- Um bloco de código reutilizável que realiza uma tarefa específica. { .fragment }
- Promove a modularização e evita repetição de código (DRY - Don't Repeat Yourself). { .fragment }

---

## Estrutura Básica
```cpp
tipo_retorno nome_funcao(parametros) {
    // Corpo da função
    return valor;
}
```

---

## Tipo de Retorno
- `int`, `float`, `string`, etc. { .fragment }
- `void`: Quando a função não retorna nada. { .fragment }

---

## Parâmetros (Argumentos)
- Entradas que a função recebe para trabalhar. { .fragment }
- Podem ser opcionais ou múltiplos. { .fragment }

---

## Declaração vs Definição
- **Declaração (Protótipo)**: Avisa ao compilador que a função existe. { .fragment }
- **Definição**: Contém o código real da função. { .fragment }

---

## Por que usar Protótipos?
- Permite chamar funções antes de sua implementação no arquivo. { .fragment }
- Geralmente colocados no topo do arquivo ou em arquivos `.h`. { .fragment }

---

## Passagem por Valor
- Uma cópia do dado é enviada. { .fragment }
- Alterações dentro da função **não afetam** a variável original. { .fragment }

---

## Passagem por Referência
- O endereço (referência) é enviado. { .fragment }
- Alterações **afetam diretamente** a variável original. { .fragment }
- Use o símbolo `&`. { .fragment }

---

## Quando usar Referência?
1. Para alterar a variável original. { .fragment }
2. Por performance (evita cópia de objetos grandes como strings ou vectors). { .fragment }

---

## Funções Const
- `void imprimir(const string &s)` { .fragment }
- Protege o dado de ser alterado acidentalmente. { .fragment }

---

## Sobrecarga de Funções (Overloading)
- Várias funções com o mesmo nome, mas parâmetros diferentes. { .fragment }
```cpp
void desenhar(int x);
void desenhar(int x, int y);
```

---

## Funções Inline
- Sugestão ao compilador para substituir a chamada da função pelo seu código. { .fragment }
- Aumenta performance em funções minúsculas. { .fragment }

---

## Valores Padrão (Default Arguments)
```cpp
void alerta(string msg = "Erro desconhecido");
```
- Permite chamar a função sem passar o argumento. { .fragment }

---

## Escopo de Variáveis
- **Locais**: Existem apenas dentro da função. { .fragment }
- **Globais**: Acessíveis por todo o programa (evite!). { .fragment }

---

## Variáveis Estáticas (static)
- Mantêm seu valor entre as chamadas da função. { .fragment }

---

## Recursividade
- Uma função que chama a si mesma. { .fragment }
- Deve ter um **caso base** para não virar um loop infinito. { .fragment }

---

## Stack Overflow (Pilha de Amostragem)
- Erro que acontece quando há excesso de chamadas recursivas. { .fragment }

---

## Funções Lambda (C++11)
- Funções anônimas escritas "na hora". { .fragment }
```cpp
auto soma = [](int a, int b) { return a + b; };
```

---

## Bibliotecas de Funções
- C++ possui milhares de funções prontas em bibliotecas como `<cmath>`, `<string>`, `<algorithm>`. { .fragment }

---

## Organização Profissional
- Arquivo `.h`: Declarações. { .fragment }
- Arquivo `.cpp`: Implementações. { .fragment }

---

## Resumo da Aula
- Divida problemas grandes em funções pequenas. { .fragment }
- Use referências para performance. { .fragment }
- Evite variáveis globais. { .fragment }

---

## Fim da Aula 05
- Próxima aula: Arrays e Strings!