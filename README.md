# get_next_line

## About the Project
This function is capable to read each line of a file by calling it in loop from a main function.<br/>
You can set the buffer of your choice in [get_next_line.h](get_next_line.h) by changing `# define BUFF_SIZE 42`<br/>
For use it you need to include the header file and create a char pointer (who will store the line) and compile with get_next_line.c <br/>
You can, for example, call it in loop for read an entire file, like this: <br/>

```
#include <stdio.h>
#include "get_next_line.h"

int main(void)
{
	char *line;

	if ((fd = open(<your_file>, O_RDONLY)) == -1)
		return (-1);
	while (get_next_line(fd, &line) > 0)
	{
		printf("%s\n", line);
		free(line);
	}
	free(line);
	return (close(fd) == -1 ? -1 : 0);
}

``` 

## Curious ?
You can see the subject [here](get_next_line.fr.pdf)
