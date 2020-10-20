---
layout: post
section-type: post
title: Basic Algorithm Patterns for Coding Interviews
category: technical
tags: [ 'blog', 'post', 'technical', 'prep', 'interview', 'coding']
---

In this blog post, I hope to highlight some of the most common algorithm patterns I compiled while prepping for my coding interviews. When I first started prepping for coding interviews, I tended to *memorize* the solutions for coding problems in the hopes that my interviewer would ask exactly the questions I studied. As you can guess, that never really happened so instead, I started to learn the patterns that are hidden in these problems so I could learn how to approach new problems -- problems I've never seen before! 

#### Input Matters -- Especially Sorted Lists
I think it is so important, as a programmer, to look at what the inputs of the problem are. It gives you insight on how to break the question down. For inputs that are **sorted lists**, it is almost always safe to assume that you will be using binary search in some form. Modified binary searches are such a popular coding interview question, and it is important to first, understand what binary search does, and how you can modify it to fit your problem. Binary search essentially splits our sorted list into half with each iteration, also reducing our search space by half. This does wonders for reducing the linear search runtime to a logarithmic search runtime. 

**Binary Search Algorithm**: 
1. Find the beginning of the array, and the end of the array 
2. While we iterate through the array, calculate the midpoint value of the array -- the addition of l + (r-l) is so when we reset the left and right pointers 
3. Check if the midpoint equals the target, if so, return the target
4. If the midpoint is less than the target, iterate on the right half of the list (the greater half) by setting the new left pointer as mid + 1
5. If the midpoint is greater than the target, iterate on the left half of the list (the lesser half) by setting the new right pointer as mid - 1 
6. Return -1 if we can't find it

**Modified Binary Search Problems**: 
- LeetCode #33: [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/) (Medium)
- LeetCode #34: [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) (Medium)
- LeetCode #528: [Random Pick with Weight](https://leetcode.com/problems/random-pick-with-weight/) (Medium)
- LeetCode #4: [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) (Hard)
- LeetCode #1095: [Find in Mountain Array](https://leetcode.com/problems/find-in-mountain-array/) (Hard)