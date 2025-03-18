No C, a biblioteca padrão fornece várias cabeçalhos (`#include <...>`) que contêm funções e macros essenciais para diferentes funcionalidades. Aqui estão algumas das mais utilizadas:

1. **`#include <stdio.h>`** – Entrada e saída padrão
    - Funções: `printf()`, `scanf()`, `gets()`, `puts()`, `fopen()`, `fclose()`, `fprintf()`, `fscanf()`

1. **`#include <stdlib.h>`** – Gerenciamento de memória, conversões e sistema
    - Funções: `malloc()`, `calloc()`, `free()`, `atoi()`, `exit()`, `rand()`, `srand()`

1. **`#include <string.h>`** – Manipulação de strings
    - Funções: `strlen()`, `strcpy()`, `strncpy()`, `strcat()`, `strcmp()`, `strstr()`, `memcpy()`

1. **`#include <math.h>`** – Funções matemáticas
    - Funções: `sqrt()`, `pow()`, `sin()`, `cos()`, `tan()`, `fabs()`, `ceil()`, `floor()`

1. **`#include <ctype.h>`** – Manipulação de caracteres
    - Funções: `toupper()`, `tolower()`, `isalpha()`, `isdigit()`, `isspace()`

1. **`#include <time.h>`** – Manipulação de tempo e data
    - Funções: `time()`, `clock()`, `difftime()`, `strftime()`, `sleep()`

1. **`#include <stdbool.h>`** – Tipos booleanos (`true` e `false`)
    - Define: `bool`, `true`, `false`

1. **`#include <limits.h>`** – Limites dos tipos de dados
    - Define valores como `INT_MAX`, `INT_MIN`, `CHAR_MAX`, `LONG_MAX`

1. **`#include <float.h>`** – Limites dos tipos de ponto flutuante
    - Define valores como `FLT_MAX`, `DBL_MIN`, `LDBL_EPSILON`

1. **`#include <errno.h>`** – Tratamento de erros
	- Variável global `errno`, macros como `EIO`, `ENOMEM`, `EINVAL`