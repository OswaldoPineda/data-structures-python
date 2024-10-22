![image](https://github.com/user-attachments/assets/d882d206-f722-447a-b9df-872ac266a54a)

### **What is Time Complexity?**

The **Time complexity** of an algorithm can be defined as a measure of the amount of time taken to run an algorithm as a function of the size of the input. In simple words, it tells about the growth of time taken as a function of input data.

Time complexity is categorized in 3 types:

- **Best-Case Time Complexity:** The minimum amount of time required by an algorithm to run, based on the given most suitable input is known as best-case complexity. It is denoted by the sign Big Omega (Ω).
- **Average Case Complexity:** The average amount of time required by an algorithm to run, taking into consideration all the possible inputs is known as average-case complexity. It is denoted by the sign Big Theta (Θ).
- **Worst Case Complexity:** The maximum amount of time required by an algorithm to run, taking into consideration possible worst case is known as worst-case complexity. It is denoted by the sign Big O(O).

## Big O notation

Big O notation is a way of describing the speed or complexity of a given algorithm.

Simply, Big O notation tells you the number of operations an algorithm will perform. It takes its name from the “Big O” in front of the estimated number of operations.

What the Big O notation does not tell you is how fast the algorithm will be in seconds. There are too many factors that influence how long it takes for an algorithm to run. Instead, you will use the Big O notation to compare different algorithms by the number of operations they do.

### Big o worst case

Imagine you are a teacher and you have a student named Jane. You want to find her records, so you use a simple search algorithm to traverse your school district's database.

You know that the simple search takes O(n) times to execute. This means that in the worst case, you will have to search through every record (represented by n) to find Jane's record.

But when you run the simple search, you find that Jane's records are the first entry in the database. You don't have to look at every entry – you found it on your first try.

*Did this algorithm take O(n) time? Or did it take O(1) because you found Jane's records on the first try?*

In this case, O(1) is the best case: you were lucky that Jane's records were at the beginning. But Big O notation focuses on the worst case, which is O(n) for the simple search. It's a guarantee that the simple search will never be slower than O(n) time.

### O(n)

In a code where the worst scenario is go thought all the elements the notation is `O(n)`

```python
def print_items(n):
    for i in range(n):
        print(i)

print_items(10)
```

This is represented as

![image](https://github.com/user-attachments/assets/0bbca171-71b0-4868-9bff-40695cf60e4a)


Meaning that if you increases the possible scenarios, the time increases proportional.

If you have an algorithm like:

```python
def print_items(n):
    for i in range(n):
        print(i)

    for j in range(n):
        print(j)

print_items(10)
```

The notation for this would be `O(2n)` due to the same number of operations are running twice, one rule for the notation is remove the constant, eve if the notation is `O(100n)` we drop the constant.

### O(n^2)

It is also known as **Quadratic Time complexity**. In this type the running time of algorithm grows as **square** function of input size. This can cause very large time for large inputs. Here, the notation O in `O(n2)` represents its worst cases complexity.

> The O(N^2) time complexity means that the running time of an algorithm grows quadratically with the size of the input. It often involves nested loops, where each element in the input is compared with every other element.
> 

An example on code is

```python
def print_items(n):
    for i in range(n):
        for j in range(n):
            print(i,j) 

print_items(10)
```

When you have an algorithm like the following one where there are more scenarios and the expected notation would be `O(n^2 + n)`  the rule is keeping only the dominan value resulting on `O(n^2)`

```python
def print_items(n):
    for i in range(n):
        for j in range(n):
            print(i,j)
    
    for k in range(n):
        print(k)

print_items(10)
```

### O(1)

In short, O(1) means that it takes a constant time, like 14 nanoseconds, or three minutes no matter the amount of data in the set.

```python
def add_items(n):
    return n + n + n
 

print add_items(10)
```

O(n) means it takes an amount of time linear with the size of the set, so a set twice the size will take twice the time. You probably don't want to put a million objects into one of these.

This is always the best scenario possible to take and is represented as constant in the initial image.

### O(log n)

The most common attributes of logarithmic running-time function are that:

- the choice of the next element on which to perform some action is one of several possibilities, and
- only one will need to be chosen.

Or

- the elements on which the action is performed are digits of n

This is why, for example, looking up people in a phone book is O(log n). You don't need to check *every* person in the phone book to find the right one; instead, you can simply divide-and-conquer by looking based on where their name is alphabetically, and in every section you only need to explore a subset of each section before you eventually find someone's phone number.

Of course, a bigger phone book will still take you a longer time, but it won't grow as quickly as the proportional increase in the additional size.
