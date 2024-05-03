# GoProgramming
Here is where I will be practising and uploading all my updates in Golang

Why should you learn go? What's unique and good about the Go language?
### Advantages of Go:
1. Code runs fast.
2. Garbage collection - Similar languages that run fast like Go does, do not use a garbage collector. So this is a really useful feature.
3. Simpler obejcts - Go is essentially object oriented, but it has this concept of objects, the object orientation is a little simplified as compared to other languages.
4. Concurrency is efficient.

### Software Translation
Let's looks at three very broad categories of languages:

**Machine Level Language (MLL)**
1. CPU instructions represented in binary - like say 11110000 could be the opcode for ADD.
2. Lowest level language.
3. Directly executed on the CPU; on the processor.
4. Instructions are very, very straightforward and simple - like add(might add two register contents and put it into another register) or multiply.

**Assembly Level Language (ALL)**
1. Basically machine language, almost a 1:1 mapping to machine language.
2. Same complexity as machine level language but easier to read.
3. CPU instructions with mnemonics - like ADD for doing addition.

**High Level Language (HLL)**
1. Language that essentially humans commonly use to program in.
2. Much easier to use than assembly language or machine language.
3. Provide you with lots of abstractions that any program would be used to:
   - variables (MLL and ALL do not use variables)
   - type (There's no idea of a type or anything like that in ALL or MLL)
   - if statements (MLL and ALL have conditional branches but they are much harder to use)
   - for loops (same as if statements)
  

All software must be translated into the machine language of the processor. Since processor does not understand HLL. It only knows its own MLL. So, in order for the code to execute on the processor, it has to be first translated into the machine language of the processor. So, even if it's C, Python, Java whatever it is, has to be translated. So, there is this software translation step that has to go on. This can go on in two ways: Compilation or Interpretation.
1. **Compiled Language** - language where the translation from high-level language to machine code happens one time before you execute the code, like in C, C++, Go, Java partially. The compiled executable is basically machine language code plus other stuff, but it's basically machine language code.
2. **Interpreted Language** - instructions are translated while the code is executed. It adds time to the execution because every time you see an instruction, and say Python, that code, that instruction has to be translated into machine code on a fly, and that takes a certain amount of time just to do that translation. So, in addition to actually executing the instruction, you've got to do this translation from the instruction into the equivalent machine code, so that slows you down.

> Mentioned Java partially because Java gets compiled into a bytecode which is then interpreted at runtime.

### Efficiency vs Ease-of-use
1. Compiled code is generally faster to execute, that's because you don't have to do the translation every time you run the code.
2. Interpreters make coding easier. (It can help you handle things that a programmer doesn't want to handle)
   - Manage memory automatically. (getting rid of variables and other pieces of data when you're not using them)
3. Go is a good compromise
   - Compiled Language
   - Garbage Collection (one if the features of interpreted language)
     - where should memory be allocated?
     - when can memory be deallocated?
   - Slows down execution a bit but it's got an efficient garbage collector
> Manual memory management is hard. Deallocate memory too early and you end up having false memory accesses. Deallocate memory too late and you're wasting memory (memory leak)
