# Mini-Projeto 13: Supermercado com STL 🛒

---

### 📝 Descrição
Crie um sistema simplificado de caixa de supermercado usando os containers e algoritmos da STL para gerenciar o inventário e as vendas.

### 🎯 Requisitos
- Usar um `std::map<int, string>` para associar IDs de produtos aos seus nomes.
- Usar um `std::vector<double>` para armazenar os preços dos itens no carrinho.
- Usar o algoritmo `std::accumulate` (da biblioteca `<numeric>`) para calcular o valor total da compra.
- Usar `std::sort` para exibir os preços do carrinho em ordem crescente no cupom fiscal.

### 💡 Dicas
- O `std::map` facilita a busca rápida de produtos pelo código de barras.
- Integre com lambdas para aplicar descontos automáticos em itens acima de um certo valor.

---

### 🚀 Desafio Extra
Adicione uma funcionalidade de "Remover último item" usando `pop_back()` e verifique se o carrinho está vazio com `empty()` antes de finalizar.