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
```
```
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        if len(nums)<1:
            return 0
        ans,i = 1,0
        nums = list(set(nums))
        nums.sort()
        count = 1
        while i < len(nums)-1:
            if nums[i]+1==nums[i+1]:
                i+=1
                count+=1
                if count>ans:
                    ans = count
            else:
                i+=1
                count=1
        return ans
```


```
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        if len(nums)<1:
            return 0
        ans,i = 1,0
        nums = list(set(nums))
        nums.sort()
        count = 1
        while i < len(nums)-1:
            if nums[i]+1==nums[i+1]:
                count+=1
                if count>ans:
                    ans = count
            else:
                count=1
            i+=1
        return ans
```



```
class Solution:
    def isPalindrome(self, s: str) -> bool:
        tempstr = ''
        for lett in s:
            if (lett>='a' and lett<='z') or (lett>='A' and lett<='Z') or (lett>='0' and lett<='9'):
                if lett>='A' and lett<='Z':
                    tempstr += chr(ord(lett) + 32)
                else:
                    tempstr+=lett
        st,ls = 0,len(tempstr)-1
        print(tempstr)
        while st<ls:
            if tempstr[st]!=tempstr[ls]:
                return False
            st+=1
            ls-=1
        return True
```
