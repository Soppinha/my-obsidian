Usados para comparar valores e retornam `true (1)` ou `false (0)`.


| Operador | Descrição      | Exemplo (`a = 10, b = 3`) | Resultado        |
| -------- | -------------- | ------------------------- | ---------------- |
| `==`     | Igual          | `a == b`                  | `0` (falso)      |
| `!=`     | Diferente      | `a != b`                  | `1` (verdadeiro) |
| `>`      | Maior que      | `a > b`                   | `1`              |
| `<`      | Menor que      | `a < b`                   | `0`              |
| `>=`     | Maior ou igual | `a >= b`                  | `1`              |
| `<=`     | Menor ou igual | `a <= b`                  | `0`              |

---
```c title:"exemplo"
if (idade >= 18) {
    printf("Você é maior de idade.\n");
} else {
    printf("Você é menor de idade.\n");
}
```
