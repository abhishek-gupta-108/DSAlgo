## Binary Search

**Binary search is notorious for "off-by-one" errors**. The reason it’s confusing is that there isn't just one "correct" way; there are actually **two main templates**, and the logic changes depending on which one you pick. 

Here is a breakdown to help you choose the right logic every time.
#### 1. The "Standard Search" Template
Use this when: You are looking for a specific value (e.g., "Find the index of 7"). <br>
Condition: while (l <= r) <br>
Update r: r = m - 1 <br>
Update l: l = m + 1 <br>
Logic: Since you are checking if (nums[m] == target), you know for a fact that m is not the answer if the condition fails. Therefore, you can safely exclude m by adding or subtracting 1. <br>
Exit state: If the loop finishes, l > r and the target was not found.  <br>

#### 2. The "Boundary Search" Template
Use this when: You are looking for the first/last occurrence of something, or the smallest element that satisfies a condition (e.g., "Find the leftmost 1 in an array of 0s and 1s").  <br>
Condition: while (l < r) <br>
Update r: r = m <br>
Update l: l = m + 1 <br>
Logic: Here, the middle element m might actually be the answer you're looking for, so you don't want to discard it. By setting r = m, you keep it in your search range. <br>
Exit state: The loop stops when l == r. This is great because you don't have to wonder whether to return l or r—they are the same.  <br>


Summary Table
## Binary Search Templates Comparison

| Feature | Template 1: Standard Search | Template 2: Boundary / Optimization |
|----------|----------------------------|--------------------------------------|
| Primary Use Case | Finding a specific value (e.g., *Target exists?*) | Finding a threshold/boundary (e.g., *First True*) |
| While Condition | `while (l <= r)` | `while (l < r)` |
| Mid Logic (if) | `if (nums[m] == target) return m;` | `if (isFeasible(m)) r = m;` |
| Left Update | `l = m + 1` | `l = m + 1` |
| Right Update | `r = m - 1` | `r = m` |
| Termination | `l > r` (Range is empty) | `l == r` (One element remains) |
| Result | Target found or not found | `l` (or `r`) is the answer |


#### How to avoid the "Infinite Loop" ?
A common bug in the l < r template is when the code gets stuck. If your logic uses l = m and r = m - 1, the loop might never end because m is calculated using integer division (which rounds down).  <br>

````
Pro Tip: If you use l = m + 1 and r = m, use the standard mid calculation:
  m = l + (r-l)/2
If you ever find yourself needing l = m and r = m - 1, you must round the mid up:
  m = l + (r-l+1)/2
````

#### Preventing Overflows: 
Always use int m = l + (r - l) / 2; instead of (l + r) / 2 to avoid integer overflow issues. 

#### Which one should you use?
Most LeetCode problems (especially Medium/Hard ones) are "Boundary Search" problems. I recommend mastering the while (l < r) template. It is much more robust for problems like Search in Rotated Sorted Array or Koko Eating Bananas. 
