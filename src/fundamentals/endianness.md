# Endianness: Little Endian vs. Big Endian

If you have Ghidra already installed, take a look at [this binary file.](hardcoded)

If not, that's OK, too. After asking Ghidra to analyze the file, you should see the following:

```
void main(undefined param_1)

{
  undefined4 local_39;
  undefined4 local_35;
  undefined4 local_31;
  undefined2 local_2d;
  undefined4 local_2b;
  undefined4 local_27;
  undefined4 local_23;
  undefined4 local_1f;
  undefined4 local_1b;
  undefined4 local_17;
  undefined3 uStack_13;
  undefined1 *local_10;
  
  local_10 = &param_1;
  local_2b = 0x74696872;
  local_27 = 0x7b465443;
  local_23 = 0x73696874;
  local_1f = 0x5f73695f;
  local_1b = 0x64726168;
  local_17 = 0x65646f63;
  uStack_13 = 0x7d64;
  local_39 = 0x6c6c6548;
  local_35 = 0x6f77206f;
  local_31 = 0x2e646c72;
  local_2d = 10;
  printf("\n %s",(char *)&local_39);
  return;
}
```