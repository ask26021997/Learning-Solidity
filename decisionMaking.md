

# if - else statements

These can be written inside a functions, constructor, modifiers but not directly inside contract.
```
uint a = 10;
if( a == 10 ) {
    a = 20; -- here new variables can also be declared
} else {
    a = 30;
}
```

{ } -- **Required** if multiple lines are required to be executed as part of this condition truth.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**else optional**
```
if(a==10)
    a=20; -- here no new variable can be declared if { } are not used as this won't make any sense.
else
    a=30;

if ( a == 30){
    // do something
} else if (a != 50) { -- if else ladder is is also possible multiple times
    // do something else
} else {

}

if(a==30) { -- if without else is possible
    a=40; 
}

a = 20;
else { -- else without if is **not** possible
    a=40; 
}
```

# Nesting
Nesting of if statements is also possible

```
if ( condition ) {
    if ( condition ) {

    } else if ( condition ) {

    } else {
        if( condition ) {

        }
    }
} else {
    if ( condition ) {
        
    }
}
```

