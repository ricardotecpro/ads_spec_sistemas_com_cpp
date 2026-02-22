# Mini-Projeto 02: Calculadora de IMC ⚖️

---

### 📝 Descrição
Crie uma calculadora de Índice de Massa Corporal (IMC) que solicita dados do usuário e exibe as estatísticas básicas.

### 🎯 Requisitos
- Solicitar o nome do usuário.
- Solicitar o peso (em kg) e a altura (em metros).
- Calcular o IMC usando a fórmula: $IMC = peso / altura^2$.
- Exibir os dados formatados.

### 💡 Dicas
- Use o tipo `double` para peso e altura para maior precisão.
- Use `std::fixed` e `std::setprecision(2)` para limitar as casas decimais da saída.

```cpp
#include <iomanip> // Necessário para setprecision
// ...
cout << fixed << setprecision(2);
cout << "Seu IMC é: " << imc << endl;
```

---

### 🚀 Desafio Extra
Pesquise como usar `sizeof()` para mostrar quantos bytes o seu programa está usando para armazenar os dados do usuário.