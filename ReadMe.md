```
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        ans,i =0,0
        nums.sort()
        print(nums)
        count = 1
        while i < len(nums)-1:
            if nums[i]+1==nums[i+1]:
                i+=1
                count+=1
                if count>ans:
                    ans = count
            else:
                i+=1
                count=0
        return ans
```
```
def longestConsective(nums):
    new = sorted(nums)
    print(new)
    result = []
    position = 0
    while position <= :
        for i in new:
            if new[position+1] == i+1:
                result.append(i)
                position += 1
