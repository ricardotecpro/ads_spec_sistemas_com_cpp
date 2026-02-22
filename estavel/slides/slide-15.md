# Aula 15 - Build e CMake 🛠️

---

## O Problema da Escala
- Um arquivo `.cpp` é fácil de compilar. <!-- .element: class="fragment" -->
- Como gerenciar 1.000 arquivos, bibliotecas e sistemas diferentes? <!-- .element: class="fragment" -->

---

## Compilação Separada
- Cada `.cpp` gera um arquivo `.o` (objeto). <!-- .element: class="fragment" -->
- O Linker junta tudo no final. <!-- .element: class="fragment" -->

---

## Arquivos de Cabeçalho (.h / .hpp)
- Contêm a "promessa" do que a função faz. <!-- .element: class="fragment" -->
- Permitem que diferentes arquivos se comuniquem sem saber a implementação completa. <!-- .element: class="fragment" -->

---

## Include Guards (#pragma once)
- Evitam que o compilador leia o mesmo header duas vezes (erro de redefinição). <!-- .element: class="fragment" -->

---

## O que é o CMake?
- Um gerador de sistemas de build. <!-- .element: class="fragment" -->
- Ele não compila; ele cria os arquivos (Makefiles, projetos VS) para quem compila. <!-- .element: class="fragment" -->

---

## Vantagens do CMake
- Multiplataforma (Windows/Linux/Mac). <!-- .element: class="fragment" -->
- Padrão de mercado. <!-- .element: class="fragment" -->
- Gerencia dependências externas de forma simples. <!-- .element: class="fragment" -->

---

## CMakeLists.txt: O Mestre
```cmake
cmake_minimum_required(VERSION 3.10)
project(MeuProjeto)

add_executable(app main.cpp utils.cpp)
```

---

## Organização de Pastas Profissional
- `/src`: Código-fonte (`.cpp`). <!-- .element: class="fragment" -->
- `/include`: Cabeçalhos (`.h`). <!-- .element: class="fragment" -->
- `/build`: Onde a "sujeira" (arquivos gerados) fica. <!-- .element: class="fragment" -->

---

## Construindo o Projeto (Build Out-of-Source)
```bash
mkdir build
cd build
cmake ..
cmake --build .
```

---

## Target-Based CMake
- O C++ Moderno foca em **Targets**. <!-- .element: class="fragment" -->
- `target_include_directories(app PRIVATE include)` <!-- .element: class="fragment" -->

---

## Compilando no Windows vs Linux
- Windows usa `\` e Linux usa `/` (CMake resolve isso!). <!-- .element: class="fragment" -->
- Diferenças de extensões (`.exe` vs sem extensão). <!-- .element: class="fragment" -->

---

## Flags do Compilador
- `-Wall`: Todos os avisos. <!-- .element: class="fragment" -->
- `-O3`: Otimização máxima. <!-- .element: class="fragment" -->
- `-std=c++20`: Define a versão da linguagem. <!-- .element: class="fragment" -->

---

## Bibliotecas Estáticas (.lib / .a)
- O código é embutido dentro do seu executável. <!-- .element: class="fragment" -->

---

## Bibliotecas Dinâmicas (.dll / .so)
- O código é carregado apenas quando o programa roda. <!-- .element: class="fragment" -->

---

## Encontrando Bibliotecas Externas
- `find_package(TBB REQUIRED)` <!-- .element: class="fragment" -->

---

## Macros e Definições (#define)
- Permitem mudar o comportamento do código conforme o sistema operacional. <!-- .element: class="fragment" -->

---

## Code Linting e Formatação
- **Clang-Format**: Para manter o estilo do código. <!-- .element: class="fragment" -->
- **Clang-Tidy**: Para encontrar erros de lógica e estilo. <!-- .element: class="fragment" -->

---

## Sistemas de Controle de Versão (Git)
- O que colocar no `.gitignore`? <!-- .element: class="fragment" -->
- Nunca coloque a pasta `build/` ou arquivos binários! <!-- .element: class="fragment" -->

---

## Automação de Testes
- `enable_testing()` <!-- .element: class="fragment" -->
- `add_test(NAME Teste1 COMMAND app)` <!-- .element: class="fragment" -->

---

## Resumo da Aula
- Organize seu projeto desde o dia 1. <!-- .element: class="fragment" -->
- Aprenda o básico de CMake: é a linguagem do C++. <!-- .element: class="fragment" -->
- Separe headers de implementações. <!-- .element: class="fragment" -->

---

## Fim da Aula 15
- Próxima aula: Projeto Final e Carreira!