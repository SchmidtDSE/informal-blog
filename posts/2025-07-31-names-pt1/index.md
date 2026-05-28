---
title: "Software engineering for scientists: Naming things (part 1)"
date: "2025-07-31"
author:
  - "Schmidt DSE Tech Team"
image: "nametag.png"
---

Do you dread opening a certain code file?
Do you have a rat's nest of `if`/`then` statements?
Do you have to read paragraphs of comments to know what's going on?
Do you often use `print` statements when you need to understand what your code is doing?

Your code likely has a lot of "things" in it, but not enough names for your things.


## Names are important

TODO: Why?

Self-documentation (error messages)
Discoverability
Cognitive load


## How to know when to give things names

TODO: Rules of thumb

WET/DRY (rule of 3)
Lots of (and/or lengthy) comments


### If this sounds familiar, you need more names!

If you're seeing any of these common indicators, that might be a sign that you need more
names.
Names can take the form of function names, class names, module names, or variable
names.
You can always make more names by grouping your code under a new construct like a
variable, a function, or a module.

**We'll follow this blog post up with more on how to use names in each of these cases!**


## Examples

The programs below are functionally identical, but better names make a huge difference
in the readability and maintainability.


### Before names:

```python
b_1 = 5
x_1 = 10
b_2 = 5
x_2 = 10
m_1 = 0.75
m_2 = 0.5

def y(m, x, b):
    return m * x + b

y_1 = y(m=m_1, x=x_1, b=b_1)
y_2 = y(m=m_2, x=x_2, b=b_2)

print(f"After {x_1} years in a greenhouse, your plant would be {y_1} inches tall")
print(f"After {x_2} years outdoors, your plant would be {y_2} inches tall")
```

### After names!

```python
def get_plant_height(start_inches, years, inches_per_year):
    return inches_per_year * years + start_inches

transplant_height = 5
experiment_years = 10

greenhouse_inches = get_plant_height(
    start_inches=transplant_height,
    years=experiment_years,
    inches_per_year=0.75,
)

outdoor_inches = get_plant_height(
    start_inches=transplant_height,
    years=experiment_years,
    inches_per_year=0.5,
)

print(f"After {experiment_years} years in a greenhouse, your plant would be {greenhouse_inches} inches tall")
print(f"After {experiment_years} years outdoors, your plant would be {outdoor_inches} inches tall")
```
