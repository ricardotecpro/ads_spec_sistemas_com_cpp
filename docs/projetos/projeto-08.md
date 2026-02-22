# Mini-Projeto 08: Cadastro de Produtos em Arquivo 💾

---

### 📝 Descrição
Crie um sistema que permite cadastrar produtos e salvá-los permanentemente em um arquivo de texto.

### 🎯 Requisitos
- Definir uma `struct Produto` com Nome, Preço e Código.
- Criar um menu com as opções: 1-Adicionar Produto, 2-Listar Todos, 3-Sair.
- Os produtos devem ser salvos em um arquivo chamado `produtos.txt`.

### 💡 Dicas
- Ao listar, leia o arquivo do início ao fim usando um loop `while`.
- Use o modo de abertura `std::ios::app` para não apagar os produtos já cadastrados ao adicionar um novo.

```cpp
ofstream file("produtos.txt", ios::app);
if (file.is_open()) {
    file << p.nome << " " << p.preco << endl;
}
```

---

### 🚀 Desafio Extra
Adicione uma opção para limpar todo o arquivo de produtos (resete o banco de dados).