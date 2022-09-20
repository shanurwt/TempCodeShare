
```
class Solution:
    def productExceptSelf(self, nums: List[int]) -> List[int]:
        left=[0]*len(nums)
        right=[0]*len(nums)
        left[0],right[-1]=1,1
        for i in range(1,len(nums)):
            left[i]=left[i-1]*nums[i-1]
            right[len(nums)-1-i]=right[len(nums)-i]*nums[len(nums)-i]
        for i in range(len(nums)):
            nums[i]=left[i]*right[i]
        return nums
```
```
this code sus af homie
                     -WNHF
The array/list can be divided into 2 parts- left and right array/list. Left[0] and Right[last] will be 1. Left list will be calculated by multiplying 
left[index-1]*nums[index-1]. Right list will be calculated by numtiplying right[last-index]*nums[last-index]. At last multiply left and right elements and store it 
into nums list.

```
```
res = [1] * len(nums)
        for i in range(1, len(nums)):
            # [1, 2, 3, 4] nums
            # [1, 1, 2, 6] res
            # [24,12,8, 6] final res
            res[i] = res[i - 1] * nums[i - 1]
        right_prod = 1
        for i in range(len(nums) - 1, -1, -1):
            res[i] = right_prod * res[i]
            right_prod *= nums[i]
        return res
```
