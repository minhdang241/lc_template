# Sliding Window
Pattern: (Longest|Shortest|Number of) (Substrings|Subarrays) with (At most|Exactly) K elements that fit (some condition). This usually requires TC as O(N).
    - Longest -> While loop invalid condition
    - Shortest/Minimum -> While loop valid condition
    - Number of subarray/substring that has atmost/exactly k elements

    template:
    for (right = 0; right < n; right++) {
        update window with element at right pointer
        while condition is invalid:
            remove element at the left pointer
        update the global value
    }

# Binary Search
Pattern: Find minimum of something and we can discover some kind of monotonicity, for example, if condition(k) is True, then condition(k+1) is also True.
    template:
    l, r = min, max
    while l < r:
        m = (l+r)//2
        if condition(m):
            r = m
        else:
            l = m + 1
    return left | left - 1 depends on the problem.
    *Note*: left represents the minimal k satisfying the condition. 

    Proof to show that a result is available:
    using condition(k) and condition(k-1) with k is the minimal value satisfying the condition. Thus, if condition(k-1) is also True then k should be available to select.

# Two pointers


# Graph
1. For directed graph, to detect cycle with DFS we can't use a visited array. Instead, using the COLOR algorithm.
    - LC 1059



