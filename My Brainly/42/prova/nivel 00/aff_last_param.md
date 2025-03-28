## Simples
```c
#include <unistd.h>

void ft_putchar(char c)
{
	write(1, &c, 1);
	write(1, "\n", 2);
}

int main(void)
{
	putchar('c');
	return 0;
}
```

## Médio
```c
void ft_putchar(char c)
{
	
}

int main(void)
{
	
}
```

## Difícil
```c
#include <unistd.h>

void ft_putchar(char c)
{
	write(1, &c,1);
}

char ft_first_param(char *str)
{
	
}

int main(int argc,  **argv)
{
	
}
```
