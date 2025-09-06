# Python Concepts

1. **Fundamental Data Types**: int, float, bool, str, list, tuple, set, dict
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
7. **Lists**: Ordered sequence of objects of any type
   - All string slicing operations above apply here
   - List slicing creates a new copy
   - To copy a new list new_cart = cart[:] => Creates a new list
   - new_cart = cart => Both lists refer to same memory location, no new list created
8. Actions on Lists:
   - **Length**, **len(sampleList)** returns length of the array
   - **Append**, Adds object to end of the list, **sampleList.append(100)**
   - 
9. 


## Resources
1. replit to run python code, https://replit.com/
   - change .replit file to update entrypoint
2. 