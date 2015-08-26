---
title: 2015-08-27-unh Python Lesson Outline

---

# Setup #

-   Make sure that before lunch everyone has installed Anaconda python
    and run the <http://bsmith89.github.io/2015-08-27-unh/setup/index.html>
    test scripts.
-   (TD) Install anaconda python2.7 distribution
-   (TD) Put note in etherpad for students to download the
    [data repository][data-repo] to their desktop
    -   Expect it to be named `python-novice-inflammation/data`

[data-repo]: http://swcarpentry.github.io/python-novice-inflammation/python-novice-inflammation-data.zip




# Day 1 Plan #

Could I ask students if they want the motivation first?  If so, I can show them
the [numpy](#libraries-and-plotting) section, otherwise start the [following
section](#variables-assignment-and-arithmatic)




## Libraries and Plotting ##
    -   loading csv data
    -   getting mean's, max's, min's
    -   Plotting
        -   Heatmap
        -   Trends




## Variables, Assignment, and Arithmatic ##


### Assign variables with an equals sign ###

```python
weight_kg = 55
print weight_kg

print 'weight in pounds:', 2.2 * weight_kg
print 'tar weight:', weight_kg - 1.656
print 'each piece (of 5) weighs:', weight_kg / 5.0
```

### Variables are like sticky notes ###

```python
weight_kg = 57.5

print 'weight in kilograms is now:', weight_kg
```

### Evaluation happens at the time of assignment ###

```python
weight_lb = 2.2 * weight_kg
weight_kg = 25

print 'weight_kg is now:', weight_kg
print 'but weight_lb has not changed:', weight_lb
```

### Check your understanding ###

Draw diagrams showing what variables refer to what values after each statement
in the following program:

```python
mass = 47.5
age = 122
mass = mass * 2.0
age = age - 20
```



## Storing Multiple Values in Lists ##

### Lists are a way to store multiple values ###

```python
odd_numbers = [1, 3, 5, 7]
print odd_numbers
```

### Indexing lists ###

```python
names = ['Newton', 'Turing', 'Darwing']

print names[0]
print names[1]
print names[2]

i = 1
names[1]

print names[0:2]
```

### Assigning and appending ###

```python
names[2] = 'Darwin'
print names

# But not
a_name = Edison
a_name[4] = 'z'

names.append('Tesla')
print names
```

### Variables referencing lists ###

```python
those_same_names = names

print 'names is currently:', names
print 'those_same_names is currently:', those_same_names

those_same_names.append('Einstein')
print 'those_same_names is now:', those_same_names
print 'but names has also changed:', names
```

### Challenge question ###

What is printed by the following

```python
a_list = ["what's", "in" "a", "name"]

print a_list[3][3]
```




## Repeating Actions with Loops ##

### Motivation ###

What if we want to print everything in names?

```python
print names

print names[0]  # Newton
print names[1]  # Turing
print names[2]  # Darwin
print names[3]  # Tesla
print names[4]  # Einstein
```

That's kinda repetitive, and what happens if the length of the list is
unknown before we run that code?

There must be a better way.

```python
for some_name in names:
    print some_name
print "That's all of the names!"
```

### Anatomy of a loop ###

### Counting things with loops ###

### Iterators: briefly ###

### Challenge question ###

Exponentiation is built into Python:

```python
print 5 ** 3
125
```

Write a loop that calculates the same result as 5 ** 3 using multiplication
(and without exponentiation).




## Making Choices ##

### Booleans ###

While `=` is the assignment operator, we often use it in common writing to mean
"is equal to".

In python, you ask the question "is x equal to y" with `x == y`.

The value of that statement depends on the values of `x` and `y`.

```python
print 6 == 6

x = 6
y = 7
z = '6'
print x == y
print x > y
print x <= x
```

### Booleans logic: `and` and `or` ###

```python
print x == z
print x == int(z)
print (x == z) or (x == int(z))
```

### Anatomy of an If-statement ###

```python
num = 37
if num > 100:
    print 'greater than 100'
else:
    print 'not greater than 100'
print 'done'
```

The `else` part is not necessary.

What if we want to do something else if `num` _is_ greater than 25?

We _could_ do this:

```python
num = 37
if num > 100:
    print 'greater than 100'
else:
    if num > 25:
        print 'greater than 25'
    print 'not greater than 100'
print 'done'
```

But this is messy and it's cleaner to use an `elif` block, which means
the same thing.


```python
num = 37
if num > 100:
    print 'greater than 100'
elif num > 25:
    print 'greater than 25'
else:
    print 'not greater than 25'
print 'done'
```

### Check your understanding ###

What will be printed if you run this code? Why did you pick this answer?

```python
if 4 > 5:
    print 'A'
elif 4 == 5:
    print 'B'
elif 4 < 5:
    print 'C'
```



### Libraries and Plotting ###

While the _language_ python is powerful, the most useful part for you may be
the tools and software that have been built with it.

While we've already shown you some of the words and short sentences that can
be made with python, let's take a look at entire libraries of work that
have already been constructed.

In python, the syntax to load a package is `import <package>`.
Let's import one of the most useful packages and play with it a bit.

```python
import numpy

data = numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')
print data
```

-   `numpy` is a python package that we've already installed
-   `import numpy` loads it into our program so that we can use everything
    inside of that package
-   `loadtxt` is a function written in the `numpy` package
-   `numpy.loadtxt` means "the function named `loadtxt` which belongs to
    `numpy`" (the dot means, "an attribute of").
-   `fname` and `delimiter` are two parameters that we're giving to loadtxt
-   We call the function with its parameters and assign the result to `data`.

