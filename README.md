Two Sum - LeetCode Solution

Problem Statement

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

Example

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

Solution Approach

The solution utilizes a hash map (dictionary in Python) to efficiently find the required indices in one pass.

Code Implementation

def two_sum(nums: list[int], target: int) -> list[int]:
    num_map = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in num_map:
            return [num_map[complement], i]
        num_map[num] = i
    return []

Complexity Analysis

Time Complexity: O(n), where n is the number of elements in nums. We traverse the list once.

Space Complexity: O(n), as we store elements in a hash map.

How to Run

Clone this repository:

git clone https://github.com/your-username/two-sum.git
cd two-sum

Run the Python script:

python solution.py

Contributions

Feel free to fork this repository, submit issues, or contribute improvements!

License

This project is licensed under the MIT License.

