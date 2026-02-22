# Mini-Projeto 12: Classe Vetor Matemático 📐

---

### 📝 Descrição
Crie uma classe `Vetor2D` que representa um vetor no plano cartesiano e sobrecarregue operadores para facilitar cálculos.

### 🎯 Requisitos
- Atributos `x` e `y`.
- Sobrecarregar o operador `+` para somar dois vetores (`(x1+x2, y1+y2)`).
- Sobrecarregar o operador `<<` para imprimir o vetor como `(x, y)`.
- Sobrecarregar o operador `==` para comparar se dois vetores são iguais.

### 💡 Dicas
- Lembre-se de retornar uma referência ao fluxo (`ostream&`) na sobrecarga do `<<`.
- A função de soma deve retornar um novo objeto `Vetor2D`.

---

### 🚀 Desafio Extra
Sobrecarregue o operador `*` para realizar o produto escalar entre dois vetores (retornando um `double`).