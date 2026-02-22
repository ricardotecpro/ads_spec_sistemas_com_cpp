# Quiz 08 - Estruturas e Arquivos 📂

1. Para que serve uma `struct` no C++?
    - [ ] Para criar um loop infinito
    - [x] Para agrupar diferentes tipos de dados sob um único nome
    - [ ] Para definir apenas números inteiros
    - [ ] Para importar bibliotecas externas
    > Explicação: `struct` permite criar registros personalizados (ex: Produto com Nome, Preço e ID).

2. Qual a biblioteca padrão para manipulação de arquivos?
    - [ ] stdio.h
    - [ ] iostream
    - [x] fstream
    - [ ] string
    > Explicação: `fstream` (File Stream) contém as classes `ifstream`, `ofstream` e `fstream`.

3. Qual a diferença entre `ifstream` e `ofstream`?
    - [ ] ofstream é mais rápido
    - [ ] ifstream é para gravar, ofstream para ler
    - [x] ifstream é para leitura (input), ofstream para escrita (output)
    - [ ] Não há diferença
    > Explicação: Os nomes seguem a lógica: Input File Stream e Output File Stream.

4. O que o modo `std::ios::app` faz ao abrir um arquivo?
    - [ ] Apaga o conteúdo original
    - [x] Adiciona o novo conteúdo ao final (Append)
    - [ ] Protege o arquivo com senha
    - [ ] Converte para binário
    > Explicação: O modo Append evita a sobrescrita dos dados existentes.

5. Como verificamos se um arquivo foi aberto com sucesso?
    - [ ] arquivo.check()
    - [x] arquivo.is_open() ou if(arquivo)
    - [ ] arquivo.status == 200
    - [ ] isfile(arquivo)
    > Explicação: É fundamental checar se o arquivo existe ou se há permissões de acesso.

6. Como acessamos um membro de uma struct (`s`)?
    - [ ] s->membro
    - [x] s.membro (Operador de Ponto)
    - [ ] s:membro
    - [ ] s[membro]
    > Explicação: O ponto é usado para acesso direto a instâncias de structs e classes.

7. O que o comando `arquivo.close()` faz?
    - [ ] Deleta o arquivo do disco
    - [x] Libera o recurso e garante que os dados foram salvos (flush)
    - [ ] Oculta o arquivo
    - [ ] Formata o conteúdo
    > Explicação: Fechar o arquivo é essencial para liberar o "handle" do sistema operacional.

8. Podemos ter uma `struct` dentro de outra `struct`?
    - [x] Sim (Structs Aninhadas)
    - [ ] Não, é proibido
    - [ ] Apenas se forem do mesmo tamanho
    - [ ] Sim, mas apenas uma vez
    > Explicação: Isso permite modelar dados complexos, como um "Aluno" que possui uma struct "Endereco".

9. O que significa o sufixo `.csv` em arquivos de dados?
    - [ ] Comprimido Sem Vírus
    - [x] Comma Separated Values (Valores Separados por Vírgula)
    - [ ] C++ Standard Version
    - [ ] Code System Validated
    > Explicação: É um formato de texto comum usado para representar planilhas e bancos de dados simples.

10. No C++, qual a principal diferença técnica entre `struct` e `class`?
    - [ ] struct é mais lenta
    - [ ] class não aceita funções
    - [x] Por padrão, membros de struct são públicos e de class são privados
    - [ ] struct não suporta herança
    > Explicação: Funcionalmente são quase idênticas, mudando apenas a visibilidade padrão.