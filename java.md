# Java

Java is just another high leve language. Fear not, the methods for programming
is *almost* the same in all languages :)

## Table of Contents

- [Datatypes and variables](#datatypes-and-variables)
  - [Calculations](#calculations)
  - [Arrays](#arrays)
- [Control structures](#control-structures)
  - [if-else](#if-else)
  - [for](#for)
  - [while](#while)

## Datatypes and variables

In Java you always need to instantiate a variable with a data type. There are
several datatypes to choose from, and once a datatype has been set for a
variable, you cannot change it afterwards. Java needs this datatype in order to
reserve some memory to match and to ensure what is called *type safety*. This
being that you don't try to multiply a string and so on. You will later learn
how to make your own classes, but here are the types you will usually be using:

|Name        |Short name  |Description and example                           |
|---------   |---------   |---------                                         |
|String      |String      |A text like "feriba" and "this is a test"         |
|Integer     |int         |A whole number (no decimals) like 1 or 17         |
|Float       |float       |A decimal number like 1.17 or 2.99                |
|Double      |double      |A decimal number like 1.17 or 2.99                |
|Boolean     |boolean     |A true/false value                                |

When you create a variable it can either be created with a value or just
reserved and set with a default value. The form for doing this is to write the
type, followed by a space and then the name of the variable. The name must be
in one word, but underscores (_) are allowed and numbers too, as long as the
variable starts with a letter.

```java
int my_number = 23;
int some_other_random_number = 45;

double my_decimal_number = 23.45;
String my_name = "Kim";
boolean finished = false;
```

As you can see, the naming is rather free, and it almost always makes sense to
initiate your variable. At least then you know what it contains :)

*[table of contents](#table-of-contents)*

### Calculations

When calculating you need to be aware of different ways of doing things. Java
has a very advanced toolkit that programmers often use to find a smart way of
solving things. Things like dividing, but only receiving the remainder of the
division (modulus) or only the integer parts (integer division). Furtunately,
the main rules are the same. Multiplication and division comes before adding
and substracting and so forth. Also you can use parantheses to make calculations
in the right order.

|Name        |Symbol      |Description and example                           |
|---------   |---------   |---------                                         |
|Addition    |+           |2 + 3 = 5                                         |
|Subtraction | -          |2 - 3 = -1                                        |
|Multiply    |\*          |2 \* 3 = 6                                        |
|Division    |/           |6 / 2 = 3 and 6 / 4 = 1 (!) but 6 / 4.0 = 1.5     |
|Modulus     |%           |6 % 2 = 0 and 6 % 4 = 2                           |

Note here that in the division example, if you divide with an integer it does
not return the remainder of the division, but only the whole number. If you
divide by a decimal number (e.g. float or double), you get the remainder as
well.

*[table of contents](#table-of-contents)*

### Arrays

Arrays are a construction where you basically get a long list of variables
instead of the classical one value only. All have the same datatype, and you
can have arrays of any datatype you like - but again, you cannot mix!

You write the initialization in the same way as you would with a normal
variable, with the exception that you have to use brackets ([])

*[table of contents](#table-of-contents)*
