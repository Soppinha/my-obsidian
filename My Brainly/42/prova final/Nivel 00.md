### Ex 00

- Exer aff_a
```c
char ft_putchar(char c)
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
	retunr (*str);
}
```
