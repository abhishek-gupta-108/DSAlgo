
##  For Array/Strings(Contiguous Subarray/Substring)

### Using Binary Search
   - where a contiguous chunking has to happen in String or Array
   - You are giving a fixed limit that affects how you chunk the array.
   - You have to maximize of minimize the result
   - https://leetcode.com/problems/longest-repeating-character-replacement/description/?envType=problem-list-v2&envId=string
   - https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/description/
   

### Using Sliding Window/two pointer

#### Template: where you feel that the sliding window will expand but that can be solved: <br>
Once you solved this with 2 pointers, there is still opportunity to improve =>O(2N) to O(N) by pruning

Problem:
1. https://leetcode.com/problems/longest-substring-with-at-most-two-distinct-characters/description/ (Premium) - Given a string s, return the length of the longest substring that contains at most two distinct characters.
2. https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/description/ - (Premium) - Generric to above - Given a string s and an integer k, return the length of the longest substring of s that contains at most k distinct characters.
3. https://leetcode.com/problems/subarrays-with-k-different-integers/description/ - For Integer array
