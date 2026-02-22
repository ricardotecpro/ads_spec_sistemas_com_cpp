# Aula 10 - Construtores e Destrutores 🏗️

---

## O Ciclo de Vida do Objeto
- **Nascimento**: Construtor <!-- .element: class="fragment" -->
- **Vida**: Uso de métodos/atributos <!-- .element: class="fragment" -->
- **Morte**: Destrutor <!-- .element: class="fragment" -->

---

## O Construtor
- Método especial chamado automaticamente na criação do objeto. <!-- .element: class="fragment" -->
- Mesmo nome da classe, sem tipo de retorno. <!-- .element: class="fragment" -->

---

## Construtor Padrão (Default)
```cpp
Classe() { ... }
```
- Criado pelo C++ se você não definir nenhum. <!-- .element: class="fragment" -->

---

## Construtor Parametrizado
```cpp
Produto(string n, float p) : nome(n), preco(p) {}
```
- Permite criar objetos já configurados. <!-- .element: class="fragment" -->

---

## Member Initializer List
- `: nome(n), preco(p)` <!-- .element: class="fragment" -->
- Mais eficiente que atribuir dentro das chaves `{}`. <!-- .element: class="fragment" -->

---

## Sobrecarga de Construtores
- Podemos ter vários construtores para diferentes formas de criar o objeto. <!-- .element: class="fragment" -->

---

## Delegating Constructors (C++11)
- Um construtor que chama outro da mesma classe para evitar repetição. <!-- .element: class="fragment" -->

---

## Construtor de Cópia (Copy Constructor)
- Chamado quando criamos um objeto a partir de outro (`A = B`). <!-- .element: class="fragment" -->
- Importante para classes com ponteiros! <!-- .element: class="fragment" -->

---

## Cópia Rasa vs Profunda (Shallow vs Deep)
- **Rasa**: Copia o endereço do ponteiro (Perigoso!). <!-- .element: class="fragment" -->
- **Profunda**: Aloca nova memória e copia o conteúdo (Seguro). <!-- .element: class="fragment" -->

---

## O Destrutor
- Chamado automaticamente quando o objeto sai de escopo ou é deletado. <!-- .element: class="fragment" -->
- Nome precedido por til (~): `~Classe()`. <!-- .element: class="fragment" -->

---

## Para que serve o Destrutor?
- Liberar memória alocada dinamicamente (`delete`). <!-- .element: class="fragment" -->
- Fechar conexões de banco de dados e arquivos. <!-- .element: class="fragment" -->

---

## Chamada Automática
```cpp
{
   Objeto obj; // Construtor
} // Saiu do bloco: Destrutor automático
```

---

## Destrutores Virtuais
- Essenciais em hierarquias de herança para evitar memory leaks. <!-- .element: class="fragment" -->

---

## Explicit Constructors
- Impede conversões de tipo automáticas indesejadas. <!-- .element: class="fragment" -->
- `explicit MeuTipo(int x);` <!-- .element: class="fragment" -->

---

## Deleted Functions (C++11)
- `Classe(const Classe&) = delete;` <!-- .element: class="fragment" -->
- Impede que um objeto seja copiado. <!-- .element: class="fragment" -->

---

## Defaulted Functions
- `Classe() = default;` <!-- .element: class="fragment" -->
- Pede para o compilador gerar a versão padrão. <!-- .element: class="fragment" -->

---

## RAII (Revisitado)
- Resource Acquisition Is Initialization. <!-- .element: class="fragment" -->
- A base da segurança de memória no C++ moderno. <!-- .element: class="fragment" -->

---

## Debugging: Ordem de Chamada
- Em herança, a base é construída primeiro. <!-- .element: class="fragment" -->
- O filho é destruído primeiro. <!-- .element: class="fragment" -->

---

## Estratégias de Gerenciamento
- No C++ Moderno, evite gerenciar memória manualmente nos construtores/destrutores. <!-- .element: class="fragment" -->
- Use Smart Pointers! <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Construtores preparam o objeto. <!-- .element: class="fragment" -->
- Destrutores limpam a bagunça. <!-- .element: class="fragment" -->
- Use a lista de inicialização sempre que possível. <!-- .element: class="fragment" -->

---

## Fim da Aula 10
- Próxima aula: Herança e Polimorfismo!