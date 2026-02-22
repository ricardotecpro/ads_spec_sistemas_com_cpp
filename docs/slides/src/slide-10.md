# Aula 10 - Construtores e Destrutores 🏗️

---

## O Ciclo de Vida do Objeto
- **Nascimento**: Construtor { .fragment }
- **Vida**: Uso de métodos/atributos { .fragment }
- **Morte**: Destrutor { .fragment }

---

## O Construtor
- Método especial chamado automaticamente na criação do objeto. { .fragment }
- Mesmo nome da classe, sem tipo de retorno. { .fragment }

---

## Construtor Padrão (Default)
```cpp
Classe() { ... }
```
- Criado pelo C++ se você não definir nenhum. { .fragment }

---

## Construtor Parametrizado
```cpp
Produto(string n, float p) : nome(n), preco(p) {}
```
- Permite criar objetos já configurados. { .fragment }

---

## Member Initializer List
- `: nome(n), preco(p)` { .fragment }
- Mais eficiente que atribuir dentro das chaves `{}`. { .fragment }

---

## Sobrecarga de Construtores
- Podemos ter vários construtores para diferentes formas de criar o objeto. { .fragment }

---

## Delegating Constructors (C++11)
- Um construtor que chama outro da mesma classe para evitar repetição. { .fragment }

---

## Construtor de Cópia (Copy Constructor)
- Chamado quando criamos um objeto a partir de outro (`A = B`). { .fragment }
- Importante para classes com ponteiros! { .fragment }

---

## Cópia Rasa vs Profunda (Shallow vs Deep)
- **Rasa**: Copia o endereço do ponteiro (Perigoso!). { .fragment }
- **Profunda**: Aloca nova memória e copia o conteúdo (Seguro). { .fragment }

---

## O Destrutor
- Chamado automaticamente quando o objeto sai de escopo ou é deletado. { .fragment }
- Nome precedido por til (~): `~Classe()`. { .fragment }

---

## Para que serve o Destrutor?
- Liberar memória alocada dinamicamente (`delete`). { .fragment }
- Fechar conexões de banco de dados e arquivos. { .fragment }

---

## Chamada Automática
```cpp
{
   Objeto obj; // Construtor
} // Saiu do bloco: Destrutor automático
```

---

## Destrutores Virtuais
- Essenciais em hierarquias de herança para evitar memory leaks. { .fragment }

---

## Explicit Constructors
- Impede conversões de tipo automáticas indesejadas. { .fragment }
- `explicit MeuTipo(int x);` { .fragment }

---

## Deleted Functions (C++11)
- `Classe(const Classe&) = delete;` { .fragment }
- Impede que um objeto seja copiado. { .fragment }

---

## Defaulted Functions
- `Classe() = default;` { .fragment }
- Pede para o compilador gerar a versão padrão. { .fragment }

---

## RAII (Revisitado)
- Resource Acquisition Is Initialization. { .fragment }
- A base da segurança de memória no C++ moderno. { .fragment }

---

## Debugging: Ordem de Chamada
- Em herança, a base é construída primeiro. { .fragment }
- O filho é destruído primeiro. { .fragment }

---

## Estratégias de Gerenciamento
- No C++ Moderno, evite gerenciar memória manualmente nos construtores/destrutores. { .fragment }
- Use Smart Pointers! { .fragment }

---

## Resumo da Aula
- Construtores preparam o objeto. { .fragment }
- Destrutores limpam a bagunça. { .fragment }
- Use a lista de inicialização sempre que possível. { .fragment }

---

## Fim da Aula 10
- Próxima aula: Herança e Polimorfismo!