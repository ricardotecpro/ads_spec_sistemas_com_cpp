# Mini-Projeto 05: Sistema de Conversão de Temperatura 🌡️

---

### 📝 Descrição
Crie um programa modularizado que converte temperaturas entre Celsius, Fahrenheit e Kelvin.

### 🎯 Requisitos
- Uma função para cada tipo de conversão (Ex: `celsiusParaFahrenheit`).
- Uma função de menu para exibir as opções.
- Uso de passagem por valor para garantir que a temperatura original não seja alterada sem necessidade.

### 💡 Dicas
- Mantenha a `main` limpa: ela deve apenas chamar as funções.
- Tente usar a sobrecarga de funções para criar uma função `imprimirTemperatura` que aceite tanto um `int` quanto um `double`.

```cpp
double toFahrenheit(double c) {
    return (c * 9/5) + 32;
}
```

---

### 🚀 Desafio Extra
Implemente uma função que aceite uma temperatura e um código de unidade ('C', 'F', 'K') e retorne a temperatura correspondente em todas as outras unidades.