# Quiz 10 - Construtores e Destrutores 🏗️

1. Quando o "Construtor" de uma classe é executado?
    - [ ] Quando o programa acaba
    - [x] No momento em que um objeto da classe é instanciado
    - [ ] Apenas se for chamado manualmente
    - [ ] Ao compilar o código
    > Explicação: O construtor serve para inicializar o objeto automaticamente.

2. Qual o nome obrigatório de um construtor?
    - [ ] init()
    - [ ] constructor()
    - [x] O mesmo nome da classe
    - [ ] setup()
    > Explicação: C++ identifica o construtor pelo nome idêntico ao da classe, sem tipo de retorno.

3. O que é o "Destrutor"?
    - [ ] Uma função que apaga o código-fonte
    - [x] Um método especial chamado quando o objeto sai de escopo ou é deletado
    - [ ] Um vírus de computador
    - [ ] O compilador
    > Explicação: O destrutor libera recursos e limpa a memória do objeto.

4. Como identificamos um destrutor no código?
    - [ ] Pela palavra end
    - [x] Pelo símbolo til (~) antes do nome da classe
    - [ ] Pelo nome final()
    - [ ] Pela cor vermelha no editor
    > Explicação: O til `~` simboliza o oposto (destruição) da criação.

5. O que é uma "Lista de Inicialização" em um construtor?
    - [ ] Uma lista de compras
    - [x] Uma forma eficiente de definir valores iniciais aos atributos antes do corpo do construtor
    - [ ] Um array de strings
    - [ ] O menu do programa
    > Explicação: Sintaxe `: atributo(valor)` que melhora a performance e permite inicializar constantes.

6. Quantos destrutores uma classe pode ter?
    - [ ] Quantos desejar
    - [x] Apenas um
    - [ ] Dois (um para cada sistema operacional)
    - [ ] Zero
    > Explicação: Diferente dos construtores, o destrutor não pode ter parâmetros nem sobrecarga.

7. O que acontece se você não definir um construtor na sua classe?
    - [ ] O programa não compila
    - [x] O compilador cria um "Construtor Padrão" vazio automaticamente
    - [ ] O objeto não é criado
    - [ ] Um erro de tempo de execução ocorre
    > Explicação: O C++ provê um construtor básico se nenhum outro for especificado.

8. Qual a função da "Regra dos Três"?
    - [ ] Fazer o código rodar 3x mais rápido
    - [x] Garantir que classes que gerenciam memória tenham Destrutor, Construtor de Cópia e Operador de Atribuição
    - [ ] Limitar o tamanho das funções
    - [ ] Proteger contra 3 tipos de hackers
    > Explicação: É uma diretriz para evitar bugs sutis de cópia rasa de ponteiros.

9. Pode haver sobrecarga de construtores?
    - [x] Sim, podemos ter vários construtores com parâmetros diferentes
    - [ ] Não, apenas um por classe
    - [ ] Apenas no C++ moderno
    - [ ] Apenas se a classe for pública
    > Explicação: Isso permite criar objetos de formas variadas (ex: `Data()` e `Data(dia, mes, ano)`).

10. Um destrutor pode retornar um valor?
    - [ ] Sim, um código de erro
    - [x] Não, destrutores nunca possuem tipo de retorno
    - [ ] Apenas se for booleano
    - [ ] Apenas se for void
    > Explicação: O papel do destrutor é apenas limpeza, sem comunicação de retorno.