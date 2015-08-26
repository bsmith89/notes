2015-08-27-unh Python Lesson Outline

# Setup #

-   Make sure that before lunch everyone has installed Anaconda python
    and run the http://bsmith89.github.io/2015-08-27-unh/setup/index.html
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

### Check you understanding ###

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

### Indexing Lists ###

```python

names = ['Newton', 'Turing', 'Darwing']

print names[0]
print names[1]
print names[2]

print names[0:2]

```

### Assigning to Lists ###

```python

names[2] = 'Darwin'
print names

```
