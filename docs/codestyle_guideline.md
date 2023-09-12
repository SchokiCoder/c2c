# Indentation

4 spaces are one indentation and actual space characters must be used.  
switch and case are aligned and the content of the case gets one indentation.  
Good example (do this):  
```
switch (letter) {
case 'A':
    handle_a();

case 'B':
    handle_b();
}
```

Multiple statements do not belong on the same line.  
Bad example (**don't** do this):  
```
if (cond) foo();
bar();
```

The line limit is 140 characters long.  
Do not break user visible string so they can be searched for.  

# Braces

Opening braces accompany whatever caused this brace to exist, on the same line.  
The closing brace is put on the next line after the embraced content.  
Putting something that causes braces to exist on the same line of a closing
brace is legal.  
Good example:  
```
if (true) {
    yay();
} else {
    neigh();
}
```

# Spaces

Use a space after all keywords that don't generally look like functions aka.
builtin functions.  
Use spaces after: `if switch case for do while ...`  
but not after `sizeof elemsof offsetof ...`.  

Use space around arithmetic, assignment, comparison, and logical operators.  
Arithmetic: `+ - * /`  
Assignment: `= += -= *= /=`  
Comparison: `== >= <= !=`  
Logical: `&& ||`  

Good example:  
```
a + b;
a = -b;
a *= b;

if ((a == b) && (c.foo != d))
```

# Names

Variable names, function names and module names adhere to the snake_case.  
Struct names should be CamelCase but with a uppercase letter at the
beginning.  
Global constants are all UPPER_CASE.  
Good example:  
```
module example_stuff;

type CompanionCube struct {
    i32  w;
    i32  h;
    bool alive;
}

fn void do_thing(i32 core_sanity) {
    CompanionCube ratmans_cube;
    
    if (core_sanity > EVIL_CORE_SANITY)
        core_transfer();
}
```

# Comments

Preferred style for multiline comments is as follows:  
```
/* This is
 * my
 * long comment
 */
```