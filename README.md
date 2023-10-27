# python-interview-tasks

Here are two simple python programming tasks we would like you to implement using your preferred IDE. Talk it thru as you do the task.

## Task 1: Pull some data elements from a data structure and output a list.

Source JSON data:

 [ 
   { 
      "id":1,
      "patient":"Steve",
      "readings":[ 
         "100",
         "101"
      ]
   },
   { 
      "id":2,
      "patient":"Allen",
      "readings":[ 
         "200",
         "201"
      ]
   }
]


Expected Output:

["Steve", "Allen"]

<details>
  <summary><i>Solution</i></summary>
  <b>
```python
import json

trialDataJson = """[ 
   { 
      "id":1,
      "patient":"Steve",
      "readings":[ 
         "100",
         "101"
      ]
   },
   { 
      "id":2,
      "patient":"Allen",
      "readings":[ 
         "200",
         "201"
      ]
   }
]"""

data = []
try:
    data = json.loads(sampleJson)
except Exception as e:
    print(e)

dataList = [item.get('patient') for item in data]
print(dataList)
```
</b>
</details>


## Task 2: Remove duplicates from a list and create a tuple and find the minimum and maximum number


Source data:

sample_list = [87, 45, 41, 65, 94, 41, 99, 94]

Expected Outcome:

unique items [87, 45, 41, 65, 99]
tuple (87, 45, 41, 65, 99)
min: 41
max: 99

<details>
  <summary><i>Solution</i></summary>
```
sample_list = [87, 52, 44, 53, 54, 87, 52, 53]

print("Original list", sample_list)

sample_list = list(set(sample_list))
print("unique list", sample_list)

t = tuple(sample_list)
print("tuple ", t)

print("Minimum number is: ", min(t))
print("Maximum number is: ", max(t))
```
</details>