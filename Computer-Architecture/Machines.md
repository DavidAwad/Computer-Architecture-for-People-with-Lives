# The Modern Computer

So this is our first chapter, an introduction to how a typical machine works. 

Let's start with the literal. 


Your computer has a couple of fundamental pieces. Most of this should be straightforward but... whatever. 

So as a programmer, these are the parts of the computer that matter to you. 


| Parts |  |
|:-------:|:------:|
| Central Processing Unit | The Processor, basically the way your computer does all the math. | 
| Hard Drive | The place where all of your information is stored |
| **RAM** | Random Access Memory, basically a faster hard drive |


## CPU

So the CPU is it's own book altogether, but here's what I can tell you. 

The CPU, often just called the processor, is the component that contains the microprocessor. That microprocessor is the heart of all the PC's operations, and the performance of both hardware and software rely on the processor's performance. Intel and AMD are the largest CPU manufacturers for PCs, though you'll find others on the market, too. The two common CPU architectures are 32-bit and 64-bit, and you'll find that certain software relies on this architecture distinction.


## The Hard Drive 

The hard drive is also somewhat straightforward, 

You can think of it as a huge, huge, array of cylinders that contain 1's or 0's. Binary values that, if you have enough of them, resemble data structures to the operating system, and thats exactly what it uses them for. 

If you want to get a real engineering level understanding of how it works, you can read more about it [here](http://www.explainthatstuff.com/harddrive.html). 


## RAM

Even the fastest processor needs a buffer to store information while it's being processed. The RAM is to the CPU as a countertop is to a cook: It serves as the place where the ingredients and tools you're working with wait until you need to pick up and use them. 

For example, reads from disk might take 600 milliseconds where reads from memory might cost 200 nanoseconds. The faster you can read information from disk, the faster every process on the operating system will potentially be able to be. 
Building RAM thats as fast as possible makes for a very interesting engineering problem that has nothing to do with the goal of this book :D 


