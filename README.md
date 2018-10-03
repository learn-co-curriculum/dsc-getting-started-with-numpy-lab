
# NumPy Lab

## Introduction

Now that we have introduced NumPy, let's put it to practice. In this lab, we are going to be creating arrays, performing operations on them, and returning new array all using the NumPy library. Let's get started!

## Objectives
* Know that numpy is imported as np: import numpy as np
* Understand how to initialize numpy arrays from nested Python lists, and access elements using square brackets
* Understand the shape attribute on numpy arrays
* Understand how to create arrays from scratch including Np.zeros, np.ones, np.full
* Learn how to do indexing in arrays
    * Slicing
    * Integer indexing
    * Boolean indexing
* Learn to perform scalar and vector math

# Import NumPy under the standard alias


```python
#Your code here
import numpy as np
```

# Generating Some Mock Data

Create a NumPy Array for each of the following:
    1. Using a range
    2. Using a Python List
    
Below, create a list in Python that has 5 elements (i.e. [0,1,2,3,4]) and assign it to the variable `py_list`. 

Next, do the same, but instead of a list, create a range with 5 elements and assign it to the variable, `py_range`.

Finally, use the list and range to create NumPy arrays and assign the array from list to the variable `array_from_list`, and the array from the range to the variable `array_from_range`.


```python
py_list = [0,1,2,3,4]
py_range = range(0,5)
array_from_list = np.array(py_list)
array_from_range = np.array(py_range)
```

Next, we have a list of heights and weights and we'd like to use them to create a collection of BMIs. However, they are both in inches and pounds (imperial system), respectively. 

Let's use what we know to create NumPy arrays with the metric equivalent values, (height in meters & weight in kg).

> **Remember:** *NumPy can make these calculations a lot easier and with less code than a list!*

> 1.0 inch = 0.0254 meters

> 2.2046 lbs = 1 kilogram


```python
# use the conversion rate for turning height in inches to meters
list_height_inches = [65, 68, 73, 75, 78]
array_height_inches = np.array(list_height_inches)
array_height_meters = array_height_inches * 0.0254
```


```python
# use the conversion rate for turning weight in pounds to kilograms
list_weight_pounds = [150, 140, 220, 205, 265]
array_weight_pounds = np.array(list_weight_pounds)
array_weight_kg = array_weight_pounds / 2.2046
```

The metric formula for calculating BMI is as follows:

> BMI = weight (kg) ÷ height^2 (m^2)

So, to get BMI we divide weight by the squared value of height. For example, if i weighed 130kg and was 1.9 meters tall, the calculation would look like:

> BMI = 130 / (1.9*1.9)

Use the BMI calculation to create a NumPy array of BMIs


```python
BMI_array = array_weight_kg / (array_height_meters * array_height_meters)
```

## Summary

In this lab, we practiced creating NumPy arrays from both lists and rages. We then practiced peforming math operations like converting imperial measurements to metric measurements on each element of a NumPy array to create new arrays with new values. Finally, we used both of our new NumPy arrays to operate on eachother and create new arrays containing the BMIs from our arrays containing heights and weights.
