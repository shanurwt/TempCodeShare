
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
this code sus af homie
