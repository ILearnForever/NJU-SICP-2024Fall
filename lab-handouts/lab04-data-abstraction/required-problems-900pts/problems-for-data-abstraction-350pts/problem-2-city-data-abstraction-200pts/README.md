# Problem 2: City Data Abstraction (200pts)

Say we have an abstract data type for cities. A city has a name, a latitude coordinate, and a longitude coordinate.

Our ADT has one **constructor**:

* `make_city(name, lat, lon)`: Creates a city object with the given name, latitude, and longitude.

We also have the following selectors in order to get the information for each city:

* `get_name(city)`: Returns the city's name
* `get_lat(city)`: Returns the city's latitude
* `get_lon(city)`: Returns the city's longitude

Here is how we would use the constructor and selectors to create cities and extract their information:

```python
    >>> nanjing = make_city('Nanjing', 31, 118)
    >>> get_name(nanjing)
    'Nanjing'
    >>> get_lat(nanjing)
    31
    >>> beijing = make_city('Beijing', 39, 116)
    >>> get_lon(beijing)
    116
```

All of the selector and constructor functions can be found in the lab file, if you are curious to see how they are implemented. However, the point of data abstraction is that we do not need to know how an abstract data type is implemented, but rather just how we can interact with and use the data type.
