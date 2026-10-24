# AI-assisted exercise — Data Structures and Algorithms (DSA)

## Topic
Linear search and binary search

## Prompt used
> Explain the difference between linear search and binary search using a simple real-world example. Describe how each algorithm works, state their time complexities, and explain why binary search requires sorted data. Keep the explanation suitable for a B.Tech student.

## Tool and date
- **AI tool:** ChatGPT
- **Date:** 23 October 2026
- **Subject:** Data Structures and Algorithms (DSA)

## Summary of the response
The response explained that linear search checks elements one by one and works on sorted or unsorted data, while binary search compares against the middle element and repeatedly halves the remaining range. It gave best-case O(1) for both; average and worst-case O(n) for linear search; and average and worst-case O(log n) for binary search. It explained that binary search needs sorted data because the order is what makes it safe to discard half the search range.

## Review and verification
I read the explanation and did not identify a correction to make. I did not run code or time either algorithm on an input set. The complexity statements describe the usual comparison-based implementations; practical performance also depends on data structure and access costs.

## What I learned
I learned why binary search is asymptotically faster for large sorted collections, while linear search remains useful for small or unsorted collections.

## Record status
The response was reviewed in this assignment session and no correction was reported. The review did not include a documented external-source check or independent practical test, so this file does not claim either one took place.
