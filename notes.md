# Data Structures

## Runtime Complexity and Big O Notation
 - an *algorithm* is a set of instructions for accomplishing a task
 - efficiency can mean *time efficiency* or *space efficiency*
 - *Big O Notation* is a way to describe the rate of change in execution speed of an algorithm when the data size increases; it is a way of compairing an algorythm's efficiency
 - Common Big O Runtimes:
     - Constant O(1): constant time, runtime or space uneffected by the size of the input; ex. lottery ball machine; accessing an element of an array by it's element
        ```
        def print_100th_element(array):
            print(array[99])

        # OR 

        def loop_50_times(array):
            for i in range(50):
                print(array[i])
        ```
     - Logarithmic O(log n):  logarithmic time, as size of input increases, runtime or space will grow at a slightly slower rate, pretty good solution; ex. flipping thru a dictionary, we know roughly where we're headed, but not the exapt page...scaled to a full bookshelf still roughtly where we're looking; `Binary Search` - searching for an entry in sorted data, find middle of array then compare to the target, now we know which half to look in, etc.
        ```
        def foo(input):
            i = len(input)
            while i > o:
                print(i)
                i /=2
        ```
     - Linear O(n): as size of input increases, runtime or space increases at the same rate, generally an acceptable solution; ex. counting something
        ```
        # looping thru every element looking for target
        def search(array, target):
            for el in array:
                if target == el:
                    return True
            return False
        
        # OR
        def foo(input):
            for i in input:
                print(i)
        ```
     - Linearithmic O(n log n): as the size of the input increases, the runtime or space will grow at a slightly faster rate, may be a workable solution but might not be ideal; ex. looping thru every element, and then doing something to each element; often seen in sorting algorithms 
        ```
        # mergesort
        # quicksort
        # heapsort
        #timsort
        ```
     - Polynomial O(n^c): quadratic time, as the size of the input increases, the runtime or space used will grow at a faster rate, may work for small inputs but is not scalable; ex. nested loops(numbe rof loops constant), `bubble sorting`
        ```
        # bubble sort
        def bubble_sort(array):
            for i in range(len(array)-1):
                for j in range(len(array)-2):
                    if array[i] > array[i+1]:
                        array [i], array[i+1] = array[i+1], array[1]

        # nested loops
        def foo(input):
            for word in input:
                for char in word:
                    print(char)
        ```
     - Exponential O(c^n): as the size of the input increases, the runtime or space used will grow at a much faster rate, this solution is inefficient; ex. nested loops(nubmer of loops increases as input increases); cracking unknown password
        ```
        # assume input an integer
        def foo(input):
            if n == 0: 
                return 0
            elif n == 1:
                return 1
            else:
                return foo(input-1) + foo(input-2)
        ```
     - Factorial O(n!): as the size of th input increases, the runtime or space will gros astronomically even with relatively small inputs; ex.
        ```
        # if input = ['a', 'b', 'c']
        def foo(input):
            word = permutation(input)
            for w in words:
                print(w)
                #abc, acb, bac, bca,cab, cba, #CBGBOMFUG, #ACAB


## Singly Linked Lists
 - 

## Stacks and Queues
 - *Stacks*: Last-In, First-Out; or First In; Last Out (a.k.a. LIFO or FILO)
     - `push` adds an item to the top of the stack
     - `pop` removes and returns the element at the top of the stack
     - `len` returns the number of elements in the stack
     - `top` returns a reference to the top element
 - *Queues*: First-In, First-Out
     - `enqueue` adds an element to the back of the queue.
     - `dequeue` removes and returns the element at the front of the queue.
     - `len` returns the number of elements in the queue.

## Doubly Linked List
 - 
## Binary Search Tree
 - *trees*: can be thought of as linked lists,but without the constraint that each node only points to one other node
 - *binary tree*: tree where each node can point to TWO other nodes
 - Terminology:
     - Root: topmost node of tree
     - Child: a node directly connected to another node when moving away form the root
     - Parent: a node directly connected to another node when moving towards form the root
     - Siblings: nodes that share the same parent
     - Leaf: node that does not have any children
 - Pros and Cons:
     - Pro: Searching for an element is more efficient than array or linked-list
     - Con: not as efficient to insert in binary serch tree as array or linked-list
     - Con: Performance depends on if tree is "balanced" or not. 