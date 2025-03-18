Em C, os **modificadores de tipo** (`short`, `long`, `signed`, `unsigned`) ajustam o **tamanho** e o **intervalo de valores** das variáveis numéricas (`int` e `char`).

## **`short` (inteiro curto)**
- Reduz o tamanho de um `int` (geralmente **2 bytes** em sistemas de 32/64 bits).
- Intervalo típico: `-32.768` a `32.767`.
---
```c title:"exemplo"
#include <stdio.h>

int main() {
    short int idade = 25;
    printf("Idade: %d\n", idade);
    return 0;
}
```
- ~ **Formato no `printf()`**: `%hd`


## **`long` (inteiro longo)**

- Aumenta o tamanho de um `int` (geralmente **4 ou 8 bytes**, dependendo do compilador/sistema).
- Intervalo: **depende da arquitetura** (mínimo `-2.147.483.648` a `2.147.483.647` para `long int` de 4 bytes).
---
```c title:"exemplo"
#include <stdio.h>

int main() {
    long int populacao = 8000000000; // 8 bilhões
    printf("População mundial: %ld\n", populacao);
    return 0;
}
```
- ~ **Formato no `printf()`**: `%ld`

- ? `long long` (inteiro ainda maior, normalmente **8 bytes**)
---
```c title:"exemplo"
long long int estrelas = 9223372036854775807; // Maior valor de long long
printf("Número de estrelas: %lld\n", estrelas);
```
- ~ **Formato no `printf()`**: `%lld`

## **`unsigned` (somente valores positivos)**

- Remove o sinal (`+` ou `-`), permitindo **apenas valores positivos**.
- **Dobra o valor máximo permitido**, pois todo o espaço de bits é usado para valores positivos.
---

```c title:"exemplo"
#include <stdio.h>

int main() {
    unsigned int numero = 4000000000; // Máximo para 4 bytes
    printf("Número positivo: %u\n", numero);
    return 0;
}
```
- ~ **Formato no `printf()`**: `%u`
- ? Pode ser usado com `short`, `long` e `char`!
---
```c title:"exemplo"
unsigned short int idade = 30;     // Somente positivos
unsigned long int dinheiro = 99999;
unsigned char letra = 'A';         // Armazena 0 a 255
```


## **`signed` (permite valores negativos e positivos)**

- Padrão para `int` e `char`, então **não precisa ser especificado**.
- Exemplo: `signed int` é o mesmo que `int`.
---
```c title:"exemplo"
signed int temperatura = -10;  // Mesma coisa que "int temperatura = -10;"
```
- ~ **Formato no `printf()`**: `%d`
- ? Pode ser útil para `char`, pois `char` pode ser **signed** ou **unsigned** dependendo do compilador:
---
```c title:"exemplo"
signed char a = -100;   // Pode armazenar valores negativos (-128 a 127)
unsigned char b = 200;  // Apenas valores positivos (0 a 255)
```


## 📝 **Resumo: Tamanhos e Intervalos**

| Tipo                 | Tamanho (bytes) |      Intervalo de valores      |
| -------------------- | --------------- |:------------------------------:|
| `short int`          | 2               |        -32.768 a 32.767        |
| `unsigned short`     | 2               |           0 a 65.535           |
| `int`                | 4               | -2.147.483.648 a 2.147.483.647 |
| `unsigned int`       | 4               |       0 a 4.294.967.295        |
| `long int`           | 4 ou 8          |       Depende do sistema       |
| `unsigned long`      | 4 ou 8          |        Apenas positivos        |
| `long long int`      | 8               | -9 quintilhões a 9 quintilhões |
| `unsigned long long` | 8               |       0 a 18 quintilhões       |
| `signed char`        | 1               |           -128 a 127           |
| `unsigned char`      | 1               |            0 a 255             |

### 💡 **Dicas: Quando usar cada um?**
- ok **Use `unsigned`** quando você tem certeza de que o número **nunca será negativo** (ex: idades, quantidades).  
- ok **Use `long` ou `long long`** quando precisar armazenar números **muito grandes** (ex: população mundial).  
- ok **Use `short`** para economizar memória em sistemas embarcados ou com restrições.  
- ok **Prefira `int`** para a maioria dos casos, pois é mais otimizado para a CPU.
