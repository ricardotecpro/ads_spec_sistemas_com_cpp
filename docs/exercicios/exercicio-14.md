# Exercícios - Aula 14: Gerenciamento de Memória

Explorando Smart Pointers e segurança de memória.

### 🟢 Básicos
1. **Unique Pointer**: Crie um `std::unique_ptr` para um inteiro e mude o seu valor.
2. **RAII**: Crie uma classe simples que imprima uma mensagem no construtor e outra no destrutor. Verifique se a mensagem do destrutor aparece ao sair de um bloco `{}`.

### 🟡 Intermediários
3. **Shared Pointer**: Crie um `std::shared_ptr` e passe-o para duas funções diferentes. Imprima o contador de referências dentro de cada função.
4. **Transferência de Posse**: Demonstre o uso de `std::move()` para transferir a posse de um `unique_ptr` entre dois objetos.

### 🔴 Desafio
5. **Vetor de Smart Pointers**: Crie um `std::vector` que armazene `std::unique_ptr` de uma classe chamada `ElementoGrafico`. Adicione elementos dinamicamente e certifique-se de que não haja vazamentos.