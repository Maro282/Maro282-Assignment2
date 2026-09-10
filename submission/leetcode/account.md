# Reverse string

profile link => https://leetcode.com/u/marawanelsawy00/

problem solution link (two sum) => https://leetcode.com/problems/reverse-string/solutions/8511507/reverse-string-using-two-pointers-approa-srkk/

# Intuition

We can reverse the string in-place by using two pointers: one at the beginning and one at the end. We swap the characters at these positions and move both pointers toward the center.

# Approach

Initialize two pointers, `left` at the beginning of the array and `right` at the end. While `left < right`, swap `s[left]` and `s[right]`, then increment `left` and decrement `right`. This continues until the pointers meet.

# Complexity

- Time complexity: O(n)

- Space complexity: O(1)

# Code

```csharp
public class Solution {
    public void ReverseString(char[] s) {
              int right =  s.Length - 1;
            int left = 0;

           while(left < right)
        {
                char temp = s[right];
                s[right]=s[left];
                s[left]= temp;
                left ++;
                right --;
        }
    }
}
```
