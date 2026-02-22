# Quiz 15 - Multiplataforma e Build 🛠️

1. Qual a função dos arquivos `.h` (Headers)?
    - [ ] Guardar os dados do usuário
    - [x] Conter as declarações e assinaturas de classes e funções
    - [ ] Ser o executável do programa
    - [ ] Criar menus coloridos
    > Explicação: Headers permitem que diferentes arquivos `.cpp` conheçam a existência das funções uns dos outros.

2. Por que usamos `#pragma once` ou Include Guards?
    - [ ] Para acelerar a internet
    - [x] Para evitar que o mesmo cabeçalho seja incluído várias vezes, causando erros de redefinição
    - [ ] Para proteger o código contra pirataria
    - [ ] Para traduzir o código automaticamente
    > Explicação: Eles garantem que o compilador processe o conteúdo do arquivo apenas uma vez por unidade de tradução.

3. O que é o CMake?
    - [ ] Um compilador de C++
    - [x] Uma ferramenta que gera scripts de build para diferentes sistemas e compiladores
    - [ ] Um editor de texto (IDE)
    - [ ] Uma linguagem de banco de dados
    > Explicação: CMake é o padrão de mercado para gerenciar a compilação de projetos C++ complexos.

4. Qual o nome do arquivo de configuração do CMake?
    - [ ] config.cmake
    - [ ] makefile.txt
    - [x] CMakeLists.txt
    - [ ] build.yml
    > Explicação: O CMake procura obrigatoriamente por um arquivo chamado exatamente `CMakeLists.txt`.

5. Qual comando do CMake gera os projetos de build (na pasta atual)?
    - [ ] cmake --run
    - [ ] cmake --build
    - [x] cmake .
    - [ ] cmake compile
    > Explicação: O comando `cmake .` (ou `cmake ..` em pastas de build) configura o projeto.

6. O que a flag `-Wall` faz na compilação?
    - [ ] Constrói uma parede de proteção
    - [x] Ativa todos (All) os avisos (Warnings) do compilador
    - [ ] Deleta os arquivos temporários
    - [ ] Otimiza o código para Windows
    > Explicação: É essencial para encontrar bugs e problemas de portabilidade antes mesmo de rodar o programa.

7. Qual a diferença de Case Sensitivity entre Windows e Linux?
    - [ ] Windows diferencia letras maiúsculas de minúsculas em nomes de arquivos
    - [x] Linux diferencia (Arquivo.h != arquivo.h), enquanto o Windows geralmente ignora
    - [ ] Linux não permite nomes de arquivos longos
    - [ ] Não há diferença
    > Explicação: Esta é uma das causas mais comuns de falha em builds multiplataforma.

8. Para que serve o comando `#ifdef _WIN32`?
    - [ ] Para baixar o Windows
    - [x] Para executar um bloco de código apenas se o sistema operacional for Windows
    - [ ] Para verificar se o computador tem 32 bits
    - [ ] Para imprimir a versão do Windows
    > Explicação: São as diretivas de pré-processamento que permitem criar código específico para cada plataforma.

9. O que significa "Modularização"?
    - [ ] Escrever o código em um arquivo gigante
    - [x] Dividir o sistema em pequenos módulos ou componentes independentes
    - [ ] Mudar a cor do terminal
    - [ ] Usar apenas números inteiros
    > Explicação: Modularizar facilita o teste, a manutenção e a reutilização do código.

10. Qual a vantagem de uma "Build Out-of-Source" (Pasta Build)?
    - [ ] Não há vantagem
    - [x] Mantém a pasta de código limpa, separando os arquivos gerados (binários/objetos) dos fontes
    - [ ] O código roda 10x mais rápido
    - [ ] O arquivo final fica menor
    > Explicação: Facilita o gerenciamento de versões (Git) e permite limpar o projeto apenas deletando a pasta build.