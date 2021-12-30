# Learning-Solidity
Setting this repo to learn solidity by developing Smart Contracts

### Softwares/Websites Required
IDE - Remix - [remix.ethereum.org](remix.ethereum.org)

Notes/Queries:
1. When range for compiler version is defined in pragma then which compiler version is selected?
2. External not applicable for variables (state variables) - string external name = "Test"; -- Error
3. Applicable modifiers/visiblity applicable for variables:
    - public, private, internal
    - storage, memory
4. Default visiblity for variables is internal.
5. Cannot write if-else, loop code directly inside a contract just like in classes, but inside functions or modifies.
6. Data Types: uint, int, string, bool, uint8, uint16, .., uint256, int8, int16,...,int256
7. If inside function, variable with same name as state variable is declared then local variable will be visible in that function.
8. EVM - Ethereum Virtual Machine - has no access to internet file system any other resources
9. Wei - Smallest unit of ether - 18 decimals is. 1 ETH = 10**18 Wei

