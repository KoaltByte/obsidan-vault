#Operations #TypeNumbers #List #Tuple #Dictionary 
# Simple calculations

| Operation         | Symbol | Example |
| ----------------- | ------ | ------- |
| Addition          | +      | 1+9     |
| Substraction      | -      | 6-3     |
| Division          | /      | 4/2     |
| Multiplication    | *      | 4*5     |
| Exponents         | **     | 4**2    |
| Rest              | %      | 8%3     |
| Absolute division | //     | 9//4    |

# Data types
- <mark style="background: #D2B3FFA6;"> Boolean (bool):</mark>
	- Any data which can be espressend as either True  or False.
	- Used when comparing two values. For example, if you enter 10 > 9, Python will return True.
- <mark style="background: #D2B3FFA6;">String (str)</mark>
	- Data that involves test, either letters, numbers, or special characteres.
	- Strings are enclosed in etither sigle or double quotes.
- <mark style="background: #D2B3FFA6;">Numeric (int, float, complex)</mark>
	- Integrer or int is a whole number, positive or negative, whitout decimals, of unlimted length.
	- A floating-point number, or float, is a number positive or negative, containing one or more decimals.
	- A complex are imaginary number, designated by j.

# Sequence (list, tuple, set)
- `list`: 
	- Is collection that is ordered and changeable.
	- It is disignated using square brackets `[ ]` .
	- Items can be of different data types `["red", 1, 1.03, 1]`
- `tuple`: 
	- It is a collection which is ordered and unchangeable.
	- It is disignated using parentheses `()` `("red", 1, 1.03, 1)`.
- `set`: 
	- Is a collection wich is unordered, unchangeable.
	- Does not permit duplicate items.
	- It is designated using curly brackets `{ }` `{"red", 1, 1.03}`

# Mapping (dict)
- `Dictionaries`:
	- Store data *key-value* pairs.
	- They are designated using curly brackets `{ }` like a set, but notice that keys and values are associated with each other using a colon `:`.
	- Each pair is separated from the next using a comma `,`.
````python
dict1 = {
	"department" : "quindio",
	"property_type" : "house",
	"price_usd" : 330899.98	
}
````

- <mark style="background: #D2B3FFA6;">Binary (bytes, bytearray, memoryviwe):</mark>
	- Used to manipulate and display binary data.
	- Can be expressed with integers.
	- Unlike the other data types. binary types are not human-readable.

