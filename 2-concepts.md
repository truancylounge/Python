# Python Concepts

1. **Fundamental Data Types**: int, float, bool, str, list, tuple, dict, set
2. **Classes**: Custom data types
3. **Specialized Data Types**: Modules that can used
4. None
5. **Variables** naming conventions:
   - snake_case, e.g first_name = 'Ken'
   - Start with lowercase or underscore
   - Case sensitive
6. **Constants** naming convention: All caps, e.g PI = 3.14

## Useful Commands
1. **type**("Hi How are you?") => <Class 'str'>
2. **Multi line string** => ''' MultiLine text here '''
3. **Type conversion** => int("100") or str(100)
4. **Formatted String** => print(f'hi {name}. you are {age} years old') 
   Above is similar to string format command 'hi {name}. you are {age} years old'.format(name='lalith', age=100)
5. String Indexes: 
    - first_name = 'lalith'
    - first_name[0:4] => 'lali', **start:end:stepover**
    - first_name[1:] => 'alith'
    - first_name[:4] => 'lali'
    - first_name[::2] => 'llt'
    - first_name[-1] => 'h', starts from end of string
6. Reverse a string, first_name[::-1]
   - **Join**, ','.join(['Hi my name is', 'Lalith'])
7. **Lists**: Ordered sequence of objects of any type
   - All string slicing operations above apply here
   - List slicing creates a new copy
   - To copy a new list new_cart = cart[:] => Creates a new list
   - new_cart = cart => Both lists refer to same memory location, no new list created
8. List Methods:
   - **Length**, **len(sample_list)** returns length of the array
   - **Append**, Adds object to end of the list, **sample_list.append(100)**
   - **Insert**, Adds object at an index, **sample_list.insert(index, object)**
   - **Extend**, Add another list, **sample_list.extend([1, 45, 56])** or sample_list.extend(sample_list1)
   - **pop**, removes last object or object at an index
     - Removes last object from list, **sample_list.pop()**
     - If given an index, removes the object at the index, **sample_list.pop(0)**
   - **remove**, given object from the list **sample_list.remove('notebook')**
   - **clear**, removes all objects from the list, **sample_list.clear()**
   - **index**, returns index at which the object appears in the list, **sample_list.index('notebook')**
   - **in**, Check if object exists in a list, **print('notebook' in sample_list)** or **print('notebook' in "I have a notebook")**
   - **count**, return number of times an object appears in the list, **sample_list.count('notebook')**
   - **copy**, return a new list, **sample_list.copy()** similar to **sample_list[:]**
   - **sort**, sorts objects in the existing list, **sample_list.sort()**
   - **sorted**, returns a new sorted list but doesn't modify existing list, **sample_list2 = sorted(sample_list)**
   - **reverse**, modifies existing list by reversing the elements, **sample_list.reverse()** different from **sample_list[::-1]**, which return a new reversed list
   - sample_list[1] = 'Z', updates the index 1 value to Z since **lists are mutable**. Tuple is immutable. 
9. Common List Patterns:
   - **range**, create a new list with values 0 to 99, **list(range(100))** or values from 1 to 99, **list(range(1,100))**
   - **List Unpacking**, e.g a,b,c,*sample_list = [1,2,3,'test1','test2','test3'], * is used to create a sublist
10. **Dictionary**, similar to hash tables or maps, essentially a key/value pair
    - Dictionary is an **unordered key/value pair** i.e. they aren't store contiguously in memory
    - On print(dict), the order could be different
    - Dictionary keys if not unique, when retrieved the values will be of the last key
   ```python
   sample_dict = {
      'a': [1,2,3],
      'b': 'Hello World',
      'c': True
   }
   print(sample_dict['a'][1])
   ```
11. Dictionary Methods:
      - **get**, If we access a key that's not in the Dictionary python errors out.
      - To avoid this use get() which returns None, **sample_dict['age']** errors out instead use sample_dict.get('age')
      - We can also return a default value, **sample_dict.get('age', 40)** returns default 40 if no age exists.
      - **keys**, returns a list of keys in the dict, **print('b' in sample_dict.keys())**
      - **values**, returns a list of values in the dict, **print('Hello World' in sample_dict.values())**
      - **items**, return all key/value pairs as Tuple, **print(sample_dict.items())**
      - **clear**, removes all key/value pairs, **sample_dict.clear()**
      - **copy**, returns a new dictionary i.e clone, **sample_dict2 = sample_dict.copy()**
      - **pop**, returns value of the key and also remove it from the dictionary, **value = sample_dict.pop('b')**
      - **update**, if a key exists will update its value, if not it will create a new key/value and add it, **print(sample_dict.update({'c': False}))**
12. **Tuple**, Similar to lists but immutable
      - All methods on lists apply on tuple as well.
      - my_tuple = (1,2,3,4,5)
      - my_tuple[1]
      - print(5 in my_tuple)
      - Cannot sort or reverse a tuple as its immutable. As a result tuples are faster than lists
      - slicing operators work on tuples too, return a new tuple
        - new_tuple = my_tuple[1:4]
        - x,y,z,*other = (1,2,3,4,5), here other would be [4,5]
      - **length**, print(len(my_tuple))
      - **count**, print(my_tuple.count(5)), returns number of times 5 exists in tuple
      - **index**, print(my_tuple.index(2))
13. Sets, unordered collection of unique objects
      - Convert a list of duplicate items to a set of unique items
        - **unique_elements = set(sample_list)**, returns only unique items
      - **copy**, new_set = my_set.copy()
      - **clear**, my_set.clear() empties the set
      - **discard**, **my_set.discard('phone')**, removes object from the set
14. Set Advanced Methods, 
    - my_set = {1,2,3,4,5} your_set = {4,5,6,7,8,9,10}
    - **difference**
      - my_set.difference(your_set), returns {1,2,3}
    - **difference_update**
      - removes all elements of another set from this set
      - my_set.difference_update(your_set) returns {1,2,3}
      - This might look similar to difference, but here my_set gets updated but with difference it only returns the elements doesn't update my_set
    - **intersection**
      - my_set.intersection(your_set), returns {4,5}
      - shorthand, **print(my_set & your_set)**
    - **isdisjoint**, return True is sets have items in common
      - my_set.isdisjoint(your_set) is False coz there are items in common
    - union, adds 2 sets and removes duplicates if any
      - my_set.union(your_set) 
      - shorthand, **print(my_set | your_set)**
    - 
15. 




## Resources
1. replit to run python code, https://replit.com/
   - change .replit file to update entrypoint
2. w3schools tutorial, https://www.w3schools.com/python/default.asp
3. 