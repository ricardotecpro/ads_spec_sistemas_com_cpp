# Aula 12 - Sobrecarga de Operadores ⚖️

---

## Por que sobrecarregar?
- Tornar o uso de objetos tão intuitivo quanto tipos primitivos. { .fragment }
- Ex: `vetor1 + vetor2` em vez de `vetor1.somar(vetor2)`. { .fragment }

---

## Operadores que PODEM ser sobrecarregados
- Praticamente todos: `+ - * / % == != < > << >> [] () ...` { .fragment }

---

## Operadores que NÃO PODEM
- `.` (ponto) { .fragment }
- `::` (escopo) { .fragment }
- `?:` (ternário) { .fragment }
- `sizeof` { .fragment }
- `.*` (ponto asterisco) { .fragment }

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
- O primeiro operando é o próprio objeto (`this`). { .fragment }

---

## Sobrecarga via Função Global (Friend)
- Usada quando o primeiro operando não é da nossa classe (ex: `cout`). { .fragment }

---

## Friend Functions (Amigas)
- Funções fora da classe que podem acessar membros privados. { .fragment }
- Use com moderação! { .fragment }

---

## Sobrecarga de Fluxo (<< e >>)
- Permite usar `cout << obj;` e `cin >> obj;`. { .fragment }
- **Deve** ser feita via função global. { .fragment }

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
- Fundamental para classes que gerenciam memória dinâmica. { .fragment }
- Deve verificar auto-atribuição (`if (this == &outro)`). { .fragment }

---

## Operadores de Comparação (== e !=)
- Facilitam o uso em buscas e algoritmos da STL. { .fragment }

---

## Operador Subscrito ([ ])
- Permite que a classe se comporte como um array. { .fragment }
- Ex: Uma classe `MinhaLista`. { .fragment }

---

## Operador de Chamada de Função ( ( ) )
- Atribui comportamento de função ao objeto (Functors). { .fragment }

---

## Operadores Unários (++, --)
- Distinção entre prefixo `++obj` e sufixo `obj++`. { .fragment }

---

## Prefix vs Postfix
- No sufixo, adicionamos um parâmetro fantasma: `operator++(int)`. { .fragment }

---

## Regras de Ouro
1. Não mude a natureza do operador (Não use `+` para subtrair). { .fragment }
2. Mantenha a semântica intuitiva. { .fragment }
3. Sobrecarga não deve ser mágica negra, mas conveniência. { .fragment }

---

## Lógica de Operadores Lógicos
- Cuidado ao sobrecarregar `&&` e `||`, pois perde-se o comportamento de "Short-circuit". { .fragment }

---

## Operadores de Conversão
- Permitem que um objeto seja convertido em outro tipo automaticamente. { .fragment }
- `operator double() { return valor; }` { .fragment }

---

## Conversões Implícitas vs explícitas
- Prefira `explicit operator bool()` para evitar erros bobos. { .fragment }

---

## Resumo da Aula
- Sobrecarga é açúcar sintático poderoso. { .fragment }
- Use prioritariamente para classes matemáticas ou containers. { .fragment }

---

## Fim da Aula 12
- Próxima aula: STL!