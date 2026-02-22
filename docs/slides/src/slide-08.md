# Aula 08 - Estruturas e Arquivos 📂

---

## O que é uma Struct?
- Uma estrutura que agrupa variáveis de diferentes tipos sob um único nome. { .fragment }
- Ideal para representar entidades reais (Carro, Aluno, Produto). { .fragment }

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
- Uma struct dentro de outra. { .fragment }
```cpp
struct Endereco { string rua; int num; };
struct Pessoa { string nome; Endereco local; };
```

---

## Persistência de Dados
- Como salvar dados para que não sumam ao fechar o programa? { .fragment }
- **Arquivos!** { .fragment }

---

## Biblioteca fstream
- `#include <fstream>` { .fragment }
- `ifstream`: Input (Leitura). { .fragment }
- `ofstream`: Output (Escrita). { .fragment }
- `fstream`: Ambos. { .fragment }

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
- `ios::out`: Sobrescrever (Padrão ofstream). { .fragment }
- `ios::app`: Adicionar ao fim (Append). { .fragment }
- `ios::binary`: Modo binário. { .fragment }

---

## Verificação de Sucesso
- Sempre teste `if (!arquivo)` antes de usar. { .fragment }
- Arquivos podem não abrir por falta de permissão ou caminho errado. { .fragment }

---

## Manipulando Dados Estruturados em Arquivos
- Dica: Salve uma struct por linha, separada por vírgulas (formato CSV). { .fragment }

---

## Parsing de Dados
- Processo de ler uma linha de texto e separar os campos para preencher uma struct. { .fragment }

---

## Arquivos Binários
- Mais rápidos e compactos que arquivos de texto. { .fragment }
- Salvam a imagem exata da memória. { .fragment }

---

## Struct vs Class (Spoiler)
- No C++, a única diferença é que na `struct` tudo é público por padrão. { .fragment }
- Na `class`, tudo é privado por padrão. { .fragment }

---

## Boas Práticas
- Use letras maiúsculas para nomes de Structs (`Produto`). { .fragment }
- Sempre feche o arquivo com `.close()`. { .fragment }

---

## Performance: Buffer
- O C++ usa um buffer para não escrever no disco a cada letra. { .fragment }
- `endl` força o despejo (flush) do buffer. { .fragment }

---

## Tratamento de Caminhos
- Use caminhos relativos ao executável para portabilidade. { .fragment }

---

## Exemplo Real: Banco de Dados de Alunos
- Criar um menu que permita Cadastrar, Listar e Salvar alunos em disco. { .fragment }

---

## Resumo da Aula
- Structs organizam os dados. { .fragment }
- Arquivos garantem a permanência. { .fragment }
- Validação é obrigatória para evitar travamentos. { .fragment }

---

## Fim da Aula 08
- Próxima aula: Conceitos de POO!