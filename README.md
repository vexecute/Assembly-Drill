# Assembly

When you try to run the C code, it is read by the compiler. This compiler will convert all the instructions into op codes (operation code). Understanding the op codes is very difficult because every executable has thousands of op codes. That is why assembly language was created. This converts the compiled instructions into human readable language.

⇒ 32 and 64 bit architecture

⇒ We’ll be focusing on 32bit also called as x86 architecture (since it uses 8086 microprocressor)

Every C program has 4 main components ⇒ Basic elements of executable:

- `**heap**` - designed for manual memory allocation (memory is allocated in heap when functions like malloc and calloc is called as well as when global or static variables are declared)
- **`stack` -** a data structure that are compiled with elements which can be added or removed using push(add element to the top or stack) or pop(remove an element from the top of stack). Elements that are higher in the stack have lower address than those in the bottom of the stack. Whenever a function is called it is setup as what is called stack frame. All the local variables of the function are stored in a stack frame. Now comes these two registers `**ebp**` and **`esp`**. `**ebp**`(e base pointer) contains the base address of the current stack frame whereas **`esp`** (e stack pointer) contains the stack pointer of the top element of the stack frame. All addresses outside the current stack frame are called as junk addresses.

## Example:

![Untitled](Assembly%200988f4693e5c41c0a8d630a7cb805ca7/Untitled.png)

- `**registers` -** used to store addresses and values (anything that can be represented as 8bytes or less). In x86 arch there are 6 general purpose registers `**eax,ebx,ecx,edx,esi,edi`** and there three reserved registers `**ebp,esp,eip**`

- `**instructions` -** assembly instructions which are of format

                      operation arg1 (with one argument) 

                      operation arg1, arg2 (with two arguments)

             ⇒ **`mov` -** move instruction

![Untitled](Assembly%200988f4693e5c41c0a8d630a7cb805ca7/Untitled%201.png)

              ⇒ ****`**add` -** adds two arguments and stores it in the first argument.

              ⇒ **********`sub` -** similar to add but it subtracts

              ⇒ ********`push/pop` -** used for pushing and removing elements from the stack

![Untitled](Assembly%200988f4693e5c41c0a8d630a7cb805ca7/Untitled%202.png)
