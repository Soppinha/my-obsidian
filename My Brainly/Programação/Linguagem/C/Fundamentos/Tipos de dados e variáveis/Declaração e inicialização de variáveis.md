Em C, uma **variável** é um espaço na memória que armazena um valor. Podemos **declarar** e **inicializar** variáveis de diferentes tipos.

## **Declaração de Variáveis**
---
```c title:"exemplo"
int idade;      // Variável do tipo inteiro
float altura;   // Variável do tipo float
char letra;     // Variável do tipo caractere
```

## **Inicialização de Variáveis**
Podemos atribuir um valor à variável **no momento da declaração**:

---
```c title:"exemplo"
int idade = 25;
float altura = 1.75;
char letra = 'A';
```

Também podemos **declarar várias variáveis do mesmo tipo na mesma linha**

---
```c title:"exemplo"
int a = 10, b = 20, c = 30;
```


## **Atribuição Posterior**
Podemos primeiro declarar a variável e depois atribuir um valor a ela:

---
```c title:"exemplo"
int idade;
idade = 25;
```
- ? Isso é útil quando o valor só será conhecido depois.


### Declaração de Variáveis com Modificadores
Podemos usar **modificadores** (`short`, `long`, `unsigned`, `signed`):

---
```c title:"exemplo"
unsigned int numero = 40000;   // Apenas valores positivos
long long int populacao = 8000000000; // Número grande
```


## **Variáveis Constantes (`const`)**
Para criar uma variável cujo valor **não pode ser alterado**, usamos `const`:

---
```c title:"exemplo"
const float PI = 3.14159;
```
- ? Se tentarmos alterar `PI`, o compilador dará um erro.


## 📝 **Resumo**

| Tipo     | Exemplo de declaração e inicialização |
| -------- | ------------------------------------- |
| `int`    | `int idade = 25;`                     |
| `float`  | `float altura = 1.75;`                |
| `double` | `double preco = 10.99;`               |
| `char`   | `char letra = 'A';`                   |
| `const`  | `const float PI = 3.14159;`           |
