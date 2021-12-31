
# Constructors

1. One contract can have only one constractor
2. Constructor executed only once while deployment
3. Constructor can have arguments also
4. by default solidity provide default constructor with no arguments
5. constractors can be public and internal both
    - if internal then you can mark contract as abstract

```
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;

contract Base {
    string public name;
    uint public age;
    constructor(string memory _name, uint _age) public {
        name = _name;
        age = _age;
    }
}

contract DerivedA is Base('DerivedA',24) { // Valid

}

contract DerivedB is Base { // Pass values while deploying
    constructor(string memory _name, uint _age) Base(_name,_age) {}
}
```


