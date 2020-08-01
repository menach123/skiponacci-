
### The Skiponacci Sequence

Your task is to generate the Fibonacci sequence to n places, with each alternating value as "skip". For example:
```
"1 skip 2 skip 5 skip 13 skip 34"
```
Return the result as a string

You can presume that n is always a positive integer between (and including) 1 and 64.


```
fib_sequence = [1 , 1 ]

for i in range(64-2):
    fib_sequence.append(sum(fib_sequence[-2:]))
def skiponacci(n):
    sequence = []
    for i in range(n):
        if(i+1)%2 != 1:
            sequence.append('skip')
        else:
            sequence.append(str(fib_sequence[i]))
    sequence = sequence[:-1] if sequence[-1] == 'skip' else sequence
    return ' '.join(sequence)
    
```

#### Using function from <a href=https://www.javatpoint.com/python-display-fibonacci-sequence-recursion>Python Program to Display Fibonacci Sequence Using Recursion</a>


```
skiponacci(1) == "1"

```




    True




```
skiponacci(5) == "1 skip 2 skip 5"

```




    True




```
skiponacci(7) == "1 skip 2 skip 5 skip 13"
```




    True




```
skiponacci(5)
```




    '1 skip 2 skip 5'




```

```
