## Reference sheet about Java ##

This one is a WIP about Java, I'm trying to put informations and links about Java all in the same place. For now it's not visually appealing but it's not the priority.

#### Data Types ####

[DOC ORACLE on DATA TYPES](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)


Two types of data type in Java, that's a reason as why Java is not considered a truly Object language by purist.
There are primitives types

 - `byte` 8-bit signed two's complement integer. [-128;127] . default = 0
 - `short` 16-bit signed two's complement integer. [-32,768;32,767] . default = 0
 - `int` 32-bit signed two's complement integer. [-2^31;2^31-1] . default = 0 . In JavaSE >= 8, possibility to have unsigned int and support of unsigned int with the Integer class
 - `long` 64-bit signed two's complement integer. [-2^63;2^63-1] . default = 0L . In JavaSE >= 8, possibility to have unsigned long and support of unsigned long with the Integer class
 - `float` 32-bit IEEEE 754 floating points. default = 0.0f
 - `double` 64-bit IEEE 754 floating points. default = 0.0d
 - `boolean` true or false. default = false . One bit of information, but real size not precisely defined
 - `char` 16-bit Unicode character. ['\u0000';'\ufff'] . default = '\u0000'
 
String is a class but with special meaning. `String s = 'toto';` will do the same as `String s = new String('toto');`

### Operator listed by precedence ###
Lower precedence means evaluted first. 

#### Precedence 0 ####
- `new`: Not officially an operator, as it is only used in one context, followed just after by  class name.

#### Precedence 1 #### 
- (prefix) `++`: The preincrement operator (add 1)
- (prefix) `--`: The predecrement operator (substract 1)
- (unary) `+`
- (unary) `-`
- (unary) `~`: Bitwise not for `int`
- (unary) `!`: `Boolea`n not
- `(cast)`: Not officially an operator, has multitude of purposes, all united under the term casting
- (postfix) `++`: The postincrement operator (add 1)
- (postfix) `--`: The postdecrement operator (substract 1)

#### Precedence 2 ####
- `*`: Integer multiplication for `int` and floating point multiplication for `double`
- `/`: Integer division for `int` and floating point division for `double`
- `%`: Remainder operator (often miscalled the *modulus*)
#### Precedence 3 ####
- `+`: Integer addition for `int` and floating point addition for `double`. Is also the concatenation operator for `String`
- `-`: Integer substraction for `int` and floating point substraction for `double`
#### Precedence 4 ####
- `<<`: arithmetic left shift (no `<<<` cause it would be identical)
- `>>`: arithmetic shift right (signed shift, will preserve the most significant bit value)
- `>>>`: logical shift right (unsigned shift, always insert 0 to the left to fill the bits)

See [this post](https://stackoverflow.com/a/2811372/3729797) for more detailed explanation on bit shift
#### Precedence 5 ####
- `<`: Less than operator
- `>`: Greater than operator
- `<=`: Less than or equal operator
- `>=`: Greater than or equal operator
- `instanceof`: Oddly enough, `instanceof` is considered an operator even though it cannot operate on expressions.
#### Precedence 6 ####
- `==`: equal operator
- `!=`: not equal operator
#### Precedence 7 ####
- `&`: bitwise AND masking. (Used mostly for `int`)
#### Precedence 8 ####
- `^`: XOR (exclusive OR) for `int`
#### Precedence 9 ####
- `|`: bitwise OR 
#### Precedence 10 ####
- `&&`: Short-circuit logical AND for `Boolean`
#### Precedence 11 ####
- `||`: Short-circuit logical OR for `Boolean`
#### Precedence 12 ####
- `:?`: Ternary operator (`a = (b==c) ? d : e`;)
#### Precedence 13 ####
- `=`
- `*=`
- `/=`
- `+=`
- `-=`
- `<<=`
- `>>=`
- `>>>=`
- `&=`
- `^=`
- `|=`

### Keywords ###

[List of keyword](www.codejava.net/java-core/the-java-language/java-keywords)

- `abstract`
- `assert`: [Oracle doc](https://docs.oracle.com/javase/7/docs/technotes/guides/language/assert.html), [SO](https://stackoverflow.com/q/2758224/3729797)
- `boolean`
- `break`
- `byte`
- `case`
- `catch`
- `char`
- `class`
- `const`
- `continue`
- `default`
- `do`
- `double`
- `else`
- `enum`
- `extends`
- `final`
- `finally`
- `float`
- `for`
- `goto`
- `if`
- `implements`
- `import`
- `instanceof`
- `int`
- `interface`
- `long`
- `native`: [SO](https://stackoverflow.com/questions/6101311/what-is-the-native-keyword-in-java-for) in short to design FFI methods
- `new`
- `package`
- `private`
- `protected`
- `public`
- `return`
- `short`
- `static`
- `strictfp`:class keyword. Compute floats/doubles using a fixed precision, for portability. Usually less precise on newer computer.
- `super`
- `switch`
- `synchronized`: [oracle](https://docs.oracle.com/javase/tutorial/essential/concurrency/syncmeth.html), [link](https://javamex.com/tutorials/synchronization_concurrency_synchronized1.shtml)
- `this`
- `throw`
- `throws`
- `transient`: When serialising an object, all fields marked as `transient` are ignored
- `try`
- `void`
- `volatile`: Updating value when writing on it for other threads. See [this](https://stackoverflow.com/a/106787/3729797) and [this](https://www.ibm.com/developerworks/java/library/j-jtp06197/) and [this](http://tutorials.jenkov.com/java-concurrency/volatile.html) and [this](https://javamex.com/tutorials/synchronization_volatile.shtml)
- `while`

Some noteworthy points regarding Java keywords:

    - `const` and `goto` are resevered words but not used.
    - `true`, `false` and `null` are literals, not keywords.
    - All keywords are in lower-case.

### Ressources ###

[Java Language and Virtual Machine Specification](https://docs.oracle.com/javase/specs/#15.19)
