---
key: d8a5ffe7600ce9865d9ef6fbd2fee35a
title: 'Insert title here'
---

## Checking PEP8 standards

```yaml
type: TitleSlide
key: 8bfb7a963e
```

`@lower_third`
name: William Murphy
title: Software Engineer & Data Engineer

`@script`
In this chapter, we will discuss the styling and formatting of our Python code. You may ask yourself, "Why is the style of my code important?". The reason is, our code will have to be read and understood by multiple people. By keeping a consistent style, other users will be able to read through and understand our code much more quickly. This saves your team's time and also lowers the possibility of errors, when other team members may be committing changes to our code.

---

## What is PEP?

```yaml
type: FullSlide
key: 218e11b491
hide_title: false
```

`@part1`
- **PEP** stands for *Python Enhancement Proposal* {{1}}
- A PEP is a design document that provides information or describes a new feature for Python {{2}}

- **PEP 0** provides a list of all the current PEPs found here: *https://www.python.org/dev/peps/* {{3}}

- **PEP 8** is Python's style guide, found here: https://www.python.org/dev/peps/pep-0008/ {{4}}

`@script`
When a developer wants to make an improvement to Python, the developer must issue a PEP, or, Python Enhancement Proposal. A PEP is a design document that provides information or describes a new feature of Python. If you are interested, PEP 0 provides a list of all the current PEPs.  PEP 8 is of particular interest to us as this describes Python's style guidelines.

---

## Making our code PEP 8 compliant

```yaml
type: FullSlide
key: eb0f02d1d9
disable_transition: false
```

`@part1`
- The `pylint` and `flake8` Python packages are two of the most popular linters for Python {{1}}

- **pylint** command line interface provides you a score out of 10 of how Pythonic your code is {{2}}

	- `pylint` does not necessarily provide **PEP 8** compatible code 
    
- **flake8** command line interface provides a list of **PEP 8** standards that are being violated. {{3}}
	- `flake8` does not provide a score of how Pythonic your code is
    
- Using both `flake8` and `pylint` together is recommended as they analyze the style of your code differently, leading to more stylistically sound code {{4}}

`@script`
There are two main Python packages that allow us to check that our code is PEP 8 compliant; they are pylint and flake8. Both pylint and flake8 are what's known as linters. A linter is a piece of software that analyzes code to check for bugs and stylistic errors. Both flake8 and pylint achieve this task but in different ways. The pylint package comes with a useful command line interface that grades the style of your code out of 10. Please keep in mind that some of the feedback from pylint is subjective and is not necessarily a violation of PEP 8.  On the other hand, the flake8 command line interface does not provide a grade but rather, it lists all the violations of PEP 8 that are contained within your code.  Using both pylint and flake8 in conjunction is recommended.

---

## Checking our code with pylint

```yaml
type: TwoRows
key: c0250577ec
```

`@part1`
```python
# Define a simple function tht will be checked with pylint
def check_with_pylint():
    print("Running pylint linter...")
```

```sh
	# run pylint linter on the module
	pylint check_with_pylint.py
```

`@part2`
```
************* Module check_with_pylint
check_with_pylint.py:8:0: C0111: Missing function docstring (missing-docstring)

<hr />---------------------------------------------------------------
Your code has been rated at 5.00/10 (previous run: 5.00/10, +0.00)
```

`@script`
Let's start with pylint. Here, we have a simple function that we will check with pylint's command line interface. To do this, open a command line and type pylint and then the name of the module that will be checked. As you can see, pylint tells us that we are missing a docstring for our function and that our score is a 5.0/10, as well as our previous run's score. If we add a docstring, our score will be a 10/10

---

## Checking our code with flake8

```yaml
type: TwoRows
key: 83026817a4
```

`@part1`
```python
"""
check_with_pylint.py
~~~~~~~~~~~~~~~~~~~~
"""

def check_with_flake8():
    print("Running flake8 linter...")
```

```bash
flake8 check_with_flake8.py
```

`@part2`
```bash
check_with_pylint.py:8:1: E302 expected 2 blank lines, found 1
```

`@script`
Now we will check our code with flake8's command line interface. To run the flake8 linter, we simply type flake8 and then the python module's name. As you can see, flake8 returns a different result. Our script is missing 2 blank lines after the module docstring; to be flake8 compliant, we must add an extra space after the module docstring.

---

## Let's practice!

```yaml
type: FinalSlide
key: e506c7b786
```

`@script`
Now it's your turn to practice making your Ptyhon code PEP 8 compliant.
