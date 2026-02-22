# Exercícios - Aula 15: Multiplataforma e Build

Organizando projetos de forma profissional.

### 🟢 Básicos
1. **Divisão de Arquivos**: Crie um par de arquivos `Geometria.h` e `Geometria.cpp` com uma função que calcule a área de um círculo.
2. **Include Guard**: Adicione `#pragma once` ao seu arquivo header e explique o que aconteceria se ele fosse incluído duas vezes sem isso.

### 🟡 Intermediários
3. **Escrita de CMake**: Escreva um arquivo `CMakeLists.txt` manual que compile dois arquivos fonte para gerar um executável chamado `AppGeometrica`.
4. **Macros de Sistema**: Use `#if defined(_WIN32)` e `#elif defined(__linux__)` para criar um código que exiba as extensões de arquivos suportadas em cada sistema (ex: .exe vs .bin).

### 🔴 Desafio
5. **Flags de Compilação**: Tente compilar um projeto usando as flags `-Wall -Werror`. O que essas flags forçam o desenvolvedor a fazer?