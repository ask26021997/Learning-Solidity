
# modifier

1. Similar to functions
2. keyword use: **modifier**
3. Can take arguments
4. Cannot return values
5. visibility concept doesn't apply
6. to continue functions at the end use _;

### Creating modifier no arguments
```
    modifier onlyOwner {
        require(_owner == msg.sender);
        _;
    }

    // using the modifier
    function changePrice(uint _price) public payable onlyOwner {
        price = _price;
    }

```

### Creating modifier with arguments
```
    modifier costs(uint price) {
        require(msg.value >= price);
        _;
    }

    // using the modifier
    function register() public payable costs(price) {
        registeredAddress[msg.sender] = true;
    }

```

# view and pure functions

### view
if function is not changing the data on blockchain and **only reads data from blockchain** then view should be used

### pure
if function **doesnot read or write** data on/from bloackchain then pure should be used


