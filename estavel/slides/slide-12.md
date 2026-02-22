# Aula 12 - Sobrecarga de Operadores ⚖️

---

## Por que sobrecarregar?
- Tornar o uso de objetos tão intuitivo quanto tipos primitivos. <!-- .element: class="fragment" -->
- Ex: `vetor1 + vetor2` em vez de `vetor1.somar(vetor2)`. <!-- .element: class="fragment" -->

---

## Operadores que PODEM ser sobrecarregados
- Praticamente todos: `+ - * / % == != < > << >> [] () ...` <!-- .element: class="fragment" -->

---

## Operadores que NÃO PODEM
- `.` (ponto) <!-- .element: class="fragment" -->
- `::` (escopo) <!-- .element: class="fragment" -->
- `?:` (ternário) <!-- .element: class="fragment" -->
- `sizeof` <!-- .element: class="fragment" -->
- `.*` (ponto asterisco) <!-- .element: class="fragment" -->

---

## Sintaxe da Sobrecarga
```cpp
TipoRetorno operator#(parametros) { ... }
```

---

## Exemplo: Operador +
```cpp
Ponto operator+(const Ponto& outro) {
    return Ponto(x + outro.x, y + outro.y);
}
```

---

## Sobrecarga via Método de Classe
- O primeiro operando é o próprio objeto (`this`). <!-- .element: class="fragment" -->

---

## Sobrecarga via Função Global (Friend)
- Usada quando o primeiro operando não é da nossa classe (ex: `cout`). <!-- .element: class="fragment" -->

---

## Friend Functions (Amigas)
- Funções fora da classe que podem acessar membros privados. <!-- .element: class="fragment" -->
- Use com moderação! <!-- .element: class="fragment" -->

---

## Sobrecarga de Fluxo (<< e >>)
- Permite usar `cout << obj;` e `cin >> obj;`. <!-- .element: class="fragment" -->
- **Deve** ser feita via função global. <!-- .element: class="fragment" -->

---

## Exemplo: operator<<
```cpp
ostream& operator<<(ostream& os, const Ponto& p) {
    os << "(" << p.x << ", " << p.y << ")";
    return os;
}
```

---

## Operador de Atribuição (=)
- Fundamental para classes que gerenciam memória dinâmica. <!-- .element: class="fragment" -->
- Deve verificar auto-atribuição (`if (this == &outro)`). <!-- .element: class="fragment" -->

---

## Operadores de Comparação (== e !=)
- Facilitam o uso em buscas e algoritmos da STL. <!-- .element: class="fragment" -->

---

## Operador Subscrito ([ ])
- Permite que a classe se comporte como um array. <!-- .element: class="fragment" -->
- Ex: Uma classe `MinhaLista`. <!-- .element: class="fragment" -->

---

## Operador de Chamada de Função ( ( ) )
- Atribui comportamento de função ao objeto (Functors). <!-- .element: class="fragment" -->

---

## Operadores Unários (++, --)
- Distinção entre prefixo `++obj` e sufixo `obj++`. <!-- .element: class="fragment" -->

---

## Prefix vs Postfix
- No sufixo, adicionamos um parâmetro fantasma: `operator++(int)`. <!-- .element: class="fragment" -->

---

## Regras de Ouro
1. Não mude a natureza do operador (Não use `+` para subtrair). <!-- .element: class="fragment" -->
2. Mantenha a semântica intuitiva. <!-- .element: class="fragment" -->
3. Sobrecarga não deve ser mágica negra, mas conveniência. <!-- .element: class="fragment" -->

---

## Lógica de Operadores Lógicos
- Cuidado ao sobrecarregar `&&` e `||`, pois perde-se o comportamento de "Short-circuit". <!-- .element: class="fragment" -->

---

## Operadores de Conversão
- Permitem que um objeto seja convertido em outro tipo automaticamente. <!-- .element: class="fragment" -->
- `operator double() { return valor; }` <!-- .element: class="fragment" -->

---

## Conversões Implícitas vs explícitas
- Prefira `explicit operator bool()` para evitar erros bobos. <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Sobrecarga é açúcar sintático poderoso. <!-- .element: class="fragment" -->
- Use prioritariamente para classes matemáticas ou containers. <!-- .element: class="fragment" -->

---

## Fim da Aula 12
- Próxima aula: STL!