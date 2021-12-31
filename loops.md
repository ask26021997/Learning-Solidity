
# Loops
**If Loops got inifinte iterations where data gets changed the GAS will be consumed completely** -- *validate once*

## for loop
initialise - Optional
initialise - optional
incrementor/decrementor - optional

for( initialise; condition; incrementor/decrementor ) {

}

```
contract ForLoop {
    
    uint[] arr = [1,2,3,4,5,6,7,8,9,10];

    function checkMultiples(uint _a, uint _b) public pure returns(bool) {
        return _a%_b == 0 || _b%_a == 0;
    }

    function countMultiplesOf(uint _num) public view returns(uint) {
        uint count = 0;
        for(uint i=0;i<arr.length;i++) {
            if ( checkMultiples(arr[i],_num) ) {
                count++;
            }
        }
        return count;
    }

    function countMultiplesOf(uint _num) public view returns(uint) {
        uint count = 0;
        uint i=0;
        for(;;) { // all are optionals
            if ( checkMultiples(arr[i],_num) ) {
                count++;
            }
            i++;
            if ( i >= arr.length ) {
                break; // break the current loop but only one loop if nested loops then it won't stop all loops
            }
        }
        return count;
    }
}
```

# while loop

condition - mandatory provide true/false if want to skip

while(condition){
    // code
    // incrementor/decrementor
}

```
contract WhileLoop {
    
    uint[] arr = [1,2,3,4,5,6,7,8,9,10];

    function checkMultiples(uint _a, uint _b) public pure returns(bool) {
        return _a%_b == 0 || _b%_a == 0;
    }

    function countMultiplesOf(uint _num) public view returns(uint) {
        uint count = 0;
        uint i=0;
        while(i<arr.length){
            if ( checkMultiples(arr[i],_num) ) {
                count++;
            }
            i++;
        }
        return count;
    }

    function countMultiplesOf(uint _num) public view returns(uint) {
        uint count = 0;
        uint i=0;
        while(true){
            if ( checkMultiples(arr[i],_num) ) {
                count++;
            }
            i++;
            if (i<arr.length){
                continue;
            }
            break;
        }
        return count;
    }
}
```

# break statement

used **inside loops only** to break the loop and control will be given to parent (function/blocl/loop...)

# continue statement

used **inside loops only** to skip the current iteration and move to next iteration, *in case of for loop control will go to the incrementor/decrementor section*.
