# [Palindromic Integer](https://binarysearch.com/problems/Palindromic-Integer)

- Level：{Easy}
- Tags：{Math}

## Idea

- [1] Use **秦九韶** algorithm, including division and modulo operations. Modulo operation could get rightmost digit, and division moves the number one digit to the right

### Implementation - Cpp

- Complexity：
  - Time O(logN)
  - Space O(1)

``` c++
bool solve(int num) {
    int res = 0;
    int ori = num;
    while (num != 0) {
        res = res * 10 + num % 10;
        num /= 10;
    }
    return res == ori;
}
// Zed Chou

```

### Implementation - Python3
``` Python3
class Solution:
    def solve(self, num):
        return str(num)==str(num)[::-1]
// Lianz_lit
```
