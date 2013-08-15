=============================
Python Magic Methods. Briefly
=============================
Reference for https://github.com/RafeKettler/magicmethods.

## 2 Construction and Initialization

    __new__(cls, [...)
    __init__(self, [...)
    __del__(self)


## 3 Making Operators Work on Custom Classes
### 3.1 Comparison magic methods

    __cmp__(self, other)  # Removed in Python 3.
    __eq__(self, other)
    __ne__(self, other)
    __lt__(self, other)
    __gt__(self, other)
    __le__(self, other)
    __ge__(self, other)


### 3.2 Numeric Magic Methods
#### 3.2.1 Unary operators and functions

    __pos__(self)
    __neg__(self)
    __abs__(self)
    __invert__(self)
    __round__(self, n)
    __floor__(self)
    __ceil__(self)
    __trunc__(self)
    
### 3.3 Normal arithmetic operators

    __add__(self, other)
    __sub__(self, other)
    __mul__(self, other)
    __floordiv__(self, other)
    __div__(self, other)  # Removed in Python 3.
    __truediv__(self, other)
    __mod__(self, other)
    __divmod__(self, other)
    __pow__
    __lshift__(self, other)
    __rshift__(self, other)
    __and__(self, other)
    __or__(self, other)
    __xor__(self, other)

#### 3.3.1 Reflected arithmetic operators

    __radd__(self, other)
    __rsub__(self, other)
    __rmul__(self, other)
    __rfloordiv__(self, other)
    __rdiv__(self, other)
    __rtruediv__(self, other)  # Works only when from __future__ import division.
    __rmod__(self, other)
    __rdivmod__(self, other)
    __rpow__
    __rlshift__(self, other)
    __rrshift__(self, other)
    __rand__(self, other)
    __ror__(self, other)
    __rxor__(self, other)
    
#### 3.3.2 Augmented assignment

    __iadd__(self, other)
    __isub__(self, other)
    __imul__(self, other)
    __ifloordiv__(self, other)
    __idiv__(self, other)
    __itruediv__(self, other)
    __imod__(self, other)
    __ipow__
    __ilshift__(self, other)
    __irshift__(self, other)
    __iand__(self, other)
    __ior__(self, other)
    __ixor__(self, other)
    
#### 3.3.3 Type conversion magic methods

    __int__(self)
    __long__(self)
    __float__(self)
    __complex__(self)
    __oct__(self)
    __hex__(self)
    __index__(self)
    __trunc__(self)
    __coerce__(self, other)  # Removed in Python 3.

## 4 Representing your Classes

    __str__(self)
    __repr__(self)
    __format__(self, formatstr)
    __hash__(self)
    __nonzero__(self)  # Renamed to __bool__ in Python 3.
    __dir__(self)

## 5 Controlling Attribute Access

    __getattr__(self, name)
    __setattr__(self, name, value)
    __delattr__(self, name)
    __getattribute__(self, name)
    
## 6 Making Custom Sequences
### 6.2 The magic behind containers

    __len__(self)
    __getitem__(self, key)
    __setitem__(self, key, value)
    __delitem__(self, key)
    __iter__(self)
    __reversed__(self)
    __contains__(self, item)
    __missing__(self, key)
    
## 7 Reflection

    __instancecheck__(self, instance)
    __subclasscheck__(self, subclass)
    
## 9 Callable Objects

    __call__(self, [args...])
    
## 10 Context Managers

    __enter__(self)
    __exit__(self, exception_type, exception_value, traceback)
    
## 11 Building Descriptor Objects

    __get__(self, instance, owner)
    __set__(self, instance, value)
    __delete__(self, instance)
    
## 12 Copying

    __copy__(self)
    __deepcopy__(self, memodict)

## 13 Pickling
### 13.2 Pickling your own Objects

    __getinitargs__(self)
    __getnewargs__(self)
    __getstate__(self)
    __setstate__(self, state)
    __reduce__(self)
    __reduce_ex__(self)
