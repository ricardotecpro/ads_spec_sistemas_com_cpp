# Mini-Projeto 15: Boilerplate de Projeto CMake 🏗️

---

### 📝 Descrição
Prepare a estrutura profissional que será usada no seu Projeto Final, configurando o sistema de build corretamente.

### 🎯 Requisitos
- Criar a pasta do projeto com as subpastas `src`, `include` e `lib`.
- Criar um arquivo `CMakeLists.txt` que compile um executável a partir de pelo menos dois arquivos `.cpp` e um `.h`.
- Configurar o CMake para usar o padrão C++20 (`set(CMAKE_CXX_STANDARD 20)`).
- O programa deve apenas exibir uma mensagem de "Ambiente Configurado com Sucesso!".

### 💡 Dicas
- Use `target_include_directories` para apontar para a pasta `include`.
- Verifique se o binário final é gerado dentro de uma pasta `build/` separada do código-fonte.

---

### 🚀 Desafio Extra
Adicione uma flag no CMake para habilitar avisos extras (`-Wall`) apenas se o compilador for o GCC ou Clang.