Em C, os **tipos primitivos** são os tipos básicos de dados usados para armazenar valores na memória. Os principais são:

### **`int` (inteiro)**
- Armazena números inteiros (positivos e negativos).
- Geralmente ocupa **4 bytes** (32 bits) na maioria dos sistemas.
- Valores típicos: `-2147483648` a `2147483647` (`INT_MIN` e `INT_MAX` em `<limits.h>`).
---
```c title:"exemplo"
#include <stdio.h>

int main() {
    int idade = 25; // Variável do tipo inteiro
    printf("Idade: %d\n", idade);
    return 0;
}
```
- ~ **Formato no `printf()`**: `%d` ou `%i`


### **`float` (ponto flutuante de precisão simples)**
- Armazena números com casas decimais.
- Ocupa **4 bytes**.
- Precisão de **aproximadamente 6 a 7 dígitos significativos**.
---
```c title:"exemplo"
#include <stdio.h>

int main() {
    float altura = 1.75;
    printf("Altura: %.2f\n", altura); // Duas casas decimais
    return 0;
}
```
- ~ **Formato no `printf()`**: `%f`


### **`double` (ponto flutuante de precisão dupla)**
- Similar ao `float`, mas com **mais precisão**.
- Ocupa **8 bytes**.
- Precisão de **aproximadamente 15 a 16 dígitos significativos**.
---
```c title:"exemplo"
#include <stdio.h>

int main() {
    double pi = 3.141592653589793;
    printf("Valor de pi: %.15lf\n", pi);
    return 0;
}
```
- ~ **Formato no `printf()`**: `%lf`



### **`char` (caractere)**
- Armazena um **único caractere**.
- Ocupa **1 byte**.
- Representado por **aspas simples (`'A'`)**.
---
```c title:"exemplo"
#include <stdio.h>

int main() {
    char letra = 'A';
    printf("Letra: %c\n", letra);
    return 0;
}
```
- ~ **Formato no `printf()`**: `%c`

- ! **Strings em C** são arrays de `char`, terminados por `'\0'`:
---
```c title:"exemplo"
char nome[] = "Sofia"; // String (array de char)
```


## Tabela comparativa

| Tipo     | Tamanho (bytes) | Intervalo de valores           | Formato no `printf()` |
| -------- | --------------- | ------------------------------ | --------------------- |
| `int`    | 4               | -2,147,483,648 a 2,147,483,647 | `%d` ou `%i`          |
| `float`  | 4               | ~ ±3.4E-38 a ±3.4E+38          | `%f`                  |
| `double` | 8               | ~ ±1.7E-308 a ±1.7E+308        | `%lf`                 |
| `char`   | 1               | -128 a 127 (`signed char`)     | `%c`                  |
