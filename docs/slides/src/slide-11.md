# Aula 11 - Herança e Polimorfismo 🌳

---

## O Propósito da Herança
- Criar novas classes baseadas em classes existentes. { .fragment }
- "É um" (Is-a relationship): Cachorro **é um** Animal. { .fragment }

---

## Sintaxe da Herança
```cpp
class Animal { ... };
class Cachorro : public Animal { ... };
```

---

## Tipos de Herança
- `public`: Mantém os níveis de acesso da base. { .fragment }
- `private`: Torna tudo privado na filha. { .fragment }
- `protected`: Tudo vira protegido na filha. { .fragment }

---

## Revisitando: protected
- Membros visíveis para a classe e suas descendentes. { .fragment }
- Escondidos do mundo externo. { .fragment }

---

## Sobrescrita de Métodos (Overriding)
- Redefinir o comportamento de um método na classe filha. { .fragment }

---

## O Problema do Type Slicing
- Quando tratamos um objeto filho como pai e perdemos as partes do filho. { .fragment }
- Resolvido com **Ponteiros** e **Referências**! { .fragment }

---

## O que é Polimorfismo?
- Permitir que diferentes objetos reajam à mesma mensagem de formas diferentes. { .fragment }

---

## Funções Virtuais (virtual)
- Permitem que a escolha da função ocorra em tempo de execução (Dynamic Binding). { .fragment }
```cpp
virtual void emitirSom();
```

---

## Importância do virtual
- Sem `virtual`, se você usar um ponteiro `Animal*` apontando para `Cachorro`, ele chamará o `emitirSom` do Animal! { .fragment }

---

## override (C++11)
```cpp
void emitirSom() override;
```
- Garante que você está realmente sobrescrevendo algo. { .fragment }

---

## final (C++11)
- Impede que uma classe ou método seja herdado/sobrescrito. { .fragment }

---

## Funções Virtuais Puras
- `virtual void mover() = 0;` { .fragment }
- Indica que a classe **deve** implementar este método. { .fragment }

---

## Classes Abstratas
- Classes que possuem pelo menos uma função virtual pura. { .fragment }
- Não podem ser instanciadas (`new Animal()` daria erro). { .fragment }

---

## Interfaces no C++
- Criadas usando classes puramente abstratas (apenas métodos virtuais puros). { .fragment }

---

## Ordem de Destruição
- **Sempre** torne o destrutor da classe base `virtual`. { .fragment }
- Caso contrário, a parte da classe filha pode nunca ser liberada! { .fragment }

---

## Herança Múltipla
- C++ permite herdar de várias classes base simultaneamente. { .fragment }
```cpp
class Cyborg : public Humano, public Robot { ... };
```

---

## O Problema do Diamante
- Quando duas classes herdam do mesmo pai e uma quarta herda de ambas. { .fragment }
- Resolvido com **Herança Virtual**. { .fragment }

---

## Upcasting e Downcasting
- **Upcast**: Da filha para a base (Seguro e automático). { .fragment }
- **Downcast**: Da base para a filha (Manual e arriscado - use `dynamic_cast`). { .fragment }

---

## dynamic_cast
- Checa em tempo de execução se a conversão é válida. { .fragment }
- Retorna `nullptr` se falhar. { .fragment }

---

## Resumo da Aula
- Herança para reuso. { .fragment }
- Polimorfismo para flexibilidade. { .fragment }
- `virtual` e `override` são seus melhores amigos. { .fragment }

---

## Fim da Aula 11
- Próxima aula: Sobrecarga de Operadores!