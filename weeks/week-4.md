# Week 4: Data Structures and Algorithms

This week focuses on Data Structures and Algorithms (DSA), which are fundamental to efficient programming and problem-solving. While Django handles many low-level operations, understanding DSA will make you a better developer overall. You'll learn common data structures, algorithms, and how to analyze their efficiency.

## Topics Covered

1. **Basic Data Structures**
   - Arrays and Lists
   - Stacks and Queues
   - Linked Lists (Singly and Doubly)
   - Hash Tables/Dictionaries

2. **Advanced Data Structures**
   - Trees (Binary Trees, Binary Search Trees)
   - Heaps
   - Graphs
   - Tries

3. **Algorithms**
   - Sorting algorithms (Bubble, Insertion, Quick, Merge)
   - Searching algorithms (Linear, Binary)
   - Recursion
   - Dynamic Programming basics

4. **Algorithm Analysis**
   - Big O notation
   - Time and Space complexity
   - Best, Average, and Worst case scenarios

5. **Problem-Solving Techniques**
   - Breaking down problems
   - Pattern recognition
   - Optimization strategies

## Resources

- [DSA Playlist](https://www.youtube.com/playlist?list=PLeo1K3hjS3uu_n_a__MI_KktGTLYopZ12)
- [Grokking Algorithms Book](./books/grokking-algorithms-illustrated-programmers-curious.pdf)

## Tasks

### Task 1: Implement Basic Data Structures
Implement common data structures from scratch in Python.

**Requirements:**
- Stack (push, pop, peek, is_empty)
- Queue (enqueue, dequeue, front, is_empty)
- Linked List (insert, delete, search, traverse)
- Binary Search Tree (insert, search, delete, traverse)

**Example - Stack Implementation:**
```python
class Stack:
    def __init__(self):
        self.items = []
    
    def push(self, item):
        self.items.append(item)
    
    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        return None
    
    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        return None
    
    def is_empty(self):
        return len(self.items) == 0
```

### Task 2: Sorting Algorithms
Implement and compare different sorting algorithms.

**Requirements:**
- Implement Bubble Sort, Insertion Sort, and Quick Sort
- Create a function to test each algorithm with the same data
- Measure and compare their performance (time complexity)
- Analyze Big O for each algorithm

### Task 3: Searching Algorithms
Implement searching algorithms and analyze their efficiency.

**Requirements:**
- Linear Search
- Binary Search (requires sorted array)
- Compare their time complexities
- Implement on both arrays and linked lists

### Task 4: Problem-Solving Practice
Solve algorithmic problems using the data structures you've learned.

**Problems to solve:**
1. Reverse a linked list
2. Check if a string has balanced parentheses (using Stack)
3. Find the middle element of a linked list
4. Implement a LRU Cache
5. Solve the Two Sum problem

**Example - Two Sum:**
```python
def two_sum(nums, target):
    """
    Given an array of integers and a target sum,
    return indices of two numbers that add up to target.
    """
    num_map = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in num_map:
            return [num_map[complement], i]
        num_map[num] = i
    return []
```

## Tips for Success

- Focus on understanding concepts rather than memorizing code
- Practice implementing data structures without looking at solutions first
- Use the Grokking Algorithms book alongside the video playlist
- Analyze time and space complexity for every algorithm you implement
- Start with small problems and gradually increase complexity
- Use online platforms like LeetCode for additional practice (optional)

## Next Steps

DSA skills will help you write more efficient code and ace technical interviews. In Week 5, we'll finally dive into Django! Use your newfound algorithmic thinking to approach Django concepts more systematically.

Remember, DSA is a marathon, not a sprint. Consistent practice over time will yield the best results. Keep solving problems! 🧠
