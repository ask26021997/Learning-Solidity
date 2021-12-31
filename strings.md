
# strings in solidity

- sequence of characters in quotes(double/single).
- utf8

- specify explicitly where to store strings while using in functions
    - storage/memory

### to get length of string

In solidity string computation is very costly so we have to convert strings into ***bytes*** first

```
contract SolidityLoops {
    string public message = "Hello!"; // 6 characters //"Hello!\'" // 7 chars
    function greet(string memory _newMessage) public {
        message = _newMessage;
    }
    function messageLength() public view returns(uint) {
        // return message.length // not possible
        bytes memory messageBytes = bytes(message);
        return messageBytes.length;
        // return bytes(message).length; // this will also work
    }
}
```

\n : new line
\\ use backspace to escape
