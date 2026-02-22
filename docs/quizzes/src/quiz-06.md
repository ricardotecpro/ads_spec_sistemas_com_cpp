# Quiz 06 - Arrays e Strings 🧵

1. Qual o índice do primeiro elemento de um array no C++?
    - [x] 0
    - [ ] 1
    - [ ] -1
    - [ ] Aleatório
    > Explicação: C++ usa indexação baseada em zero para todos os arrays e containers.

2. Como acessamos o tamanho de um objeto `std::string`?
    - [ ] s.size
    - [x] s.length() ou s.size()
    - [ ] sizeof(s)
    - [ ] s.count()
    > Explicação: A classe `string` possui métodos específicos para informar o total de caracteres.

3. O que é uma C-Style String?
    - [ ] Uma string escrita em CSS
    - [ ] Um objeto da classe string
    - [x] Um array de char terminado por `\0` (nulo)
    - [ ] Um código secreto
    > Explicação: É a forma legada do C de tratar textos como simples vetores de caracteres.

4. Qual operador é usado para concatenar duas `std::string`?
    - [ ] .concat()
    - [x] +
    - [ ] &
    - [ ] ,
    > Explicação: O C++ sobrecarrega o operador `+` para facilitar a união de strings.

5. O que acontece se acessarmos um índice fora do limite do array (ex: `arr[10]` num array de 5)?
    - [ ] O compilador avisa e corrige
    - [ ] O valor 0 é retornado automaticamente
    - [x] Comportamento indefinido (pode travar ou ler lixo da memória)
    - [ ] O array aumenta de tamanho sozinho
    > Explicação: C++ prioriza performance e não faz checagem de limites (bounds checking) em arrays nativos.

6. Como declaramos uma matriz (array bidimensional) de 3 linhas e 2 colunas?
    - [ ] int m[3, 2];
    - [x] int m[3][2];
    - [ ] int m(3)(2);
    - [ ] array m[3, 2];
    > Explicação: Matrizes são representadas por múltiplos pares de colchetes.

7. Para que serve o método `getline()`?
    - [ ] Para ler apenas números
    - [x] Para ler uma linha inteira, incluindo espaços
    - [ ] Para pular uma linha no console
    - [ ] Para apagar o conteúdo de uma string
    > Explicação: `std::getline` contorna a limitação do `cin >>`, que para de ler ao encontrar o primeiro espaço.

8. Qual a diferença entre `'A'` (aspas simples) e `"A"` (aspas duplas)?
    - [ ] Não há diferença
    - [x] 'A' é um char, "A" é uma string (array)
    - [ ] "A" consome menos memória
    - [ ] 'A' é para números e "A" para letras
    > Explicação: ' ' define um caractere único, enquanto " " define uma sequência terminada em `\0`.

9. O que o método `s.substr(0, 3)` faz?
    - [ ] Apaga o texto
    - [x] Retorna uma nova string com os 3 primeiros caracteres
    - [ ] Substitui caracteres
    - [ ] Converte para maiúsculo
    > Explicação: `substr` extrai uma parte da string original.

10. Como percorremos um array de forma moderna (C++11)?
    - [ ] loop(arr) {}
    - [x] for(int x : arr) {} (Range-based for)
    - [ ] foreach(arr as x) {}
    - [ ] while(arr.next()) {}
    > Explicação: O range-based for é mais seguro e legível para percorrer coleções completas.