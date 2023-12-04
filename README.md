# About the repositories: Serial_parameter
Adjust the parameters through the serial port

# How to configure
Take the file `Serial_parameter.ino` as an example:
+ Copy the two files (`ser_par.cpp` and `ser_par.h`) to the directory
+ `#include "ser_par.h"`
+ Define an array containing the addresses of the variables you want to set by serial
  ```int *par_list[5] = {&a,&b,&c,&d,&e};```
+ Call `ser_par()` in the loop function and pass in the array parameters
  ```ser_par(par_list);```

# How to use
Use the serial port to send：`SaTb\n`

`S`, `T`, `\n` are used as markers. They cannot be modified.

Normally, `\n` is sent by Arduino by default, and does not need to be entered.

Replace `a` with the index of the array of parameters to be adjusted, and `b` with the value you want to set to.

# Warning
+ The variable to be adjusted can only be of type int
