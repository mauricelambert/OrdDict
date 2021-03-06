# OrdDict

## Description
This package implement an order dict.

## Requirements
 - Python 3
 - Standard library

## Installation
```
pip install OrdDict
```

## Example
```python
from OrdDict import OrdDict

order_dict = OrdDict({ "key1" : "value1", "key2" : "value2" }, { "key3" : "value3" }, key4 = "value4")
order_dict["key6"] = "value6"
order_dict.insert(4, "key5", "value5")
order_dict.deplace(5, "key5")
order_dict.delete("key6")
order_dict.update({ "key6" : "value6" })

for i, (key, value) in enumerate(order_dict.items()) :
	print(f"{i} {key} {value}")

order_dict.remove(5)
order_dict.reverse()

order_dict = order_dict + { "key7" : "value7" }
order_dict += { "key8" : "value8" }
del order_dict["key8"]
copy = order_dict.copy()

for i, a in enumerate(reversed(order_dict)) :
	print(f'{i} {a} {order_dict.get_from_index(i)}')

copy.delete_from_index(0)
copy.clear()

keys = order_dict.to_dict()
len(order_dict)

order_dict.insert(0, "key0", "value0")

for value in order_dict.values() :
	print(value)

for key in order_dict.keys() :
	print(key)

for key in order_dict :
	print(key)

value = order_dict.get("key0")
value = order_dict.get("not a key")

value = order_dict.setdefault("key0", "a default value")
value = order_dict.setdefault("new key", "new value")

index = order_dict.index("new key")
index = order_dict.index_from_value("new value")

value = my_ord_dict.value_from_index(index)
key = my_ord_dict.key_from_index(index)

key, value = my_ord_dict.get_from_index(index)
my_ord_dict.remove(index)

my_ord_dict.count("value0")
my_ord_dict.extend({ "key8" : "value8" })

value = my_ord_dict.pop("key8")
key, value = my_ord_dict.pop_from_index(0)

my_ord_dict.add("key0", "value0")

my_ord_dict.sort()
my_ord_dict.sort_by_values()
```

## License
Licensed under the [GPL, version 3](https://www.gnu.org/licenses/).

## Link
[Github Page](https://github.com/mauricelambert/OrdDict)