
> [!note] 
>  When we working with tabular data, in important to organize rows and columns following the next principles:
    1. Each row corresponds to a single house in our dataset. We will call each of these houses an **observation**
    2. Each column corresponds to a characteristics of each house. We'll call these **features**.
    3. Each cell contains only **one value**.

# Lists
> [!info] 
> In python, a list is a collection of data that stores multiples items in a single variable.
>  These items can be change and can be duplicated.
>  A list can store data of multiple type, not all items in the list need to be the same type.

- Python comes with several data structures that we can to organize tabular data.
````python
# Declare variable
house_0_list = [115910.26, 128, 4]
# Type of variable
print(f"house_0_list type is {type(house_0_list)}")
# Lengt of variable 
print(f"The length of house_0_list is: {len(house_0_list)}")
# Get output of variable
house_0_list
````

- **Append an item to a list**

