#C

So let's talk a little bit about how C works. 

C is a compiled language. It's linked and compiled into a machine code executable that can be called from the shell. 


This book assumes a bit of knowledge about higher level knowledge about high level languages like Java or C#, or even higher languages like Python or even Ruby.


Let's start with the simple stuff, enjoy the unsurprising hello world. 

```C
#include <stdio.h>

main()
{
  printf("Hello, world!\n");
  return 0;
}
```

The means of importing packages in C, is through `#include` statements where `<library.h>` will typically be the name of the C library you want to use in your programs. 

C uses a main function that is called on execution of the program from the shell. In this case it's only going to print `Hello World!`. 

## Structs

The Next Question is **objects** ... They don't exist! ... also classes don't exist either.

The answer is in fact done through something called *structs*. Bascially an opaque object that you can add any type of data. 

```C
struct node {
  int weight; 
  int value;
} ;
```

