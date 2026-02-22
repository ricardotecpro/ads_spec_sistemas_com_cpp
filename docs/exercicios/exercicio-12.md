# Exercícios - Aula 12: Sobrecarga de Operadores

Personalizando a sintaxe dos seus objetos.

### 🟢 Básicos
1. **Sobrecarga SOMA**: Crie uma classe `Peso` (com um atributo `kg`) e sobrecarregue o operador `+` para somar dois pesos.
2. **Operador de Saída**: Sobrecarregue o operador `<<` para que você possa imprimir um objeto `Peso` diretamente com `std::cout`.

### 🟡 Intermediários
3. **Comparação**: Sobrecarregue o operador `>` para comparar dois objetos `Peso`.
4. **Operador de Atribuição**: Implemente a sobrecarga do operador `=` para garantir uma cópia segura entre dois objetos que contenham dados dinâmicos.

### 🔴 Desafio
5. **Operador de Incremento**: Sobrecarregue o operador `++` (prefixado) para a sua classe `Peso`, aumentando o valor de `kg` em 1.