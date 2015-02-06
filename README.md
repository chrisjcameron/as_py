as_py
=====

Automator Workflow to replace selected text with the result of executing said text as a python statement

as_py.workflow should be installed in ~/Library/Services/

Select some text in an editable field and and choose as_py from the Services contextual menu or
from the <application> >> Services Toolbar menu. The selected text is replaced by the result of executing 
the selected text as a python statement. 

Current Limitations:

- Cannot handle smart quotes

Fixed:

- Module imports work as long as sys is imported last.

------------------------------------------------

Example Usage (Quote indent is the script output)

```
[ x**2 for x in range(10) ]
```
> [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

```
45.67 * 1.085
```
> 49.55195


```
for x in range(10):
    if x > 5: print(x)
    else: print(x**2)
```

> 0  
> 1  
> 4  
> 9  
> 16  
> 25  
> 6  
> 7  
> 8  
> 9  

```
x = [ 20, 30, 40]
y = [1, 2, 3]
print([ str(x)+str(y) for x,y in zip(x,y)])
```
> ['201', '302', '403']


