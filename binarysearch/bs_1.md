# [Sum of Two Numbers](https://binarysearch.com/problems/Sum-of-Two-Numbers)

- Level：{Easy}
- Tags：{Array}, {HashTable}

## Idea

- [1] Traverse the input array and Use a hash table to record appearance, find if {target - current number} exists; If so, we could find a pair of two numbers, return true. 

### Implementation - Cpp

- Complexity：
  - Time O(N)
  - Space O(N)

``` c++
bool solve(vector<int>& nums, int k) {
    int n = nums.size();
    unordered_map<int, int> hash;
    for (int i = 0; i < n; i++) {
        int rem = k - nums[i];
        if (hash.count(rem)) {
            return true;
        }
        hash[nums[i]] = nums[i];
    }
    return false;
}
// ZedChou
```


