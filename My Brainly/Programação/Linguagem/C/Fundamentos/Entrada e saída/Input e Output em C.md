As funções `printf()` e `scanf()` são usadas para **exibir** e **ler dados** no C. Elas fazem parte da biblioteca `<stdio.h>`.

## **`printf()` - Exibir dados na tela**
A função `printf()` é usada para **imprimir** textos e variáveis na saída padrão (tela).

---

```c title:"exemplo"
#include <stdio.h>

int main() {
    int idade = 25;
    float altura = 1.75;
    char inicial = 'A';

    printf("Idade: %d anos\n", idade);
    printf("Altura: %.2f metros\n", altura);
    printf("Inicial do nome: %c\n", inicial);

    return 0;
}
```

##### **Formatos (`%`):**

|Tipo|Especificador|
|---|---|
|Inteiro|`%d` ou `%i`|
|Ponto flutuante (float)|`%f`|
|Duplo (double)|`%lf`|
|Caractere|`%c`|
|String|`%s`|

##### 💡**Dicas:**
- `\n` → Quebra de linha
- `%.2f` → Define casas decimais

## **`scanf()` - Ler entrada do usuário**
A função `scanf()` é usada para **ler valores do teclado**.

---

```c title:"exemplo"
#include <stdio.h>

int main() {
    int idade;
    float altura;
    char inicial;

    printf("Digite sua idade: ");
    scanf("%d", &idade);

    printf("Digite sua altura: ");
    scanf("%f", &altura);

    printf("Digite a inicial do seu nome: ");
    scanf(" %c", &inicial);  // O espaço antes de %c evita problemas com ENTER

    printf("\nDados inseridos:\n");
    printf("Idade: %d anos\n", idade);
    printf("Altura: %.2f metros\n", altura);
    printf("Inicial do nome: %c\n", inicial);

    return 0;
}
```
- ? **O operador `&` (E comercial) é necessário para armazenar o valor lido na variável.**

## ❗**Cuidados com `scanf()`**
 - no **Problema comum com `%c`**  
	Quando `scanf("%c", &variavel)` é usado após `scanf("%d")` ou `scanf("%f")`, pode haver um problema com a leitura do ENTER.

- ok **Solução:**  
	Coloque um **espaço antes de `%c`**:
---

```c title:"exemplo"
scanf(" %c", &letra);
```

- no **Problema com leitura de strings (`%s`)**  
	Se for ler uma string, `scanf("%s", nome);` lê apenas **uma palavra**.

- ok **Solução:**  
	Use `scanf("%[^\n]s", nome);` para ler uma frase.  
	Ou use `fgets()` para evitar problemas com o buffer.