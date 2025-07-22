
```c
#include <libft.h>

void *ft_memchr(const void *s, int c, size_t n)
{
	size_t i;
	unsigned char *str;
	unsigned char charac;

	i = 0;
	str = (unsigned char *) s;
	charac = (unsigned char) c;
	while (i < n)
	{
		if (str[i] == charac)
	{

return ((void *) &str[i]);

}

}

return (NULL);

}

```
