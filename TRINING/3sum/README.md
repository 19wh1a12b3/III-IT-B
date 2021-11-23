
class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        hashMap = {}
        for i in range(len(nums)):
            hashMap[nums[i]] = i
        result = []
        visit = set()
        for i in range(len(nums)):
            for j in range(i+1,len(nums)):
                complete = 0 -(nums[i] + nums[j])
                if tuple(sorted([complete,nums[i],nums[j]])) in visit:
                    continue
                visit.add(tuple(sorted([complete,nums[i],nums[j]])))
                third = hashMap.get(complete)
                if third != None and third != i and third != j:
                    result.append(([complete,nums[i],nums[j]]))
        return result
