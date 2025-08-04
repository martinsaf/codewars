# My solution:
```bash
def correct(s):
    res = []
    for x in s:
        if x == '5':
            res.append('S')
        elif x == '0':
            res.append('O')
        elif x == '1':
            res.append('I')
        else:
            res.append(x)
    return ''.join(res)
```

# Instruction:
Character recognition software is widely used to digitise printed texts. Thus the texts can be edited, searched and stored on a computer.

When documents (especially pretty old ones written with a typewriter), are digitised character recognition softwares often make mistakes.

Your task is correct the errors in the digitised text. You only have to handle the following mistakes:

S is misinterpreted as 5
O is misinterpreted as 0
I is misinterpreted as 1
The test cases contain numbers only by mistake.
