#C

So let's talk a little bit about how C works. This book assumes a bit of knowledge about higher level knowledge about high level languages like Java or C#, or even higher languages like Python or even Ruby. So I'm just going to give a quick overview of how to use C if you're farmiliar with other high level languages. 

C is a compiled language. It's linked and compiled into a machine code executable that can be called from the shell. 

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

Main typically returns 0 on success, and reports a 1 for error. 

## Pointers

```C
int main(){
  char *myString[100] ; 
  return 0; 
}
```
C uses a construct called pointers to do most of it's references. 

It also doesn't actually have strings. It only really has character pointers, basically an array of `char`s. 

## Structs

The Next Question is **objects**, in C they don't exist! ... also classes don't exist either.

The answer is in fact done through something called *structs*. Bascially an opaque object that you can fill with any data type. 

```C
struct node {
  int weight; 
  int value;
} ;
```

So the way you deal with these structs to create fancy things like lists and graphs is by using functions that simply take structs.
```C
// best way to fake having classes in C
void setNode(node *temp, int w , int v){
  temp->weight = w;
  temp->value = v;
  return 0;
}
```
It's not terribly convenient but it does help 


## Malloc
