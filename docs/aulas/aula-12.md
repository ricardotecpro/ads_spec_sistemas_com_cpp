# Aula 12 - Sobrecarga de Operadores ⚖️

Nesta aula, aprenderemos como ensinar ao C++ como lidar com operadores nativos (`+`, `-`, `*`, `<<`) em nossas próprias classes.

---

## ⚖️ O que é Sobrecarga de Operador?

É a capacidade de redefinir o comportamento de operadores para tipos definidos pelo usuário. Isso torna o código muito mais intuitivo e legível.

Sem sobrecarga: `res = c1.somar(c2);`
Com sobrecarga: `res = c1 + c2;`

---

## ➕ Operadores Aritméticos

Para sobrecarregar um operador, criamos uma função com o nome `operator` seguido do símbolo desejado.

```cpp
class Ponto {
public:
    int x, y;
    Ponto operator+(const Ponto& outro) {
        return {x + outro.x, y + outro.y};
    }
};
```

---

## 📤 Operador de Fluxo (`<<`)

Muito útil para imprimir objetos diretamente com `std::cout`. Ele deve ser implementado como uma função amiga (`friend`) ou fora da classe.

```cpp
friend std::ostream& operator<<(std::ostream& os, const Ponto& p) {
    os << "(" << p.x << ", " << p.y << ")";
    return os;
}
```

---

## 🧠 Boas Práticas

!!! info "Preserve o Sentido"
    Não sobrecarregue o operador `+` para fazer uma subtração. Isso confunde outros desenvolvedores e torna o código imprevisível.

!!! tip "Operadores de Comparação"
    Sobrecarregar os operadores `==` e `<` é essencial se você pretende usar seus objetos em containers da STL que precisam de ordenação ou busca.

---

## 💻 Exemplo Prático: Números Complexos

```cpp
#include <iostream>

class Complexo {
private:
    double real, imag;
public:
    Complexo(double r = 0, double i = 0) : real(r), imag(i) {}

    // Sobrecarga do +
    Complexo operator+(const Complexo& outro) {
        return Complexo(real + outro.real, imag + outro.imag);
    }

    // Sobrecarga do << para impressão fácil
    friend std::ostream& operator<<(std::ostream& os, const Complexo& c) {
        os << c.real << " + " << c.imag << "i";
        return os;
    }
};

int main() {
    Complexo c1(3, 4);
    Complexo c2(1, 2);
    Complexo c3 = c1 + c2;

    std::cout << "C1: " << c1 << std::endl;
    std::cout << "C2: " << c2 << std::endl;
    std::cout << "Soma: " << c3 << std::endl;

    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Aritmética**: Crie uma classe `Vetor2D` e sobrecarregue o operador `-` para subtrair dois vetores.
2. **Comparação**: Adicione o operador `==` à classe `Vetor2D` para verificar se dois vetores são idênticos.
3. **Desafio**: Sobrecarregue o operador `[]` para acessar os componentes `x` (índice 0) e `y` (índice 1) de um objeto `Vetor2D`.

---

## 🚀 Mini-Projeto da Aula

**Calculadora de Tempo**:
Crie uma classe `Tempo` (Horas, Minutos, Segundos). Sobrecarregue o operador `+` para somar dois horários, garantindo que os minutos e segundos extras sejam convertidos corretamente (ex: 70 segundos -> 1 minuto e 10 segundos). Implemente também o operador `<<` para exibir o tempo no formato `HH:MM:SS`.