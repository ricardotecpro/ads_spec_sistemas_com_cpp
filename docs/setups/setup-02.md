# Setup 02: C e C++ 🚀

## Opção 1: Code::Blocks (Mais Fácil)
Ideal para iniciantes, pois já vem com tudo configurado.
1.  Acesse [codeblocks.org](https://www.codeblocks.org/downloads/binaries/).
2.  Baixe a versão que tem **mingw-setup.exe** no nome (ex: `codeblocks-20.03mingw-setup.exe`).
3.  Instale e execute. Ele deve detectar o compilador automaticamente.

## Opção 2: VS Code + MinGW (Profissional)
1.  **Baixe o MinGW-w64**: [sourceforge.net/projects/mingw-w64/](https://sourceforge.net/projects/mingw-w64/).
2.  Extraia e coloque a pasta na raiz `C:\mingw64`.
3.  **Variáveis de Ambiente**:
    *   Pesquise "Variáveis de Ambiente" no Windows.
    *   Edite o `Path` e adicione `C:\mingw64\bin`.
4.  **VS Code**: Instale a extensão "C/C++" da Microsoft.

## 4. Solução de Problemas Comuns ⚠️

*   **'gcc' não é reconhecido**: Você esqueceu de adicionar a pasta `bin` do MinGW ao PATH do Windows. Revise o passo 1.
*   **Erro ao compilar**: Certifique-se de que salvou o arquivo com a extensão `.c` (para C) ou `.cpp` (para C++).
*   **Terminal fecha rápido**: Adicione `getchar();` ou `system("pause");` antes do `return 0;` para segurar a tela.