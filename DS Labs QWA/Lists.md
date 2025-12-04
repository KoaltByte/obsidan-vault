> [!info] 
> A list a collection of data that stores multiple items on a single variable. These items must be ordered, able to be  changed and can be duplicated. Can store data of multiple types.

# Creating list
- List can be as long or as short as you like. 
- List are written with square brackets `[ ]`.
- The next code for a short list that shows the price of houses in US 
````python
price_us = [97919.38, 300511.20, 293758.14]
print(price_us)
````

# Working with lists
- We can access any item on the list by referring to the item's index number.
- In python the first item is always 0.
````python
print(price_us[1])
````

# Append items
- To add an item to a list that already exists, using the append method
````python
price_use.append(540244.86)
````

# Analysis whit operations
- We can do analysis with the values in the list, for example:
	- If we wanted to know the total value in US dollars of the houses on our price_us list
	````python
	total_usd = sum(price_us)
	````
	- We can use 2 or more methods to obtain a new value:
````python
	average_usd = sum(price_us)/len(price_uds)
````



# Summary

| What do it do?   | Syntax                        |
| ---------------- | ----------------------------- |
| Crating list     | `list_name = [value1,2,3,x]`  |
| Print all values | `print(list_name`             |
| Access to a item | `print(list_name[index]`      |
| Add an item      | `list_name.append(new_value)` |
|                  |                               |
