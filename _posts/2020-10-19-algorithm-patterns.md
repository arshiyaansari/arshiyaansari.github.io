---
layout: post
section-type: post
title: Basic Algorithm Patterns for Coding Interviews
category: technical
tags: [ 'blog', 'post', 'technical', 'prep', 'interview', 'coding']
---

in this blog post, i hope to highlight one of the most common algorithm patterns i compiled while prepping for my coding interviews. when i first started prepping for coding interviews, i tended to *memorize* the solutions for coding problems in the hopes that my interviewer would ask exactly the questions i studied. as you can guess, that never really happened so instead, i started to learn the patterns that are hidden in these problems so i could learn how to approach new problems -- problems i've never seen before! 

#### input matters -- especially sorted lists
i think it is so important, as a programmer, to look at what the inputs of the problem are. it gives you insight on how to break the question down. for inputs that are **sorted lists**, it is almost always safe to assume that you will be using binary search in some form. modified binary searches are such a popular coding interview question, and it is important to first, understand what binary search does, and how you can modify it to fit your problem. binary search essentially splits our sorted list into half with each iteration, also reducing our search space by half. this does wonders for reducing the linear search runtime to a logarithmic search runtime. 

**binary search algorithm**: 
1. find the beginning of the array, and the end of the array 
2. while we iterate through the array, calculate the midpoint value of the array -- the addition of l + (r-l) is so when we reset the left and right pointers 
3. check if the midpoint equals the target, if so, return the target
4. if the midpoint is less than the target, iterate on the right half of the list (the greater half) by setting the new left pointer as mid + 1
5. if the midpoint is greater than the target, iterate on the left half of the list (the lesser half) by setting the new right pointer as mid - 1 
6. return -1 if we can't find it

**modified binary search problems**: 
- leetcode #33: [search in rotated sorted array](https://leetcode.com/problems/search-in-rotated-sorted-array/) (Medium)
- leetcode #34: [find first and last position of element in sorted array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) (Medium)
- leetcode #528: [random pick with weight](https://leetcode.com/problems/random-pick-with-weight/) (Medium)
- leetcode #4: [median of two sorted arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) (Hard)
- leetcode #1095: [find in mountain array](https://leetcode.com/problems/find-in-mountain-array/) (Hard)