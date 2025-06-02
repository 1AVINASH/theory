## Metaclass

## Garbage Collection

## ASGI (Asynchronous server gateway interface)
* It's a specification that defines how web servers and frameworks communicate in Python, particularly when dealing with asynchronous operations
* It's a standard interface that enables web applications to handle multiple requests concurrently and efficiently, especially for scenarios like WebSockets and other real-time features. 
* It defines how web servers and web applications interact, specifying how requests are passed and responses are sent back. 
* It's designed for asynchronous programming, allowing web applications to handle multiple requests without blocking. 


## Libraries
### cmd
* A Cmd instance or subclass instance is a line-oriented interpreter framework. 
* The cmd module is mainly useful for building custom shells that let a user work with a program interactively.
* It’s useful as a superclass of an interpreter class you define yourself in order to inherit Cmd’s methods and encapsulate action methods.
* The cmd loop is entirely isolated from the OS shell. It's just a Python loop reading input, parsing it, and calling Python methods in your class.
* Cmd.cmdloop(intro=None): Repeatedly issue a prompt, accept input, parse an initial prefix off the received input, and dispatch to action methods, passing them the remainder of the line as argument.

### Socket
* Used for low level network communication (TCP, UDP)
* Takes the address family to be used as input (INET for ivp4, and INET6 for ipv6)
* Takes the type of connection to be created. SOCK_STREAM for tcp, and SOCK_DGRAM for udp


## Frameworks
### FastApi
A modern, high-performance web framework for building APIs with Python. It's designed with asynchronous programming in mind, making it extremely fast and able to handle multiple requests concurrently. Key components that power FastAPI include Uvicorn, Starlette, Swagger UI, and Pydantic

* Starlette: A lightweight ASGI framework that handles the core HTTP operations, including routing, middleware, and WebSockets support.
* Starlette provides the low-level tools that FastAPI uses to manage HTTP requests, making it a stable and performant foundation for building web applications.


* Uvicorn: An ASGI server designed to serve asynchronous applications


### AsyncIO vs Threading
* Threading creates new threads which run in parallel (they don't run parallely in Python because of GIL). This involves thread creation which has an overhead
* Asyncio uses context switching to perform tasks in the same thread. 
* Threading performs preemptive scheduling (which means that the OS handles the thread scheduling). Meanwhile asyncio uses co-operative scheduling which means the program has to yield control of the thread to the main thread which will handle the scheduling/processing. 
