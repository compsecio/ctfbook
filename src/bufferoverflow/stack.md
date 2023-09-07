# The Stack

With a colleague, sketch out how the following items would be arranged on the stack.

Assume the following:
* We are dealing with a 32-bit, little endian processor. 
* int's are four bytes each


Code:
```C
int w = 1;
int x = 2;
int y = 3;
int z = 4;
int int_array[4] = {5,6,7,8};
```



---



You can check your answer by looking at the following output from gcc on the above code.

```
        mov     DWORD PTR [rbp-4], 1
        mov     DWORD PTR [rbp-8], 2
        mov     DWORD PTR [rbp-12], 3
        mov     DWORD PTR [rbp-16], 4
        mov     DWORD PTR [rbp-32], 5
        mov     DWORD PTR [rbp-28], 6
        mov     DWORD PTR [rbp-24], 7
        mov     DWORD PTR [rbp-20], 8
```



Finally, if I executed the command, ```int_array[4] = 9;```, which values change?
