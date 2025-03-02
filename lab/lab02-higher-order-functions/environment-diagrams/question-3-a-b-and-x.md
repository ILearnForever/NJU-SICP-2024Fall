# Question 3: A, B, and X

Draw the environment diagram of the following code:

```python
a = lambda x: x * 2 + 1

def b(b, x):
    return b(x + a(x))

x = 3
b(a, x)
```

After drawing the diagram, compare it to the correct one [here](https://pythontutor.com/composingprograms.html#code=a%20%3D%20lambda%20x%3A%20x%20*%202%20%2B%201%0A%0Adef%20b%28b,%20x%29%3A%0A%20%20%20%20return%20b%28x%20%2B%20a%28x%29%29%0A%0Ax%20%3D%203%0Ab%28a,%20x%29\&cumulative=true\&curInstr=13\&mode=display\&origin=composingprograms.js\&py=3\&rawInputLstJSON=%5B%5D). Then predict what would python display and submit your answer with `python ok -q q3 -u`.
