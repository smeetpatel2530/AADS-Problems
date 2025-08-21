# Insertion Sort


```cpp
class Solution {
public:
    vector<int> insertionSort(vector<int>& nums) {
        int n = nums.size(); 
        for (int i = 1; i < n; i++) {
            int key = nums[i]; 
            int j = i - 1; 
            while (j >= 0 && nums[j] > key) {
                nums[j + 1] = nums[j];
                j--;
            }
            
            nums[j + 1] = key; 
        }
        
        return nums;
    }
};


```

## Time Complexity = O(N^2)
## Space Complexity = O(1)

