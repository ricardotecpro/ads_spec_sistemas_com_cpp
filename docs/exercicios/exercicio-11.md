# Exercícios - Aula 11: Herança e Polimorfismo

Construindo hierarquias de classes.

### 🟢 Básicos
1. **Herança Simples**: Crie uma classe pai `Veiculo` e uma classe filha `Moto` que herde de `Veiculo`.
2. **Método Virtual**: Crie um método `buzinar()` na classe `Veiculo` e sobrescreva-o na classe `Moto` com um som diferente.

### 🟡 Intermediários
3. **Ponteiro da Base**: Crie um ponteiro do tipo `Veiculo*` que aponte para um objeto `Moto`. Chame o método `buzinar()` e verifique qual implementação é executada.
4. **Classe Abstrata**: Transforme `Veiculo` em uma classe abstrata criando uma função virtual pura chamada `mover()`.

### 🔴 Desafio
5. **Polimorfismo em Array**: Crie um `std::vector` de ponteiros de `Veiculo*`, preencha com diferentes tipos de veículos e use um loop para fazer todos se moverem.