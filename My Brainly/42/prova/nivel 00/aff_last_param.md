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

void ft_last_param(char *str)
{
	int i;
	i = 0;

	while(str[i] != '\0')
	{
		ft_putchar(str[i]);
		i++;
	}
	pt_putchar('\n');
}

int main(int argc,  **argv)
{
	if(argc >= 2)
	{
		ft_last_param(argv[arrgc - 1]);
	}
	else
	{
		ft_putchar('\n');
	}

	return 0;
}
```
