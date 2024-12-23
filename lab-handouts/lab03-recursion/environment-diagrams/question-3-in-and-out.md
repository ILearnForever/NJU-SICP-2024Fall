# Question 3: In and Out

Draw the environment diagram of the following code:

```python
x = 3
def out(g, m):
    x = 5 * m
    def inner():
        return x
    if m == 0:
        return g
    else:
        return out(inner, m-1)
v = out(out, 1)()
```

After drawing the diagram, compare it to the correct one [here](https://pythontutor.com/cp/composingprograms.html#code=x%20%3D%203%0Adef%20out%28g,%20m%29%3A%0A%20%20%20%20x%20%3D%205%20*%20m%0A%20%20%20%20def%20inner%28%29%3A%0A%20%20%20%20%20%20%20%20return%20x%0A%20%20%20%20if%20m%20%3D%3D%200%3A%0A%20%20%20%20%20%20%20%20return%20g%0A%20%20%20%20else%3A%0A%20%20%20%20%20%20%20%20return%20out%28inner,%20m-1%29%0Av%20%3D%20out%28out,%201%29%28%29\&cumulative=true\&curInstr=0\&mode=display\&origin=composingprograms.js\&py=3\&rawInputLstJSON=%5B%5D). Then predict what would python display and submit your answer with `python ok -q q3 -u`.
