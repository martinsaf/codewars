# My solution:
```bash
def reverse_words(text):
    res = ""
    word = ""
    for char in text:
        if char != " ":
            word+= char
        else:
            res+= word[::-1] + " "
            word = ""
    
    res += word[::-1]
    
    return res
```

# Instructions:
Complete the function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.

Examples
"This is an example!" ==> "sihT si na !elpmaxe"
"double  spaces"      ==> "elbuod  secaps"
