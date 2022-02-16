# Python

## List Comprehension

List comprehension is a way to create new lists, based on existing lists.

### Syntax

```
new_list = [ new_item for item in list if condition]
new_dict = { new_key:new_value for (key, value) in dict.items() if condition }
```

### Example

```
# List
list_1 = [ "2", "4", "5", "16" ]
list_2 = [ "2", "3", "5", "35" ]

shared_numbers = [ int(num) for num in list_1 if num in list_2 ]
# [2, 5]

# Dictionary
weather_c = {
  "Monday": 10,
  "Tuesday": 25,
  "Wednesday": 18
}

weather_f = { day: (temp * 9 / 5 + 32) for (day, temp) in weather_c.items() }
# {
#   "Monday": 50,
#   "Tuesday": 77,
#   "Wednesday": 64.4
# }
```

## Azure Function Powershell Issue

If you get an error about the powershell script not being signed when debugging
an azure function, run the following command from an admin powershell prompt:

```
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy Unrestricted
```

Be sure to reset it when finished

```
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy AllSigned
```
