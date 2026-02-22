# Aula 15 - Multiplataforma e Build 🛠️

Nesta aula, sairemos do arquivo único e aprenderemos como organizar projetos profissionais que funcionam tanto no Windows quanto no Linux.

---

## 📂 Organização de Múltiplos Arquivos

Em projetos reais, separamos a **interface** (Headers) da **implementação** (Source).

- **`.h` / `.hpp`**: Contém apenas as declarações de classes e funções.
- **`.cpp`**: Contém a lógica de funcionamento.

### Exemplo de Estrutura:
- `include/Calculadora.h`
- `src/Calculadora.cpp`
- `main.cpp`

---

## 🏗️ CMake: A Ferramenta de Build Padrão

O **CMake** é uma ferramenta multiplataforma que gera os scripts de compilação automáticos (Makefiles, Projetos Visual Studio, etc).

`CMakeLists.txt` básico:
```cmake
cmake_minimum_required(VERSION 3.10)
project(MeuSistema)

add_executable(MeuSistema main.cpp src/Calculadora.cpp)
```

---

## 🌍 Diferenças Windows vs Linux

| Característica | Windows | Linux |
| :--- | :--- | :--- |
| Extensão | `.exe` | Sem extensão (binário) |
| Separador | `\` (Contra-barra) | `/` (Barra) |
| Compilador | MSVC / MinGW | GCC / Clang |
| Case Sensitivity | Insensível aos nomes | Sensível aos nomes |

---

## 🧠 Flags Importantes do Compilador

!!! tip "Dicas de Build"
    - `-Wall`: Ativa todos os avisos de erro comuns.
    - `-O2` ou `-O3`: Ativa otimizações de performance.
    - `-std=c++17`: Define a versão do padrão da linguagem.

!!! info "Include Guards"
    Sempre use `#pragma once` no topo dos seus arquivos `.h` para evitar que o compilador inclua o mesmo arquivo várias vezes, o que geraria erros de redefinição.

---

## 💻 Exemplo Prático: Scripts de Build

<div class="termy" markdown="1">
```bash
$ mkdir build && cd build
$ cmake ..
$ cmake --build .
$ ./MeuSistema
```
</div>

---

## 📝 Exercício de Fixação

1. **Modularização**: Crie um projeto com uma classe `Util` separada em arquivos `.h` e `.cpp`.
2. **CMake**: Escreva um `CMakeLists.txt` para compilar o projeto anterior.
3. **Desafio**: Use `#ifdef _WIN32` para criar uma função que imprima "Rodando no Windows" ou "Rodando no Linux" dependendo do sistema.

---

## 🚀 Mini-Projeto da Aula

**Template de Projeto Profissional**:
Organize uma pasta de projeto seguindo o padrão: `src`, `include`, `build` e `data`. Inclua um `CMakeLists.txt` funcional e um `README.md` explicando como compilar o projeto. Esse template será a base para o seu Projeto Final.