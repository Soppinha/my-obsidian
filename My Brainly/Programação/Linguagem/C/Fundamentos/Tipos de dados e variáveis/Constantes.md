As **constantes** em C são valores que **não podem ser alterados após a atribuição**. Existem duas formas principais de definir constantes:

- **`const`** → Usa uma variável constante, respeitando o tipo de dado.
- **`#define`** → Usa uma **macro** para definir um valor fixo, sem tipo específico.

## **Constantes com `const`**
O **modificador `const`** torna uma variável **imutável** após sua inicialização.

---
```c title:"exemplo"
#include <stdio.h>

int main() {
    const float PI = 3.14159;  // Definição de constante
    const int ANO_NASCIMENTO = 2000;

    printf("PI: %.5f\n", PI);
    printf("Ano de nascimento: %d\n", ANO_NASCIMENTO);

    // PI = 3.14;  // ❌ ERRO! Constantes não podem ser alteradas
    return 0;
}
```

##### **Vantagens do `const`:**  
- ok Mantém o tipo da variável.  
- ok Usa menos memória do que `#define`.  
- ok O compilador pode otimizar melhor.


## **Constantes com `#define`**
O **`#define`** define um nome para um **valor fixo**.

- **Não ocupa espaço na memória**, pois é substituído pelo compilador.
- **Não tem tipo**, então pode causar erros inesperados.
- Normalmente, o nome das constantes `#define` é escrito em **maiúsculas**.

---
```c title:"exemplo"
#include <stdio.h>

#define PI 3.14159
#define ANO_NASCIMENTO 2000

int main() {
    printf("PI: %.5f\n", PI);
    printf("Ano de nascimento: %d\n", ANO_NASCIMENTO);

    // PI = 3.14;  // ❌ ERRO! Não é uma variável, é um valor fixo
    return 0;
}
```

##### **Vantagens do `#define`:**  
- ok Substituição direta no código (sem alocação de memória).  
- ok Útil para **definir valores fixos em todo o código**.

##### **Desvantagens do `#define`:**
- no **Não tem tipo** → Pode gerar erros de compatibilidade.
- no **Não pode ser depurado** facilmente, pois é substituído antes da compilação.


## **Diferenças entre `const` e `#define`**

|Característica|`const`|`#define`|
|---|---|---|
|**Tem tipo?**|✅ Sim|❌ Não|
|**Ocupa memória?**|✅ Sim|❌ Não|
|**Depuração**|✅ Sim|❌ Não|
|**Modificável?**|❌ Não|❌ Não|
|**Substituição no código?**|❌ Não|✅ Sim|

💡 **Quando usar `const`?**  
- ok Quando precisar de um **tipo específico** (ex: `int`, `float`, `char`).

💡 **Quando usar `#define`?**  
- ok Para **valores fixos** que não precisam de um tipo (ex: PI, mensagens, caminhos de arquivos)