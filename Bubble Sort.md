# Bubble Sort


```cpp
class Solution {
public:
    vector<int> bubbleSort(vector<int>& nums) {
        int n = nums.size();
        for (int i = n - 1; i >= 0; i--) {
            bool didSwap = false;
            for (int j = 0; j <= i - 1; j++) {
                if (nums[j] > nums[j + 1]) {
                    swap(nums[j], nums[j + 1]);
                    didSwap = true;
                }
            }
            if (!didSwap) {
                break;
            }
        }
        return nums;
    }
};

```

## Time Complexity = O(N^2)
## Space Complexity = O(1)
```
