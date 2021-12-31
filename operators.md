
1. Arithmetic Operators
2. Post and Pre increment/decrement operators
3. Comparision Operators
4. Logical Operators
5. Bitwise Operators -- pending
6. Assignment Operator
7. Compound Assignment Operators

# Arithmetic Operators
Applicable only for Integers
+, -, *, /, %

/ --> will return only quotient.

# Post and Pre increment/decrement operators

++, --
```
uint a = 10;
uint b = 20;
uint x = a++; // post increment of A so x will be assigned first a then a will be incremented by 1
              // x = a;
              // a = a+1;
uint y = ++a; // pre increment of A so a will be incremented by 1 first then y will be assigned updated value of a
              // a = a+1;
              // y = a;

// similarly -- operator

x = b--; // post decrement
y = --b; // pre decrement

```

These can also be used along with arithmetic operators.
```
x = b + b++ + ++b - --a + a++; // valid statement
```

# Comparision Operators

<, >, <=, >=, ==, !=

Comparison will return with true or false only.
Note: implicit conversion to uint won't happen (true/false doesn't reflect Non Zero and Zero)

- With integers all these operators can be used.
- With booleans only equality operators can be used (== and !=) as </> doesn't make sense for booleans.
- With strings these operators cannot be used.

```
uint a = 10;
uint b = 20;

bool x;
x = a < b; // true
x = a > b; // false
x = a <= b; // true
x = a >= b; // false
x = a == b; // false
x = a != b; // true

bool a = false;
bool b = true;
bool x;
x = a < b; // invalid statement ( < incompatible with type bool, bool)
x = a > b; // invalid statement
x = a <= b; // invalid statement
x = a >= b; // invalid statement
x = a == b; // false
x = a != b; // true

string a = "Hello";
string b = "World";
bool x;
x = a < b; // invalid statement ( < incompatible with type string, string)
x = a > b; // invalid statement
x = a <= b; // invalid statement
x = a >= b; // invalid statement
x = a == b; // invalid statement
x = a != b; // invalid statement
```

# Logical Operators

&& - Logical AND
|| - Logical OR
!  - Logical NOT

These are for somewhat creating chains for comparision

&& -- both sides must be true for overall to be true
      if one condition returns false then remaining conditions won't be checked.
|| -- atleast one side must be true
      if one condition returns true then remaining conditions won't be checked.
!  -- negate the result.
      This cannot be assigned to any variable but can only be used in chaining or conditions like in if()

```
uint a = 10;
uint b = 20;
uint x;
if ( a <= 100 && b <= 20 ){
    x = a;
} else if ( a >= 100 || b < 200 && !(a <= b) ) {
    x = b;
} else {
    x = a + b;
}
```

# Assignment Operator

= Used to assign values
```
uint a = 10;
bool b = false;
string x = "Hello World";

uint c = a; // assign value of a to c
uint d = a = 200; // first assign 200 to a and then value of a to d

// in case of return statement assignment can be possible
return a = b; // assign value of b to a and then return value of a.

// while calling functions we can use assignment for passing values
contract DecisionMaking {
    function getSum(uint a, uint b) public pure returns(uint) {
        return a+b;
    }
    function getResult() public pure returns(uint) {
        uint a = 10;
        uint b = 20;
        uint c = getSum(a=b,b=200); // return 220 (a=20, b=200)
        return c + b; // return 420 (c = 220, b = 200)
    }
}
```

# Compound Assignment Operators

+=, -=, *=, /=, %=

```
uint x = 10;
uint y = 20;
x += y; // this is equal to x = x + (y);
x += x*y - x/y; // this is equal to x = x + (x*y - x/y);
x += x = 200; // 400 - valid statement ==> x = x + x (after assignment x = 200) so 400
```

# Sample Code to check if two numbers are multiples or not
```
    function checkMultiples(uint _a, uint _b) public pure returns(bool) {
        if ( _a%_b == 0 || _b%_a == 0) {
            return true;
        }
        return false;
    }
```


