# Mini-Projeto 14: Sistema de Gestão de Sensores (RAII) 🌡️

---

### 📝 Descrição
Simule um sistema de monitoramento industrial que gerencia múltiplos sensores usando Smart Pointers para garantir que nenhum sensor fique "perdido" na memória.

### 🎯 Requisitos
- Classe `Sensor` com atributos `id` e `leitura`.
- Usar `std::unique_ptr` para criar instâncias de sensores que pertencem apenas a uma central de controle.
- Usar `std::vector<std::unique_ptr<Sensor>>` para gerenciar a lista de sensores ativos.
- Demonstrar o uso de `std::move()` para transferir um sensor de uma central para outra.

### 💡 Dicas
- O uso de `make_unique` é obrigatório para seguir as boas práticas modernas.
- Observe as mensagens do destrutor da classe `Sensor` aparecendo automaticamente quando o vetor é limpo ou sai de escopo.

---

### 🚀 Desafio Extra
Implemente uma classe `Alerta` que usa um `std::shared_ptr` para que múltiplos módulos do sistema possam observar o mesmo sensor simultaneamente.