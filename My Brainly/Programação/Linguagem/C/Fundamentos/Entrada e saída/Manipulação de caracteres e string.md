O C possui diversas funções para **ler e exibir caracteres e strings**. As principais são:

| Função      | Descrição                                     |
| ----------- | --------------------------------------------- |
| `getchar()` | Lê **um único caractere** do usuário          |
| `putchar()` | Exibe **um único caractere** na tela          |
| `gets()`    | Lê uma **string inteira** (⚠ não recomendado) |
| `puts()`    | Exibe uma **string inteira** na tela          |

## **Lendo e Exibindo Caracteres: `getchar()` e `putchar()`**
Essas funções são usadas para **manipular caracteres individuais**.

---
```c title:"exemplo"
#include <stdio.h>

int main() {
    char letra;

    printf("Digite um caractere: ");
    letra = getchar(); // Lê um único caractere

    printf("Você digitou: ");
    putchar(letra); // Exibe o caractere na tela

    return 0;
}
```
- s **Observações:**
	O `getchar()` aguarda a entrada de um caractere e **lê também o ENTER**, que pode causar problemas em leituras subsequentes. 
	O `putchar()` recebe um caractere e o exibe.

## **Lendo e Exibindo Strings: `gets()` e `puts()`**
A função `gets()` lê uma **linha inteira** de texto, enquanto `puts()` exibe uma string.

---
```c title:"exemplo"
#include <stdio.h>

int main() {
    char nome[50]; // String de até 49 caracteres + '\0'

    printf("Digite seu nome: ");
    gets(nome); // ⚠ NÃO RECOMENDADO, pois pode causar falhas de segurança

    printf("Seu nome é: ");
    puts(nome); // Exibe a string na tela

    return 0;
}
```

- ! **Atenção:**  
	A função `gets()` **não é segura** pois não limita o tamanho da entrada, podendo causar **estouro de buffer**.

##### **Alternativa mais segura:** Use `fgets()`:
---
```c title:"exemplo"
fgets(nome, 50, stdin); // Lê no máximo 49 caracteres
```

## **Resumo**

|Função|Uso|
|---|---|
|`getchar()`|Lê **um caractere**|
|`putchar()`|Exibe **um caractere**|
|`gets()`|Lê **uma string inteira** (⚠ NÃO RECOMENDADO)|
|`puts()`|Exibe **uma string inteira**|

- ok **Melhores práticas:**
	Prefira `fgets()` ao invés de `gets()`.
	Para caracteres únicos, use `getchar()` e `putchar()`.