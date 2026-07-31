# Tower of Hanoi using State Space Search (BFS)

## Aim

To implement the **Tower of Hanoi problem using State Space Search (Breadth-First Search - BFS)** and find the shortest sequence of valid moves to transfer all disks from the source peg to the destination peg.

---

# Theory

## What is Tower of Hanoi?

Tower of Hanoi is a famous puzzle consisting of **three pegs** and **N disks** of different sizes.

* Initially, all disks are placed on **Peg A** in decreasing order of size.
* The objective is to move all disks to **Peg C**.
* Peg **B** is used as an auxiliary peg.

### Rules

1. Only one disk can be moved at a time.
2. Only the top disk of a peg can be moved.
3. A larger disk cannot be placed on a smaller disk.

---

## What is State Space Search?

A **State Space Search** represents a problem as a collection of states.

* **State** = Current arrangement of disks on the three pegs.
* **Action** = Moving one valid disk from one peg to another.
* **Goal State** = All disks are moved to Peg C.

The algorithm searches through different states until it reaches the goal.

---

## Why Breadth-First Search (BFS)?

BFS explores all possible states level by level.

Advantages:

* Finds the shortest solution.
* Never misses a valid solution.
* Easy to understand.

---

# State Representation

For **3 disks**

Initial State

```
A = (3,2,1)
B = ()
C = ()
```

Goal State

```
A = ()
B = ()
C = (3,2,1)
```

---

# Visual Explanation

Suppose there are **3 disks**.

### Step 0 (Initial State)

```
      |
      |
      |
     ===      Disk 1
    =====     Disk 2
   =======    Disk 3
-------------------------
   A        B        C
```

---

### Step 1

Move Disk 1 from A → C

```
      |
      |
      |
    =====
   =======
-------------------------
   A        B       ===
                    C
```

---

### Step 2

Move Disk 2 from A → B

```
      |
      |
      |
   =======
-------------------------
   A      =====      ===
           B          C
```

---

### Step 3

Move Disk 1 from C → B

```
      |
      |
      |
   =======
-------------------------
   A     =====
          ===
          B
```

---

### Continue...

The process continues until

```
A = ()
B = ()
C = (3,2,1)
```

---

# State Space Tree

```
                     Start
               A:(3,2,1)

               /       \
            Move1     Move2
             /           \
         State1        State2
          /  \          /  \
      State3 State4 State5 State6
                .
                .
                .
            Goal State
```

Each node represents one state.

Each edge represents one valid move.

---

# BFS Working

Queue initially contains

```
Queue

-----------------
| Start State |
-----------------
```

Remove first state

Generate all possible legal moves

```
Queue

-----------------
| State 1      |
| State 2      |
-----------------
```

Remove State 1

Generate its child states

```
Queue

-----------------
| State 2      |
| State 3      |
| State 4      |
-----------------
```

Repeat until Goal State is found.

---

# Algorithm

### Step 1

Create the initial state with all disks on Peg A.

### Step 2

Create the goal state with all disks on Peg C.

### Step 3

Create a queue for BFS.

### Step 4

Insert the initial state into the queue.

### Step 5

Create a visited set to avoid revisiting states.

### Step 6

Repeat until the queue becomes empty:

* Remove the first state from the queue.
* If it is the goal state, stop.
* Otherwise:

  * Generate all valid next states.
  * Add unvisited states to the queue.

### Step 7

Print the sequence of states from start to goal.

---

# Flowchart

```text
        Start
           |
           V
 Create Initial State
           |
           V
 Add State to Queue
           |
           V
 Is Queue Empty?
      /        \
    Yes        No
     |          |
   Stop   Remove Front State
               |
               V
      Is Goal State?
          /      \
        Yes      No
         |        |
 Print Solution   |
         |        |
        Stop      |
                 V
     Generate Valid Moves
                 |
                 V
      Add New States to Queue
                 |
                 |
          Repeat Loop
```

---

# Time Complexity

Number of possible states:

```
3^n
```

Therefore,

**Time Complexity**

```
O(3^n)
```

---

# Space Complexity

The queue and visited set may store many states.

```
O(3^n)
```

---

# Advantages

* Finds the shortest sequence of moves.
* Guarantees reaching the goal if a solution exists.
* Easy to implement using BFS.

---

# Disadvantages

* Uses more memory because it stores many states.
* Becomes slow for a large number of disks.
* Not as efficient as the recursive Tower of Hanoi algorithm for large inputs.

---

# Applications

* Artificial Intelligence (State Space Search)
* Robot motion planning
* Puzzle solving
* Path finding
* Search algorithms
* Game state exploration

---

# Sample Output

```
Enter number of disks: 2

Solution

Step 0
A: (2,1)
B: ()
C: ()

Step 1
A: (2)
B: (1)
C: ()

Step 2
A: ()
B: (1)
C: (2)

Step 3
A: ()
B: ()
C: (2,1)
```

---

# Conclusion

The Tower of Hanoi problem can be solved using **State Space Search** by treating each arrangement of disks as a **state**. **Breadth-First Search (BFS)** explores all valid states level by level and guarantees the shortest sequence of moves from the initial state to the goal state. This experiment demonstrates how AI search techniques can be applied to solve classical problems systematically.
