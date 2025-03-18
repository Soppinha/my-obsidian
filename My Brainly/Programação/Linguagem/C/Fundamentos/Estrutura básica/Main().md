A função `main()` é o ponto de entrada de qualquer programa em C. Ela define onde a execução começa e pode retornar um valor para o sistema operacional.

## Tipos de declaração da `main()`
Em C, a `main()` pode ser declarada de diferentes formas:

### Com retorno `int` e sem argumentos (mais comum)
---
```c title:"exemplo"
int main() { return 0; }
```
- ~ O `return 0;` indica que o programa terminou com sucesso.
- ~ Se omitido, o compilador pode assumir `return 0;` automaticamente (a partir do C99).

### **Com retorno `int` e argumentos (`argc` e `argv`)**
---
```c title:"exemplo"
int main(int argc, char *argv[]) {
    printf("Número de argumentos: %d\n", argc);
    return 0;
}
```
- ~ `argc`: Número de argumentos passados na linha de comando.
- ~ `argv[]`: Array de strings contendo os argumentos.

### Com `void main()` (não recomendado!)
---
```c title:"exemplo"
void main() {
    printf("Isso pode funcionar, mas não é padrão!\n");
}

```

- ! Problemas:
	Em C, `main()` deve retornar um `int`.
	Pode não ser compatível com todos os compiladores.
