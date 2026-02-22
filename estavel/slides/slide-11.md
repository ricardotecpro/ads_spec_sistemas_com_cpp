# Aula 11 - Herança e Polimorfismo 🌳

---

## O Propósito da Herança
- Criar novas classes baseadas em classes existentes. <!-- .element: class="fragment" -->
- "É um" (Is-a relationship): Cachorro **é um** Animal. <!-- .element: class="fragment" -->

---

## Sintaxe da Herança
```cpp
class Animal { ... };
class Cachorro : public Animal { ... };
```

---

## Tipos de Herança
- `public`: Mantém os níveis de acesso da base. <!-- .element: class="fragment" -->
- `private`: Torna tudo privado na filha. <!-- .element: class="fragment" -->
- `protected`: Tudo vira protegido na filha. <!-- .element: class="fragment" -->

---

## Revisitando: protected
- Membros visíveis para a classe e suas descendentes. <!-- .element: class="fragment" -->
- Escondidos do mundo externo. <!-- .element: class="fragment" -->

---

## Sobrescrita de Métodos (Overriding)
- Redefinir o comportamento de um método na classe filha. <!-- .element: class="fragment" -->

---

## O Problema do Type Slicing
- Quando tratamos um objeto filho como pai e perdemos as partes do filho. <!-- .element: class="fragment" -->
- Resolvido com **Ponteiros** e **Referências**! <!-- .element: class="fragment" -->

---

## O que é Polimorfismo?
- Permitir que diferentes objetos reajam à mesma mensagem de formas diferentes. <!-- .element: class="fragment" -->

---

## Funções Virtuais (virtual)
- Permitem que a escolha da função ocorra em tempo de execução (Dynamic Binding). <!-- .element: class="fragment" -->
```cpp
virtual void emitirSom();
```

---

## Importância do virtual
- Sem `virtual`, se você usar um ponteiro `Animal*` apontando para `Cachorro`, ele chamará o `emitirSom` do Animal! <!-- .element: class="fragment" -->

---

## override (C++11)
```cpp
void emitirSom() override;
```
- Garante que você está realmente sobrescrevendo algo. <!-- .element: class="fragment" -->

---

## final (C++11)
- Impede que uma classe ou método seja herdado/sobrescrito. <!-- .element: class="fragment" -->

---

## Funções Virtuais Puras
- `virtual void mover() = 0;` <!-- .element: class="fragment" -->
- Indica que a classe **deve** implementar este método. <!-- .element: class="fragment" -->

---

## Classes Abstratas
- Classes que possuem pelo menos uma função virtual pura. <!-- .element: class="fragment" -->
- Não podem ser instanciadas (`new Animal()` daria erro). <!-- .element: class="fragment" -->

---

## Interfaces no C++
- Criadas usando classes puramente abstratas (apenas métodos virtuais puros). <!-- .element: class="fragment" -->

---

## Ordem de Destruição
- **Sempre** torne o destrutor da classe base `virtual`. <!-- .element: class="fragment" -->
- Caso contrário, a parte da classe filha pode nunca ser liberada! <!-- .element: class="fragment" -->

---

## Herança Múltipla
- C++ permite herdar de várias classes base simultaneamente. <!-- .element: class="fragment" -->
```cpp
class Cyborg : public Humano, public Robot { ... };
```

---

## O Problema do Diamante
- Quando duas classes herdam do mesmo pai e uma quarta herda de ambas. <!-- .element: class="fragment" -->
- Resolvido com **Herança Virtual**. <!-- .element: class="fragment" -->

---

## Upcasting e Downcasting
- **Upcast**: Da filha para a base (Seguro e automático). <!-- .element: class="fragment" -->
- **Downcast**: Da base para a filha (Manual e arriscado - use `dynamic_cast`). <!-- .element: class="fragment" -->

---

## dynamic_cast
- Checa em tempo de execução se a conversão é válida. <!-- .element: class="fragment" -->
- Retorna `nullptr` se falhar. <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Herança para reuso. <!-- .element: class="fragment" -->
- Polimorfismo para flexibilidade. <!-- .element: class="fragment" -->
- `virtual` e `override` são seus melhores amigos. <!-- .element: class="fragment" -->

---

## Fim da Aula 11
- Próxima aula: Sobrecarga de Operadores!