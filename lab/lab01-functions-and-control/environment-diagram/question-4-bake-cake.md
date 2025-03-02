# Question 4: Bake Cake

Draw the environment diagram of the following code.

```python
def square(x):
    return x * x

def bake(cake, make):
    if cake == 0:
        cake = cake + 1
        print(cake)
    if cake == 1:
        print(make)
    else:
        return cake
    return make

cake = square(0)
bake(cake, 29)
```

You can view the correct environment diagram [here](https://pythontutor.com/render.html#code=def%20square%28x%29%3A%0A%20%20%20%20return%20x%20*%20x%0A%0Adef%20bake%28cake,%20make%29%3A%0A%20%20%20%20if%20cake%20%3D%3D%200%3A%0A%20%20%20%20%20%20%20%20cake%20%3D%20cake%20%2B%201%0A%20%20%20%20%20%20%20%20print%28cake%29%0A%20%20%20%20if%20cake%20%3D%3D%201%3A%0A%20%20%20%20%20%20%20%20print%28make%29%0A%20%20%20%20else%3A%0A%20%20%20%20%20%20%20%20return%20cake%0A%20%20%20%20return%20make%0A%0Acake%20%3D%20square%280%29%0Abake%28cake,%2029%29\&cumulative=true\&curInstr=15\&heapPrimitives=nevernest\&mode=display\&origin=opt-frontend.js\&py=3\&rawInputLstJSON=%5B%5D\&textReferences=false).
