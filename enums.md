
# enums

Restrict values for a values
used when a variable is demands to a value from a list of values.
like a custom data type
When used in return statements then it returns the index of value used
We can pass from external by index of the enum values
### Creating enum and declaring enum type variable and assigning enum value

```
enum size {LARGE, MEDIUM, SMALL} // No semi-colon is used at the end
size small = size.SMALL; // enum-name variable-name = enum-name.VALUE
size small = size(0); // Valid (index) this will asign LARGE but recommended is above notation
```

#### Sample Code
```
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;

contract Base {
    enum tshirtSize {LARGE, MEDIUM, SMALL} // 0, 1, 2
    tshirtSize public t;
    tshirtSize constant defaultTSize = tshirtSize.MEDIUM;
    function getDefaultTSize() public pure returns(tshirtSize) {
        return defaultTSize;
    }
    function setSmallTSize() public {
        t = tshirtSize.SMALL;
    }
    function getTSize() public view returns(tshirtSize) {
        return t;
    }
}
```




