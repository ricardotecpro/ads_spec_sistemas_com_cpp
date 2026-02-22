# Exercícios - Aula 10: Construtores e Destrutores

Gerenciando o ciclo de vida dos objetos.

### 🟢 Básicos
1. **Construtor Padrão**: Crie uma classe `Lampada` que tenha um construtor que imprime "Lâmpada fabricada!" toda vez que um objeto é criado.
2. **Destrutor**: Adicione um destrutor à classe `Lampada` que imprima "Lâmpada descartada!" ao final do programa.

### 🟡 Intermediários
3. **Construtor Parametrizado**: Crie uma classe `Smartphone` que receba no construtor o modelo e a marca, usando uma lista de inicialização.
4. **Sobrecarga de Construtor**: Crie dois construtores para uma classe `Data`: um que não recebe nada (e define 01/01/2000) e outro que recebe dia, mês e ano.

### 🔴 Desafio
5. **Rastreamento de Instâncias**: Use um membro estático (`static int contador`) para contar quantos objetos da classe `Robo` existem simultaneamente. Incremente no construtor e decremente no destrutor.