# Aula 09 - Conceitos de POO 🏢

---

## O que é POO?
- Programação Orientada a Objetos. { .fragment }
- Paradigma que aproxima o código de conceitos do mundo real. { .fragment }

---

## Os 4 Pilares da POO
1. Encapsulamento { .fragment }
2. Abstração { .fragment }
3. Herança { .fragment }
4. Polimorfismo { .fragment }

---

## Classe vs Objeto
- **Classe**: A planta do arquiteto (Molde). { .fragment }
- **Objeto**: A casa construída (Instância). { .fragment }

---

## Definindo uma Classe
```cpp
class ContaBancaria {
public:
    string titular;
    double saldo;

    void depositar(double v) { saldo += v; }
};
```

---

## Modificadores de Acesso
- `public`: Acesso universal. { .fragment }
- `private`: Acesso restrito à própria classe. { .fragment }
- `protected`: Própria classe e herdeiros. { .fragment }

---

## O Poder do Encapsulamento
- Não deixe que qualquer um mude seu saldo diretamente! { .fragment }
- Torne os atributos **privados** e use métodos para alterá-los. { .fragment }

---

## Métodos Getters e Setters
```cpp
void setSaldo(double v) { if (v > 0) saldo = v; }
double getSaldo() { return saldo; }
```

---

## Abstração
- Focar no essencial e ignorar detalhes irrelevantes. { .fragment }
- Uma classe "Carro" no sistema de mecânica foca em peças; no sistema de trânsito foca em placa/velocidade. { .fragment }

---

## Membros Estáticos (static)
- Atributos ou métodos que pertencem à **classe**, não ao objeto. { .fragment }
- Compartilhados por todas as instâncias. { .fragment }

---

## Ponteiro implicitando: the `this` pointer
- Todo objeto possui um ponteiro `this` que aponta para si mesmo. { .fragment }
- Útil para distinguir parâmetros de atributos com mesmo nome. { .fragment }

---

## Diagrama de Classe (UML)
```mermaid
classDiagram
    class Conta {
        -double saldo
        +string titular
        +depositar(valor)
        +sacar(valor)
    }
```

---

## Design de Classes
- Pense nas responsabilidades: "O que esta classe **sabe** e o que ela **faz**?" { .fragment }

---

## Interação entre Objetos
- Objetos podem ser passados como parâmetros para outros objetos. { .fragment }
- Ex: Uma classe `Banco` que contém uma lista de objetos `Conta`. { .fragment }

---

## Getters e Setters automáticos?
- Diferente de outras linguagens, no C++ você deve escrevê-los ou usar snippets da IDE. { .fragment }

---

## Composição (has-a)
- Uma classe que contém outra como atributo. { .fragment }
- Ex: `Carro` tem um objeto `Motor`. { .fragment }

---

## Delegação
- Quando um objeto pede para outro realizar uma tarefa. { .fragment }

---

## Boas Práticas: Interface vs Implementação
- Mantenha a interface (pública) o mais simples possível. { .fragment }
- Esconda a complexidade (privada). { .fragment }

---

## Por que C++ é bom para POO?
- Controle total sobre o ciclo de vida do objeto. { .fragment }
- Sem overhead obrigatório de Garbage Collection. { .fragment }

---

## Atributos Constantes em Classes
- Atributos que nunca mudam após criados (ex: ID secreto). { .fragment }

---

## Métodos Constantes
- `void exibir() const;` { .fragment }
- Garante que o método não alterará nenhum atributo do objeto. { .fragment }

---

## Resumo da Aula
- POO organiza sistemas complexos. { .fragment }
- Use classes para criar seus próprios tipos de dados inteligentes. { .fragment }
- Encapsule para proteger sua lógica. { .fragment }

---

## Fim da Aula 09
- Próxima aula: Construtores e Destrutores!