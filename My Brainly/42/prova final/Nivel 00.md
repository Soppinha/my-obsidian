### Ex 00

- Exer aff_a

```c
#include <unistd.h>

void ft_putchar(char c)
{
	write(1, &c, 1);
}

char ft_aff_a(char *str)
{
	int i;
	
	i = 0;
	while(str[i] != '\0')
	{
		if(str[i] == 'a')
		{
			ft_putchar('a');
		}
		i++;
	}
	ft_putchar('\n');
	return (*str);
}

int		main(int argc, char **argv)
{
	if (argc == 2)
	{
		ft_aff_a(argv[1]);
	}
	else
	{
		ft_putchar('a');
		ft_putchar('\n');
	}
	return (0);
}
```


---
- Exer aff_first_param

```c
#include <unistd.h>

char ft_fisrt_param(char *str)
{
	int i;

	i = 0;
	while(str[i] != '\0')
	{
		write(1, &str[i], 1);
		i++;
	}
	write(1, '\n', 1);
	return (*str);
}

int		main(int argc, char **argv)
{
	if (argc >= 2)
	{
		ft_first_param(argv[1]);
	}
	else
	{
		write(1, '\n', 1);
	}
	return (0);
}
```

---
- Exer aff_last_param

```c
#include <unistd.h>

char ft_last_param(char *str)
{
	int i;

	i = 0;
	while(str[i] != '\0')
	{
		write(1, &str[i], 1);
	}
	write(1, '\n', 1);
	return (*str);
}

int main(int argc, char **argv)
{
	if (argc < 2) 
	{ 
		write(1, '\n', 1);
	} 
	else 
	{ 
		ft_last_param(argv[argc - 1]); 
	}
	 return (0); 
}
```
---
- Exer aff_z

```c
void ft_putchar(char c)
{
	
}
```


---
- Exer maff_alpha

---
- Exer maff_revalpha

---
- Exer only_z


---
- Exer strlen_sh