# Aula 15 - Build e CMake 🛠️

---

## O Problema da Escala
- Um arquivo `.cpp` é fácil de compilar. { .fragment }
- Como gerenciar 1.000 arquivos, bibliotecas e sistemas diferentes? { .fragment }

---

## Compilação Separada
- Cada `.cpp` gera um arquivo `.o` (objeto). { .fragment }
- O Linker junta tudo no final. { .fragment }

---

## Arquivos de Cabeçalho (.h / .hpp)
- Contêm a "promessa" do que a função faz. { .fragment }
- Permitem que diferentes arquivos se comuniquem sem saber a implementação completa. { .fragment }

---

## Include Guards (#pragma once)
- Evitam que o compilador leia o mesmo header duas vezes (erro de redefinição). { .fragment }

---

## O que é o CMake?
- Um gerador de sistemas de build. { .fragment }
- Ele não compila; ele cria os arquivos (Makefiles, projetos VS) para quem compila. { .fragment }

---

## Vantagens do CMake
- Multiplataforma (Windows/Linux/Mac). { .fragment }
- Padrão de mercado. { .fragment }
- Gerencia dependências externas de forma simples. { .fragment }

---

## CMakeLists.txt: O Mestre
```cmake
cmake_minimum_required(VERSION 3.10)
project(MeuProjeto)

add_executable(app main.cpp utils.cpp)
```

---

## Organização de Pastas Profissional
- `/src`: Código-fonte (`.cpp`). { .fragment }
- `/include`: Cabeçalhos (`.h`). { .fragment }
- `/build`: Onde a "sujeira" (arquivos gerados) fica. { .fragment }

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
- O C++ Moderno foca em **Targets**. { .fragment }
- `target_include_directories(app PRIVATE include)` { .fragment }

---

## Compilando no Windows vs Linux
- Windows usa `\` e Linux usa `/` (CMake resolve isso!). { .fragment }
- Diferenças de extensões (`.exe` vs sem extensão). { .fragment }

---

## Flags do Compilador
- `-Wall`: Todos os avisos. { .fragment }
- `-O3`: Otimização máxima. { .fragment }
- `-std=c++20`: Define a versão da linguagem. { .fragment }

---

## Bibliotecas Estáticas (.lib / .a)
- O código é embutido dentro do seu executável. { .fragment }

---

## Bibliotecas Dinâmicas (.dll / .so)
- O código é carregado apenas quando o programa roda. { .fragment }

---

## Encontrando Bibliotecas Externas
- `find_package(TBB REQUIRED)` { .fragment }

---

## Macros e Definições (#define)
- Permitem mudar o comportamento do código conforme o sistema operacional. { .fragment }

---

## Code Linting e Formatação
- **Clang-Format**: Para manter o estilo do código. { .fragment }
- **Clang-Tidy**: Para encontrar erros de lógica e estilo. { .fragment }

---

## Sistemas de Controle de Versão (Git)
- O que colocar no `.gitignore`? { .fragment }
- Nunca coloque a pasta `build/` ou arquivos binários! { .fragment }

---

## Automação de Testes
- `enable_testing()` { .fragment }
- `add_test(NAME Teste1 COMMAND app)` { .fragment }

---

## Resumo da Aula
- Organize seu projeto desde o dia 1. { .fragment }
- Aprenda o básico de CMake: é a linguagem do C++. { .fragment }
- Separe headers de implementações. { .fragment }

---

## Fim da Aula 15
- Próxima aula: Projeto Final e Carreira!