
# Arrays

fixed sized arrays and dynamic sized arrays

variables and methods avilable
1. .length : returns length of array *applicable to both fixed/dynamic sized arrays*
2. .push(value) : add value at the end of array *applicable only for dynamic sized arrays*
3. .pop() : remove last element of array *applicable only for dynamic sized arrays*

4. delete array[index]; : this will delete the value but won't change the length of the array

### Different ways of declaring and initialising arrays
```
    // dynamic sized arrays
    uint[] arr;
    uint  []  arr;
    uint  [  ] arr;
    uint []d;
    // uint arr[]; // invalid declaration

    // fixed sized arrays
    uint[5] arr; // all elements initialised with 0 i.e. arr[0] = 0, arr[1] = 0 so on...
    uint[5] arr = [1,2,3,4,5];
    uint[5] arr = [1,2]; // remaining elements initialised with 0
    uint[2] arr = [1,2,3,4,5]; // Invalid once sized is fixed we can't elements more than that.
```

### Adding and deleting elements from dynamic sized arrays
```
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;

contract Base {

    uint[] arr;

    function push(uint _value) public {
        arr.push(_value);
    }

    function pop() public {
        arr.pop();
    }

    function deleteAt(uint _index) public { // ordering will be changed
        // delete arr[_index]; // will mark _index as deleted
        arr[_index] = arr[arr.length-1];
        arr.pop();
    }

    function array() public view returns(uint[]  memory) {
        return arr;
    }
}
```

### deleting from fixed sized arrays
```
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;

contract Base {
    uint[5] a = [1,2,3,4,5];
    function deleteFixedArrayindex(uint _index) public {
        delete a[_index]; // mark 0 at the _index
    }
    function arrayA() public view returns(uint[5]  memory) {
        return a;
    }
}
```




