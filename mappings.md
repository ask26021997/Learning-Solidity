
# mapping data type

- key => value pairing
- e.g. address to balance

1. keys are stored as keccak256
2. keys can be any type except mapping, dynamic array, contract enum struct
3. values can be any type including mapping
4. if no key exists is mapping then it will return false value and no errors
5. delete will set value to false.

```
    mapping(address => uint) balances;
    // mapping(key-type => value-type) variable-name;
    // keys will be used as an index just like used in arrays
    // variable-name[key1] = value1; // save mapping between key1 and value1 in this mapping
    // variable-name[key1]; // returns value1
    // delete variable-name[key1];
```

### Sample example
```
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;

contract Mapping {

    mapping(address => uint) public balances;

    function setBalanceOf(address _addr, uint _bal) public {
        balances[_addr] = _bal;
    }

    function getBalanceOf(address _addr) public view returns(uint) {
        return balances[_addr];
    }

    function deleteAddress(address _addr) public {
        delete balances[_addr];
    }

}
```

### Nested Mapping
```
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;

contract Mapping {

    struct Movie {
        string title;
        string director;
    }

    mapping(uint => Movie) public movies;
    mapping(string => mapping(uint => Movie)) public collections;

    function addMovie(uint _movieId, string memory _title, string memory _director) public {
        movies[_movieId] = Movie(_title,_director);
    }

    function addCollection(string memory personName, uint id, string memory _title, string memory _director ) public {
        collections[personName][id] = Movie(_title,_director);
    }
}
```




