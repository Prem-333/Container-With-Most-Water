Your code implements the Container With Most Water problem (LeetCode #11) using the Two-Pointer Technique.

Here’s the algorithm:

Algorithm for maxArea
Start

Initialize:

l = 0 (left pointer)

r = heightSize - 1 (right pointer)

ans = 0 (max area so far)

While l < r:

Compute t = min(height[l], height[r]) * (r - l) (area between two lines)

Update ans = max(ans, t)

If height[l] < height[r], increment l (l++)

Else, decrement r (r--)

Return ans

End

Why It Works
Start with the widest container (l=0, r=n-1)

Move the pointer pointing to the shorter line inward, because width decreases anyway, so to increase area, we need a taller height.
