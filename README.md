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

10. if condition with single line code without { } is possible.
11. If returns not included in function declaration then we cannot use return statement.
12. If a function returns some value then return statement is still optional and be default function will return false values i.e for uint 0, for bool false, and for string "".
13. Functions visibility:
    - public : Accessible from both internally and externally from contract and within inherited contracts as well.
    - private : Accessible only inside the contract not even inherited contracts.
    - internal : Accessible only inside the contract and also inside the inherited contracts.
    - external : Accessible only outside the contract not even within the contract. e.g. when setting from external world like using other contracts in your functionality.
14. pure and view and payable (state mutability):
    - pure : When no data has been accessed from blockchain (state variables).
    - view : When we read data from blockchain but donot modifies that data.
    - payable : When we want to modify data on blockchain and since this data has to be changed on multiple nodes then we need GAS which is real money of the users so in solidity we can pay GAS when calling function if function is marked as payable.
    - non-payable: but default this is the state mutability of function (maybe in test envronment only).
15. If function modifies data(state variable/updates data on blockchain) then it won't return any value even compiler compiles successfully as we have to remove view from function declaration so we cannot view data returned by the function (but in the transaction its mentioned as output).
16. view and payable: we can't call payable functions inside viewable functions but opposite is true.
17. view and pure: we can call pure functions inside view function but opposite is not true.
18. Operators:
    - +, -, *, %
    - ++, -- post and pre inc/dec - How do they perform in arithmetic operations -> a =2, b=12 ==> b + b++ + a++;


