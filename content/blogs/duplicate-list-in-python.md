---
title: "How to dupilicate a python list"
draft: false
---

If you want a copy of a list, you might do this:

```
list1 = list2
```

if you alter values in list2, you would find that the values in list1 also changed. This is because that list2 is a shallow copy of list1.  
A shallow copy is when you only copy the reference of a variable, meaning that list1 and list2 are essentially the same variables, just that it has two different names.

To create an actual "deep copy" of a variable, do:

```
import copy
list2 = copy.deepcopy(list1)
```

This will create two identical and different variables with the exact same value, a true copy, called deep copy.
A shallow copy might be what you want in some cases, but at the same time, it might cause confusing bugs if it's not your intention. Make sure to prevent this in the first place so you don't have to go into painful debugging, since your code will still run, just in a very confusing way.