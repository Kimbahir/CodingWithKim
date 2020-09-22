# Java

Java is just another high leve language. Fear not, the methods for programming
is *almost* the same in all languages :)

## Table of Contents

- [Datatypes and variables](#datatypes-and-variables)
  - [Calculations](#calculations)
  - [Boolean calculations](#boolean-calculations)
  - [Arrays](#arrays)
- [Control structures](#control-structures)
  - [if-else](#if-else)
  - [for](#for)
  - [while](#while)
- [User interactions](#user-interactions)
  - [Taking arguments](#taking-arguments)
  - [Printing to screen](#printing-to-screen)

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
|Add 1       |++          |int a = 1; a++; a is now 2                        |
|Subtract 1  |--          |int a = 2; a--; a is now 1                        |

Note here that in the division example, if you divide with an integer it does
not return the remainder of the division, but only the whole number. If you
divide by a decimal number (e.g. float or double), you get the remainder as
well.

*[table of contents](#table-of-contents)*

### Boolean calculations

We often need to consider boolean expressions, where we are calculating with
the values "true" and "false". Here it is often in the form of requiring some
state or comparing values. It is worth noting that where we are used to
thinking of the following as a comparison:

```java
int a;
a = 2;
```

Well, this is not a comparison in java, but instead an assignment. We calculate
the result on the right-hand side and assign it to the variable on the left. If
we were to compare the two, we would use == instead:

```java
int a = 2; // assigning the value 2
a == 2;    // this would be true - a has the value 2
```

We can chain multiple arguments together. The rules are simple as with
ordinary math, where parentheses calculate expressions internally. The most
common operators for boolean expressions is as follows:

|Name        |Symbol      |Description and example                           |
|---------   |---------   |---------                                         |
|not         |!           |!true is false                                    |
|and         |&&          |true && true is true. true && false is false      |
|or          |\|\|        |true || false is true.                            |
|not equal   |!=          |true != false is true. true != true is false      |

Often we are also using it to compare values, so a very common example is to
check if a value is larger than another:

```java
int counter = 0;
if (counter <= 10) {
    do_something();
}
```

*[table of contents](#table-of-contents)*

### Arrays

Arrays are a construction where you basically get a long list of variables
instead of the classical one value only. All have the same datatype, and you
can have arrays of any datatype you like - but again, you cannot mix!

You write the initialization in the same way as you would with a normal
variable, with the exception that you have to use brackets ([]).

*Remember that arrays always have the first position as 0!* Therefore you
always have the last position as "length - 1"

```java
// Initialize with values
int[] my_test = {1, 4, 7};
String[] names = {"Kim", "Feriba", "Mila", "Jonas"};

// Initialize with a given size and default empty values
int[] my_test = int[3];
String[] names = String[4];
```

When you have initialized an array, you can modify the individual elements,
but you have to do it via an index. Think of the index as the help to Java
to figure out which drawer it should find the shoe.

```java
// Initialize with values
int[] my_test = {1, 4, 7};
my_test[0] = 2; // was 1 before, but now it is 2
my_test[0]++; // was 2 and now is 3

String[] names = {"Kim", "Feriba", "Mila", "Jonas"};
names[4] = "test"; // will fail, because the index of the fourth position is 3!
```

Just remember, think of it as a set of drawers, where you can take things
out and put them back, but you have to tell Java which drawer to work with.

*[table of contents](#table-of-contents)*

## Control structures

We have a set of control structures to help us make the programs more
adaptable to our needs, instead of doing the same thing again and again
and again - just very fast. These are in two forms - if/else and loops (for
and while loops).

### if-else

One of the most classical things we do is to test for a certain condition,
and based on the outcome, either do one thing or another. The most used
control structure for this is the if-else statement. It works by you supplying
a boolean expression. The expression is calculated, and if the result is true,
you execute the true code block, and if the expression is false, you execute
the other. Remember, you can only have the code doing one of them, as code can
never result in *both* a **true** and a **false** being the case ;)

```java
if (<expression>) {
    // There can be many lines in the "true" part of the block
    code_if_true();
} else {
    // There doesn't *need* to be a false block, but there often are
    code_if_false();
}
```

A set of simple examples:

```java
// Example #1
String name = "kim";
if (name == "kim") {
    System.out.println("Welcome kim");
} else {
    System.out.println("Welcome student");
}

// Example #2
String login = "kim";
String password = "password1234"; // wow, the security!

// Here both the login and the password needs to be correct to get a "true"
if ((login == "kim") && (password == "password1234")) {
    System.out.println("You logged in successfully");
} else {
    System.out.println("Get lost, hacker scum!");
}
```

*[table of contents](#table-of-contents)*

### for

The for loop is probably the most used loop, because it helps us ensure that
we (almost) always end the loop, instead of running into eternity. And it provides
a handy counter when/if we need to traverse an array. Inside the for loop we have
three important sections.

- **Initialization**, executed *once* and _only_ once before the loop starts
- **Evaluation**, the test executed *before* every loop to check if it should run
- **Incrementation**, the increment (or decrement) of the counter *after* a loop

and of course the codeblock that is to be executed itself. Conceptually it looks
like this:

```java
for (initialization, evaluation, incrementation) {
    code_block();
}
```

And a very common example is:

```java
int sum = 0;
int[] student_grades = {-2, 0, 2, 10, 7, 10, 12}

for (int i = 0; i < student_grades.length; i++) {
    // The codeblock to be done if the evaluation is true
    sum += student_grades[i]; // notice, we get position i of the array
}

System.out.println("Average grade is " + (sum/student_grades.length))
```

In the example above, the initialization is:
>int i = 0

The evaluation test before each run is:
>i < student_grades.length

And the incrementation is:
>i++

This means we get the counter/index i, starting at 0, and we are constantly
comparing it with the length of the array student_grades before we test if we
should go through with another iteration of the loop. Finally we increase with
1 via the ++ construct, to ensure that we continue through the loop and doesn't
spend eternity with the first student :)

*[table of contents](#table-of-contents)*

## User interactions

We have many ways of interacting 


  - [Taking arguments](#taking-arguments)
  - [Printing to screen](#printing-to-screen)


