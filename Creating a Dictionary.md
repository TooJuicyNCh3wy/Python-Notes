Dictionaries in Python are used to store data values in key:value pairs. A dictionary is a collection which is ordered*, changeable, and does not allow duplicates. Here's how you can create a dictionary:
```
user_info = {
    "name": "Faizan",
    "age": 23,
    "city": "New York"
}
```
You can access the values by referring to their keys:
```
print(user_info["name"])  # Output: Faizan
```
Dictionaries are flexible and can have keys and values added, modified, or removed.
```
# Adding a new key-value pair
user_info["country"] = "USA"
print(user_info) # {'name': 'Faizan', 'age': 23, 'city': 'New York', 'country': 'USA'}


# Modifying an existing key's value
user_info["age"] = 26
print(user_info) # {'name': 'Faizan', 'age': 26, 'city': 'New York', 'country': 'USA'}


# Removing a key-value pair
del user_info["age"]
print(user_info) # {'name': 'Faizan', 'city': 'New York', 'country': 'USA'}
```
