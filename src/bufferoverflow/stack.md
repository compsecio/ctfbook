# The Stack

With a colleague, sketch out how the following items would be arranged on the stack.

Assume the following:
* We are dealing with a 32-bit, little endian processor. 
* char data types are 1 byte each. 
* int's are four bytes each


Code:
```C
int x = 1;
char char_array[] = "ABC"; //Assume ASCII encoding
int y = 2;
int int_array[4] = {3,4,5,6};
```



---



You can check your answer by looking at the following output from gcc on the above code.

```
        mov     DWORD PTR [ebp-4], 1
        mov     DWORD PTR [ebp-12], 4407873
        mov     DWORD PTR [ebp-8], 2
        mov     DWORD PTR [ebp-28], 3
        mov     DWORD PTR [ebp-24], 4
        mov     DWORD PTR [ebp-20], 5
        mov     DWORD PTR [ebp-16], 6
```

Complete the following:
1. If I executed the command, ```int_array[4] = 7;```, which values have changed?
2. How is ```char_array``` arranged in memory? Why does the assembly output show it to be 4407873? 