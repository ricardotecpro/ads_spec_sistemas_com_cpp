# Aula 08 - Estruturas e Arquivos 📂

Nesta aula, aprenderemos a criar nossos próprios tipos de dados complexos e a salvar informações permanentemente em arquivos.

---

## 🏗️ Structs (Estruturas)

Uma `struct` permite agrupar variáveis de diferentes tipos sob um único nome.

```cpp
struct Produto {
    int id;
    std::string nome;
    float preco;
};

Produto p1 = {1, "Teclado", 150.00};
std::cout << p1.nome;
```

---

## 📁 Persistência com `fstream`

Para trabalhar com arquivos, usamos a biblioteca `<fstream>`.

### Tipos de Fluxo:
- `ofstream`: Escrita (Output File Stream)
- `ifstream`: Leitura (Input File Stream)
- `fstream`: Ambos

### Escrita de Arquivo
```cpp
#include <fstream>

std::ofstream arquivo("dados.txt");
arquivo << "Salvando dados no C++" << std::endl;
arquivo.close();
```

---

## 📖 Leitura de Arquivo

```cpp
std::ifstream arquivoLeitura("dados.txt");
std::string linha;

if (arquivoLeitura.is_open()) {
    while (getline(arquivoLeitura, linha)) {
        std::cout << linha << std::endl;
    }
    arquivoLeitura.close();
}
```

---

## 🧠 Boas Práticas

!!! tip "Verificação de Abertura"
    Sempre verifique se o arquivo foi aberto corretamente usando `arquivo.is_open()` ou checando o objeto diretamente `if(!arquivo)`.

!!! info "Modos de Abertura"
    Você pode usar `std::ios::app` para adicionar conteúdo ao final do arquivo (append) sem apagar o que já existe.

---

## 💻 Exemplo Prático: Registro de Usuários

```cpp
#include <iostream>
#include <fstream>
#include <string>

struct Usuario {
    std::string nome;
    int idade;
};

int main() {
    Usuario user;
    std::cout << "Nome: "; std::getline(std::cin, user.nome);
    std::cout << "Idade: "; std::cin >> user.idade;

    std::ofstream db("usuarios.txt", std::ios::app);
    if (db.is_open()) {
        db << user.nome << "," << user.idade << "\n";
        db.close();
        std::cout << "Dados salvos!" << std::endl;
    }

    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Struct**: Crie uma struct `Livro` com título, autor e ano. Crie um array de 3 livros e exiba-os.
2. **Arquivos**: Crie um programa que leia um arquivo de texto e conte quantas palavras ele possui.
3. **Desafio**: Faça um programa que leia os dados salvos em `usuarios.txt` (do exemplo prático) e exiba apenas as pessoas com mais de 18 anos.

---

## 🚀 Mini-Projeto da Aula

**Sistema de Agenda Simples**:
Desenvolva uma agenda que salve Nome e Telefone em um arquivo `.csv`. O programa deve ter um menu para: 1-Adicionar Contato, 2-Listar todos os contatos e 0-Sair.