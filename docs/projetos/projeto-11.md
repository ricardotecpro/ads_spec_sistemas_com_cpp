# Mini-Projeto 11: Sistema de Gestão de Frota 🚗

---

### 📝 Descrição
Utilize herança e polimorfismo para gerenciar diferentes tipos de veículos em uma transportadora.

### 🎯 Requisitos
- Classe base abstrata `Veiculo` com método virtual puro `calcularCustoViagem(distancia)`.
- Classes filhas `Caminhao` e `Moto` que herdam de `Veiculo`.
- O custo do caminhão deve ser $R\$ 5,00/km$ e da moto $R\$ 1,00/km$.

### 💡 Dicas
- Use o modificador `override` nas classes filhas.
- Crie um loop na `main` que percorra um array de ponteiros `Veiculo*` e exiba o custo para todos.

---

### 🚀 Desafio Extra
Adicione um atributo `capacidadeCarga` na classe `Veiculo` e use-o no cálculo do custo do caminhão (quanto mais pesado, mais caro o km).