## Example  

```python
import math
# try with n = 5
%timeit n = 5; x = n * n
%timeit n = 5; x = 2 ** (math.log2(n))
%timeit n = 5; x = 2 ** (2 ** (n + 1))
%timeit n = 5; x = 2 ** (2 ** (n))
# try again with a different n to see if the relative speed holds
%timeit n = 6; x = n * n
%timeit n = 6; x = 2 ** (math.log2(n))
%timeit n = 6; x = 2 ** (2 ** (n + 1))
%timeit n = 6; x = 2 ** (2 ** (n))
```
