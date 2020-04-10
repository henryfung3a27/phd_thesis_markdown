## Methodology

There are two ways to analyse a piece of program: statically and dynamically. 
Static analysis means we can open the program in a disassembler and/or decompiler.
Popular options are `Ghidra` and `IDA`. In this project, I used `Ghidra` for
static analysis because it is free and provides a decompiler. `IDA` has a free
version but it does not include a decompiler.

TODO: Add a screenshot of Ghidra interface

In dynamic analysis, we run the program and pause it at the beginning. Then we
proceed step by step which allows us to see the status of stack, memory, registers 
and instructions. This is also known as called *debugging*. Common softwares include 
`x64dbg`, `OllyDbg` and `WinDbg`. I used `x64dbg` and `OllyDbg` interchangeably in 
this project. 

TODO: screenshot of x64dbg

To debug a dll, we cannot run it directly. A dll (or library in general) is just 
a collection of functions. There is no `main` function as an entry point. In order
to debug a function in a library, we need to write a program which loads the library
and call the function. In this project, several programs, or *wrapper* programs, 
were written to fulfill different needs when debugging. For example, a basic wrapper
will call the function by its name directly. This wrapper is only useful if the 
function of interest is an *exported* function\footnote{An exported function is 
available to be called by its oridinal and/or name.}.

Another kind of wrapper I used is by embedding assembler instructions in the code. 
Different compilers have different convensions. In `msvc`\footnote{Microsoft Visual 
C++}, when a function tries to call a class member function (i.e. a *thiscall*
\footnote{A calling convention which is used for calling C++ non-static member 
functions.}), the compiler will first move the address of `this` into register `ecx`. 
Then it pushes all other parameters onto the stack before calling the function. In 
`g++`, it handles a *thiscall* similar to handling a *cdecl*\footnote{A calling 
convension in which the caller cleans the stack, and the parameters are passed in 
right-to-left order.}. The `this` pointer is pushed onto the stack as if it were the
first parameter in the function prototype.

TODO: Add code for basic wrapper

TODO: Add code for wrapper_offset
