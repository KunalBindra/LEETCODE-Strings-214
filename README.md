# LEETCODE-Strings-214
Let's do a dry run of the `shortestPalindrome` function using an example string.

### Problem Definition:
The method `shortestPalindrome` tries to find the shortest palindrome that can be made by adding characters only to the **beginning** of the string.

#### Example:
Let's test it with the string `"abacd"`. 

#### Dry Run:

1. **Input**: 
   - `s = "abacd"`
   - `t = reverse(s) = "dcaba"`

2. **Iteration**:
   - We are looping over the reversed string `t` and checking if `s` starts with a substring of `t`.

### First Iteration (`i = 0`):
   - `t.substring(0) = "dcaba"`
   - Check if `s.startsWith("dcaba")`: 
     - `s = "abacd"` does not start with "dcaba".
   - Continue to next iteration.

### Second Iteration (`i = 1`):
   - `t.substring(1) = "caba"`
   - Check if `s.startsWith("caba")`: 
     - `s = "abacd"` does not start with "caba".
   - Continue to next iteration.

### Third Iteration (`i = 2`):
   - `t.substring(2) = "aba"`
   - Check if `s.startsWith("aba")`: 
     - `s = "abacd"` **does** start with "aba".
   - The condition is satisfied.

3. **Return Statement**:
   - The palindrome can be formed by appending `t.substring(0, 2) = "dc"` to the beginning of `s`.
   - So, the result is `"dc" + "abacd" = "dcabacd"`.

Thus, for the input `"abacd"`, the shortest palindrome is `"dcabacd"`.

### Key steps:
- Reverse the string.
- Loop through the reversed string and check where it aligns with the original.
- Prepend the unmatched part of the reversed string to form a palindrome.

Let me know if you'd like further explanation or other examples!
