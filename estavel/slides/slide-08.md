# Aula 08 - Estruturas e Arquivos 📂

---

## O que é uma Struct?
- Uma estrutura que agrupa variáveis de diferentes tipos sob um único nome. <!-- .element: class="fragment" -->
- Ideal para representar entidades reais (Carro, Aluno, Produto). <!-- .element: class="fragment" -->

---

## Declaração de Struct
```cpp
struct Aluno {
    string nome;
    int idade;
    float nota;
};
```

---

## Instanciação e Acesso
```cpp
Aluno a1;
a1.nome = "Ricardo";
a1.idade = 20;
```

---

## Inicialização (C++11+)
```cpp
Aluno a2{"Maria", 22, 9.5f};
```

---

## Arrays de Structs
```cpp
Aluno turma[30];
turma[0].nome = "Ana";
```

---

## Structs Aninhadas
- Uma struct dentro de outra. <!-- .element: class="fragment" -->
```cpp
struct Endereco { string rua; int num; };
struct Pessoa { string nome; Endereco local; };
```

---

## Persistência de Dados
- Como salvar dados para que não sumam ao fechar o programa? <!-- .element: class="fragment" -->
- **Arquivos!** <!-- .element: class="fragment" -->

---

## Biblioteca fstream
- `#include <fstream>` <!-- .element: class="fragment" -->
- `ifstream`: Input (Leitura). <!-- .element: class="fragment" -->
- `ofstream`: Output (Escrita). <!-- .element: class="fragment" -->
- `fstream`: Ambos. <!-- .element: class="fragment" -->

---

## Gravando em Arquivo
```cpp
ofstream arquivo("teste.txt");
if (arquivo.is_open()) {
    arquivo << "Olá arquivo!" << endl;
    arquivo.close();
}
```

---

## Lendo de Arquivo
```cpp
ifstream leitura("teste.txt");
string linha;
while (getline(leitura, linha)) {
    cout << linha << endl;
}
```

---

## Modos de Abertura
- `ios::out`: Sobrescrever (Padrão ofstream). <!-- .element: class="fragment" -->
- `ios::app`: Adicionar ao fim (Append). <!-- .element: class="fragment" -->
- `ios::binary`: Modo binário. <!-- .element: class="fragment" -->

---

## Verificação de Sucesso
- Sempre teste `if (!arquivo)` antes de usar. <!-- .element: class="fragment" -->
- Arquivos podem não abrir por falta de permissão ou caminho errado. <!-- .element: class="fragment" -->

---

## Manipulando Dados Estruturados em Arquivos
- Dica: Salve uma struct por linha, separada por vírgulas (formato CSV). <!-- .element: class="fragment" -->

---

## Parsing de Dados
- Processo de ler uma linha de texto e separar os campos para preencher uma struct. <!-- .element: class="fragment" -->

---

## Arquivos Binários
- Mais rápidos e compactos que arquivos de texto. <!-- .element: class="fragment" -->
- Salvam a imagem exata da memória. <!-- .element: class="fragment" -->

---

## Struct vs Class (Spoiler)
- No C++, a única diferença é que na `struct` tudo é público por padrão. <!-- .element: class="fragment" -->
- Na `class`, tudo é privado por padrão. <!-- .element: class="fragment" -->

---

## Boas Práticas
- Use letras maiúsculas para nomes de Structs (`Produto`). <!-- .element: class="fragment" -->
- Sempre feche o arquivo com `.close()`. <!-- .element: class="fragment" -->

---

## Performance: Buffer
- O C++ usa um buffer para não escrever no disco a cada letra. <!-- .element: class="fragment" -->
- `endl` força o despejo (flush) do buffer. <!-- .element: class="fragment" -->

---

## Tratamento de Caminhos
- Use caminhos relativos ao executável para portabilidade. <!-- .element: class="fragment" -->

---

## Exemplo Real: Banco de Dados de Alunos
- Criar um menu que permita Cadastrar, Listar e Salvar alunos em disco. <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Structs organizam os dados. <!-- .element: class="fragment" -->
- Arquivos garantem a permanência. <!-- .element: class="fragment" -->
- Validação é obrigatória para evitar travamentos. <!-- .element: class="fragment" -->

---

## Fim da Aula 08
- Próxima aula: Conceitos de POO!