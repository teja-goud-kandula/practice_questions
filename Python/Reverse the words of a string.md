Question: 
Reverse the words of a string without using any functions.

Input:
alpha beta gamma

Output:
gamma beta alpha

```
def words_of_string_reversed(input_str):
    word = ''
    reversed_string = ''
    for ch in input_str:
        if ch != ' ':
            word = word + ch
        elif reversed_string == '':
            reversed_string = word
        else:
            reversed_string = word + ' ' + reversed_string
            word = ''

    reversed_string = word + ' ' + reversed_string

    return reversed_string

print(words_of_string_reversed('alpha beta gamma'))
```