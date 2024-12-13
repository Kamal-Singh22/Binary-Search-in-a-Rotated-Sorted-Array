# Binary-Search-in-a-Rotated-Sorted-Array
You are given a rotated sorted array of integers nums and a target value target. Return the index of the target if it exists, otherwise return -1.

Explanation:
Binary Search with Rotated Array:

The array is divided into two parts at the pivot.
One of the two parts will always be sorted. Use this property to narrow down the search space.
Algorithm Steps:

Calculate the middle index: mid = left + (right - left) / 2.
Check if nums[mid] equals the target; if so, return mid.
If the left part (nums[left] to nums[mid]) is sorted:
If the target is within this range, adjust the right pointer to mid - 1.
Otherwise, adjust the left pointer to mid + 1.
If the right part (nums[mid] to nums[right]) is sorted:
If the target is within this range, adjust the left pointer to mid + 1.
Otherwise, adjust the right pointer to mid - 1.
Edge Cases:

If the array contains a single element.
If the target is not in the array.
Time and Space Complexity:
Time Complexity: O(log n) (binary search halves the search space at every step).
Space Complexity: O(1) (no additional space used).
