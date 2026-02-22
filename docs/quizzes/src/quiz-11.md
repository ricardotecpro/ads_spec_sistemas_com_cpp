# Quiz 11 - Herança e Polimorfismo 🌳

1. O que é "Herança" em POO?
    - [ ] Receber dinheiro de um parente
    - [x] Mecanismo onde uma classe adota atributos e métodos de outra classe pai
    - [ ] Copiar e colar código
    - [ ] Um erro de linkagem
    > Explicação: A herança promove o reaproveitamento de código e cria hierarquias lógicas.

2. Como chamamos a classe que fornece a herança?
    - [ ] Classe Filha
    - [x] Classe Base ou Classe Pai
    - [ ] Subclasse
    - [ ] Framework
    > Explicação: No C++, a classe base define os comportamentos comuns.

3. O que o modificador `protected` faz?
    - [ ] O mesmo que o private
    - [x] Torna o membro visível para a própria classe e suas classes filhas
    - [ ] Protege contra escrita
    - [ ] Torna o membro público para todos
    > Explicação: É o meio-termo ideal para membros que as sub-classes precisam acessar, mas o mundo externo não.

4. O que é "Polimorfismo"?
    - [ ] Um tipo de herança múltipla
    - [x] Capacidade de objetos de diferentes classes serem tratados como se fossem de uma base comum
    - [ ] Mudar o nome do objeto em tempo de execução
    - [ ] Converter int para float
    > Explicação: Vem do grego "muitas formas"; um mesmo comando pode ter comportamentos distintos conforme o objeto.

5. Para que serve a palavra-chave `virtual` em um método?
    - [ ] Para indicar que a função é de mentira
    - [x] Para habilitar a resolução dinâmica (polimorfismo) em tempo de execução
    - [ ] Para economizar memória
    - [ ] Para tornar a função global
    > Explicação: Sem `virtual`, o compilador usará a versão da função base em vez da sobrescrita pelo filho.

6. O que é uma "Classe Abstrata"?
    - [ ] Uma classe difícil de entender
    - [x] Uma classe que possui ao menos uma função virtual pura e não pode ser instanciada
    - [ ] Uma classe sem métodos
    - [ ] Uma classe que só existe no header
    > Explicação: Ela serve unicamente como molde para outras classes.

7. O que indica essa sintaxe: `virtual void som() = 0;`?
    - [ ] O som do computador é zero
    - [x] É uma Função Virtual Pura
    - [ ] É uma função que retorna zero
    - [ ] É um erro de sintaxe
    > Explicação: O `= 0` obriga que toda classe filha implemente esta função.

8. Para que usamos a palavra `override`?
    - [ ] Para apagar a função do pai
    - [x] Para garantir que o compilador verifique se estamos realmente sobrescrevendo uma função virtual do pai
    - [ ] Para ignorar avisos do compilador
    - [ ] Para tornar a função pública
    > Explicação: É uma boa prática do C++ Moderno que evita erros de digitação sutis em assinaturas de funções.

9. Se uma classe tem métodos virtuais, o seu destrutor deve ser...
    - [ ] Privado
    - [ ] Estático
    - [x] Virtual
    - [ ] Inline
    > Explicação: Destrutores virtuais garantem que a memória do objeto filho seja liberada corretamente se deletado via ponteiro do pai.

10. Pode haver herança múltipla no C++ (uma classe com dois pais)?
    - [x] Sim, C++ suporta herança de múltiplas classes base
    - [ ] Não, é impossível
    - [ ] Apenas com bibliotecas externas
    - [ ] Apenas no Linux
    > Explicação: C++ permite herdar de várias classes, embora exija cuidado com o problema do diamante.