# Day19 :Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order. You must write an algorithm with O(log n) runtime complexity.  

**Test Cases**
1. input:nums = [1,3,5,6], target = 5       output:2
2. Input: nums = [1,3,5,6], target = 2      Output: 1

**Intuition**
1. The array is sorted, so we can use binary search.
2. If target equals the middle element → return its index.
3. If target is less than middle → search the left half.
4. If target is greater than middle → search the right half.
5.If the element is not found, the left pointer will indicate the correct insertion index.

**Algorithm Flow**
1.Initialize two pointers:
  left = 0
  right = nums.length - 1
2.While left <= right:
3.Compute mid = left + (right - left)/2
4.If nums[mid] == target → return mid
5.Else if nums[mid] < target → move left = mid + 1
6.Else → move right = mid - 1
7.If not found → return left as the insertion index

**Complexity Analysis**
Time Complexity: O(log n)
Space Complexity: O(1)

