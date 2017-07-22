# Interview-Questions-Python

<ul>
<li>How Python types can be splitted in two categories? 
<ul> 
<li>Immutable types(tuple, str, int, float) We can't change the value of 
immutable type. 

`The value of the variable changes, but it changes by changing what the variable refers to. A mutable type can change that way, and it can also change "in place".`
Consider following piece of code:
```python
lst = []
s = ""
print(id(lst), id(s))
lst += [1]
s += 'bar' 
print(id(lst), id(s))  
```
The value of id(lst) remains the same, while the id(s) changes because it 
refers to a new object.
</li>
<li> Mutable Types(list, dict, set)
We can change the value of mutable type "in place".

</li>
</ul>
</li>

<li>
What's decorator in Python? What the decorator should return? What are they 
used for?
<p>
 A Python decorator is a specific change to the Python syntax that allows us to more conveniently alter functions and methods (and possibly classes in a future version).
 This is ideal when you need to extend the functionality of functions that you don't want to modify. 
</p>
Decorator should return a "decorated" object. Actually, decorator is just a 
syntax sugar that can be changed to the following piece of code:
 
```python
@change
def f(*args, **kwargs):
   pass
```
Is identical to:
 
```python
def f(*args, **kwargs):
   pass
f = change(f)
```


In Python function are first class objects, they can be assigned, passed to 
another functions as arguments etc. Another important property to 
understanding decorators is <b> closure </b>. Which actually means that:
<quote>
Inner functions have access to the enclosing scope
</quote>

<a> https://www.thecodeship.com/patterns/guide-to-python-function-decorators/
 </a>
</li>
<li>
What is generator? How it differs from iterator?
</li>
<li>
What's average lookup time in Python dict? Why can't we use mutable types as 
keys of dict?
</li>
<li>
What are metaclasses? What methods they should implement?
Prepare method in metaclasses
</li>
<li> What is Singleton? How would you implement it in Python?
</li>
<li>
How is implemented Python attribute access?
</li>
<li>
How modules are imported in Python? importlib
</li>
What will be the result of the following code?
 
```python
a = [0]
lst = [a]*5
lst[0].append(1)
```
</li>
<li>
How Python subclasses work? MRO
</li>
<li>
What will the following code produce?

```python
class A(object):
    x = 1
 
class B(A):
    pass
 
class C(A):
    pass
 
print A.x, B.x, C.x
B.x = 2
print A.x, B.x, C.x
A.x = 3
print A.x, B.x, C.x
```
</li>


</ul>
