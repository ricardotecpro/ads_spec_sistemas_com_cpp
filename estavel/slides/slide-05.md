# Aula 05 - Funções 🧩

---

## O que é uma Função?
- Um bloco de código reutilizável que realiza uma tarefa específica. <!-- .element: class="fragment" -->
- Promove a modularização e evita repetição de código (DRY - Don't Repeat Yourself). <!-- .element: class="fragment" -->

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
- `int`, `float`, `string`, etc. <!-- .element: class="fragment" -->
- `void`: Quando a função não retorna nada. <!-- .element: class="fragment" -->

---

## Parâmetros (Argumentos)
- Entradas que a função recebe para trabalhar. <!-- .element: class="fragment" -->
- Podem ser opcionais ou múltiplos. <!-- .element: class="fragment" -->

---

## Declaração vs Definição
- **Declaração (Protótipo)**: Avisa ao compilador que a função existe. <!-- .element: class="fragment" -->
- **Definição**: Contém o código real da função. <!-- .element: class="fragment" -->

---

## Por que usar Protótipos?
- Permite chamar funções antes de sua implementação no arquivo. <!-- .element: class="fragment" -->
- Geralmente colocados no topo do arquivo ou em arquivos `.h`. <!-- .element: class="fragment" -->

---

## Passagem por Valor
- Uma cópia do dado é enviada. <!-- .element: class="fragment" -->
- Alterações dentro da função **não afetam** a variável original. <!-- .element: class="fragment" -->

---

## Passagem por Referência
- O endereço (referência) é enviado. <!-- .element: class="fragment" -->
- Alterações **afetam diretamente** a variável original. <!-- .element: class="fragment" -->
- Use o símbolo `&`. <!-- .element: class="fragment" -->

---

## Quando usar Referência?
1. Para alterar a variável original. <!-- .element: class="fragment" -->
2. Por performance (evita cópia de objetos grandes como strings ou vectors). <!-- .element: class="fragment" -->

---

## Funções Const
- `void imprimir(const string &s)` <!-- .element: class="fragment" -->
- Protege o dado de ser alterado acidentalmente. <!-- .element: class="fragment" -->

---

## Sobrecarga de Funções (Overloading)
- Várias funções com o mesmo nome, mas parâmetros diferentes. <!-- .element: class="fragment" -->
```cpp
void desenhar(int x);
void desenhar(int x, int y);
```

---

## Funções Inline
- Sugestão ao compilador para substituir a chamada da função pelo seu código. <!-- .element: class="fragment" -->
- Aumenta performance em funções minúsculas. <!-- .element: class="fragment" -->

---

## Valores Padrão (Default Arguments)
```cpp
void alerta(string msg = "Erro desconhecido");
```
- Permite chamar a função sem passar o argumento. <!-- .element: class="fragment" -->

---

## Escopo de Variáveis
- **Locais**: Existem apenas dentro da função. <!-- .element: class="fragment" -->
- **Globais**: Acessíveis por todo o programa (evite!). <!-- .element: class="fragment" -->

---

## Variáveis Estáticas (static)
- Mantêm seu valor entre as chamadas da função. <!-- .element: class="fragment" -->

---

## Recursividade
- Uma função que chama a si mesma. <!-- .element: class="fragment" -->
- Deve ter um **caso base** para não virar um loop infinito. <!-- .element: class="fragment" -->

---

## Stack Overflow (Pilha de Amostragem)
- Erro que acontece quando há excesso de chamadas recursivas. <!-- .element: class="fragment" -->

---

## Funções Lambda (C++11)
- Funções anônimas escritas "na hora". <!-- .element: class="fragment" -->
```cpp
auto soma = [](int a, int b) { return a + b; };
```

---

## Bibliotecas de Funções
- C++ possui milhares de funções prontas em bibliotecas como `<cmath>`, `<string>`, `<algorithm>`. <!-- .element: class="fragment" -->

---

## Organização Profissional
- Arquivo `.h`: Declarações. <!-- .element: class="fragment" -->
- Arquivo `.cpp`: Implementações. <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Divida problemas grandes em funções pequenas. <!-- .element: class="fragment" -->
- Use referências para performance. <!-- .element: class="fragment" -->
- Evite variáveis globais. <!-- .element: class="fragment" -->

---

## Fim da Aula 05
- Próxima aula: Arrays e Strings!