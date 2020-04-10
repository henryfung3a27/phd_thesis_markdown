## Authentication_1

The `authentication_1` function takes 4 parameters, each with size of 4 bytes (`dword`).
After inspection by debugging, I found that the first and second parameters are addresses, 
more specifically arrays of 8 elements with 4 bytes each resulting in total of 32 bytes. 

![Caller to read `param_1` address](img/snippet_param1_read_addr_caller.png)

![Caller to read `param_2` address](img/snippet_param2_read_addr_caller.png)

![Code snippet inside `FUN_1002afe0`](img/snippet_param1_read_addr.png)

(Note: `i` is a counter from 0 to 7 inclusively, which means the function is trying to get
8 elements from address `param_1`, namely `*(param_1 + 0)`, `*(param_1 + 1)`, ..., `*(param_1 + 7)`.

