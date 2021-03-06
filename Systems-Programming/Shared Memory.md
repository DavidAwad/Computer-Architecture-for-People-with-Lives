# Shared Memory

So we know about how to use means of synchronization for our processes to make sure nobody steps on anyone else. 

This is convenient for things like multithreading, but what about if we wanted to share a data structure between processes? 

The way you can do this is by using a construct called **shared memory**. 

Here's how it works at a high level; you reserve a block of memory that essentially is not associated with a process, but with a unique *key*. 

You use the key and the operating system gives you a pointer to the beginning of that block of memory. 

Here's a small example. 
```C
	key_t  key;
	int  shmid;
	char *p;
	int size = 4096;
	
	// create a key, ftok just does some hashing to create a secure string. 
	key = ftok( "example.txt", 42 ); 
	// shmget gives us our id
	shmid = shmget( key, size, 0666 | IPC_CREAT | IPC_EXCL ) ;
	// Successful creation of shared memory segment.  Segment is filled with zeros.
	printf( "Process %d puts message in created shared memory segment attached at address %#x.\n", getpid(), p + sizeof(int) );
	// shmat works just like `malloc()` except requiring a key for memory  
	p = (char *)shmat( shmid, 0, 0 );
	// Acquired shared memory segment.  Has to wait until segment is properly initialized by creator.
	printf( "Process %d gets message from shared memory segment attached at address %#x.\n", getpid(), p );
	// do any kind of work, finish with lock and detach from shared memory. 
	shmdt(p);
```

* man page for [ftok](http://www.lehman.cuny.edu/cgi-bin/man-cgi?ftok+3)
* You can see a full example inside of [shmget.c](https://github.com/DavidAwad/Computer-Architecture-for-People-with-Lives/blob/master/Systems-Programming/shmget.c). 

