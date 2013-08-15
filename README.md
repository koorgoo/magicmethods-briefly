============================
python-magic-methods-briefly
============================

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

____(self)
____(self)
____(self)
____(self)
____(self)
____(self)
____(self)

#### 3.3.1 
