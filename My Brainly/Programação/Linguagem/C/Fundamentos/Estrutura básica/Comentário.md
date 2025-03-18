Em C, há dois tipos principais de comentários:

1. **Comentários de linha única** (`//`)
2. **Comentários de múltiplas linhas** (`/* ... */`)

## Comentários de linha única (`//`)
Os comentários de linha única começam com `//` e continuam até o final da linha.

---
```c title:"exemplo"
#include <stdio.h>

int main() {
    // Exibe uma mensagem no console
    printf("Olá, mundo!\n");  
    return 0;
}
```
- ok Útil para explicar trechos curtos de código.

## Comentários de múltiplas linhas (`/* ... */`)
Usados para comentários mais longos ou para desativar blocos de código.

---
```c title:"exemplo"
#include <stdio.h>

int main() {
    /* Este é um comentário
       de múltiplas linhas.
       Ele pode abranger várias linhas. */
    printf("Comentário de múltiplas linhas!\n");

    return 0;
}

```



- ! **Atenção**: Comentários `/* */` não podem ser aninhados!  Ou seja, o código abaixo causaria erro:
---
```c title:"exemplo"
/* Comentário externo
    /* Comentário interno */
*/
```



- ? Para desativar um bloco de código, use `#if 0 ... #endif`:
---
```c title:"exemplo"
#if 0
    printf("Este código não será compilado.\n");
#endif
```

## Boas práticas ao usar comentários 
- ok Use comentários para explicar o **"porquê"** do código, não apenas o **"como"**.  
- ok Evite comentários óbvios.  
- ok Mantenha os comentários atualizados.  
- ok Use um estilo consistente.