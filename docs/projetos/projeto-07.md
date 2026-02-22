# Mini-Projeto 07: Gestor de Memória Dinâmica 🧠

---

### 📝 Descrição
Simule um sistema que aloca dinamicamente espaço para um inventário de itens, cujo tamanho é decidido pelo usuário.

### 🎯 Requisitos
- Perguntar ao usuário quantos itens ele deseja cadastrar.
- Alocar dinamicamente um array de inteiros (IDs de itens).
- Preencher o array e depois exibir os valores.
- **Obrigatório**: Liberar a memória ao final usando `delete[]`.

### 💡 Dicas
- Lembre-se de verificar se a alocação foi bem-sucedida.
- Use ponteiros para percorrer o array alocado.

```cpp
int* inventario = new int[quantidade];
// ... processamento ...
delete[] inventario;
```

---

### 🚀 Desafio Extra
Crie uma função que redimensione o array caso o usuário queira adicionar mais itens (copiando os dados antigos para um novo espaço maior).