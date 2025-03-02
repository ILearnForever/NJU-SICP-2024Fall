# Problem 5: Protected Secret (100pts)

Write a function `protected_secret` which takes in a `password`, `secret`, and `num_attempts`.

`protected_secret` should return another function which takes in a password and prints `secret` if the password entered matches the `password` given as an argument to `protected_secret`. Otherwise, the returned function should print "INCORRECT PASSWORD". After `num_attempts` incorrect passwords are used, the secret is locked forever and the function should print "SECRET LOCKED".

We recommend you using self-referencing functions to achieve this problem.

For example:

```python
>>> my_secret = protected_secret("sicp2022", "I love python.", 1)
>>> # Failed attempts: 0
>>> my_secret = my_secret("sicp2022")
I love python.
>>> # Failed attempts: 0
>>> my_secret = my_secret("abcdefg")
INCORRECT PASSWORD
>>> # Failed attempts: 1
>>> my_secret = my_secret("NanjingUniversity")
SECRET LOCKED
```

See the doctests for a detailed example.

```python
def protected_secret(password, secret, num_attempts):
    """
    Returns a function which takes in a password and prints the SECRET if the password entered matches
    the PASSWORD given to protected_secret. Otherwise it prints "INCORRECT PASSWORD". After NUM_ATTEMPTS
    incorrect passwords are entered, the secret is locked and the function should print "SECRET LOCKED".

    >>> my_secret = protected_secret("correcthorsebatterystaple", "I love NJU", 2)
    >>> # Failed attempts: 0
    >>> my_secret = my_secret("hax0r_1")
    INCORRECT PASSWORD
    >>> # Failed attempts: 1
    >>> my_secret = my_secret("correcthorsebatterystaple")
    I love NJU
    >>> # Failed attempts: 1
    >>> my_secret = my_secret("hax0r_2")
    INCORRECT PASSWORD
    >>> # Failed attempts: 2
    >>> my_secret = my_secret("hax0r_3")
    SECRET LOCKED
    >>> my_secret = my_secret("correcthorsebatterystaple")
    SECRET LOCKED
    """
    def get_secret(password_attempt):
        "*** YOUR CODE HERE ***"
    return get_secret
```
