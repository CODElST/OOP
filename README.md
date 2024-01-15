# Lab1

OOP Labsheet 1\



## Write your first JAVA program.

```java
class Hello {
  public static void main(String args[]) {
    // Program execution begins here
    System.out.println("Hello world. I can write Java!");
  }
}
```

**Compilation:**

Compile your code through terminal by writing

```
javac <YOUR_PROGRAM_NAME>.java
```

In this case:

```
javac Hello.java
```

**Execution:**

Execute your code through terminal by writing

```
java <YOUR_PROGRAM_NAME>
```

In this case:

```
java Hello
```

**Output:**

```
Hello world. I can write Java!
```

\


After your code is compiled you will find a file with the same named as the program file but with the extension **.class**.\
A Java class file is a file containing Java bytecode and having .class extension that can be executed by JVM (Java Virtual Machine). A Java class file is created by a Java compiler from .java files as a result of successful compilation.

#### Java Class and Structure

**Class:**

The Class is the basic unit of Object Oriented Programming.\
The Class forms the basis for object oriented programming in Java.

**General Syntax of Class:**

```java
class classname
{
  type instance-variable1;
  type instance-variable2;
  ...
  type instance-variableN;

  type methodname1(parameter-list)
  { body }
  ...
  type methodnameN(parameter-list)
  { body }
}
```

Two components of Java Class:

1. Atrributes - Variables
2. Methods - Functions

**Example:**

```java
class Square {
  int value;
  public static void printSquare(int x){
    System.out.println(x*x);
  }
  public static void main(String args[]){
    int local_value = 2;
    printSquare(local_value);
    printSquare(3);
    printSquare(local_value*2);
  }
}
```

To instantiate an object of Square:

```java
Square mySquare = new Square();
```

To access variables of an object

```java
mySquare.value = 12;
```

To access methods of an object

```java
mySquare.printSquare(10);
```

**Syntax Guidelines**

1. Every line of code that runs in Java must be inside a `class`
2. A class should always start with an uppercase first letter.
3. The name of the java file must match the class name.
4. The `main()` method is required and you will see it in every Java program. Any code inside the `main()` method will be executed.

#### Java Identifiers

All Java variables must be identified with unique names called identifiers.

**Declaring (Creating) Variables:**

```java
type variableName = value;
```

**Types of Java Literals:**

1. `String` - Stores text
2. `int` - Stores integers (whole numbers)
3. `float` - Stores floating point numbers
4. `char` - Stores single characters
5. `boolean` - Stores true or false

**Variable Name Guidelines**

* Names can contain letters, digits, underscores, and dollar signs
* Names must begin with a letter
* Names should start with a lowercase letter and it cannot contain whitespace
* Names can also begin with $ and \_
* Names are case sensitive
* Reserved words (keywords) cannot be used as names

#### Java Conditional Statements

* `if`

```java
if (condition) {
  // block of code to be executed if the condition is true
}
```

* `else`

```java
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```

* `else if`

```java
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

* `switch`

```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

**Shortcut for if-else**

```java
variable = (condition) ? expressionTrue :  expressionFalse;
```

#### Java Loops

**while loop**

```java
while (condition) {
  // code block to be executed
}
```

**do-while loop**

```java
do {
  // code block to be executed
}
while (condition);
```

**for loop**

```java
for (initialization; condition; iteration) {
  // code block to be executed
}
```

**for-each loop (can be used for iterating)**

```java
for (type variableName : arrayName) {
  // code block to be executed
}
```

#### Java Data Types

| Data Type | Size/Format   | Description                          |
| --------- | ------------- | ------------------------------------ |
| byte      | 8-bit         | Byte-length integer                  |
| short     | 16-bit        | Short integer                        |
| int       | 32-bit        | Integer                              |
| long      | 64-bit        | Long integer                         |
| float     | 32-bit        | Single-precision floating point      |
| double    | 64-bit        | Double-precision floating point      |
| char      | 16-bit        | Unicode character A single character |
| boolean   | true or false | A boolean value (true or false)      |

#### Array

**Declaring an array**

```java
elementDataType[] arrayName = new elementDataType[arraySize];
```

```java
elementDataType[] arrayName = {element_1, element_2, element_3, ..., element_N};
```

Example

```java
int[] firstArray = new int[10];
int[] firstArray = {0,1,2,3,4,5,6,7,8,9};
```

**Declaring a 2D array**

```java
elementDataType[][] arrayName = new elementDataType[rowSize][colSize];
```

```java
elementDataType[][] arrayName = {{element_1_1, ..., element_1_M}, ..., {element_N_1, ..., element_N_M}};
```

Example

```java
int[][] firstTwoDArray = new int[10][20];
int[][] firstTwoDArray = {{0,1,2},{3,4,5},{6,7,8}};
```

#### Taking input from user

The Scanner class is used to get user input, and it is found in the java.util package.

| Method        | Description                         |
| ------------- | ----------------------------------- |
| nextBoolean() | Reads a boolean value from the user |
| nextByte()    | Reads a byte value from the user    |
| nextDouble()  | Reads a double value from the user  |
| nextFloat()   | Reads a float value from the user   |
| nextInt()     | Reads a int value from the user     |
| nextLine()    | Reads a String value from the user  |
| nextLong()    | Reads a long value from the user    |
| nextShort()   | Reads a short value from the user   |

```java
import java.util.Scanner;

class UserInput {
  public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
      String str = sc.nextLine();
      System.out.println("String is: " + str);
      int first = sc.nextInt();
      int second = sc.nextInt();
      int sum = first + second;
      System.out.println("Sum is: " + sum);
    }
}
```

### Exercise Problems:

#### Exercise 1

What happens when we declare multiple classes in the same file and then use javac to compile the file and the file name is any one of the declared classes?

#### Exercise 2

Write a Java program to compute the final amount a person has to repay for a loan of 10 years with interest rate of 5% per annum. The principal amount is to be taken as input from user and display the final amount.\
Use `double` datatype for principal and final amount.

**Formula:**

`FinalAmount = PrincipalAmount(1 + (TimePeriodInYears * InterestRate / 100))`

**Input**

A double representing the principal amount

**Output**

A double representing the final amount

**Sample Test Input**

```
1000.0
```

**Sample Test Output**

```
1500.0
```

#### Exercise 3

Write a Java program to print a menu to the user asking to choose between by entering the corresponding option number:

```
1. Circle
2. Rectangle
```

If `1` (circle) is chosen, take the input of radius (int) and print the area of the circle (take pi = 3.14), otherwise take the input of length (int) and breadth (int) of rectangle and print the area.\
Do this exercise with both if-else and switch statements.

**Sample Test Input 1**

```
1
10
```

**Sample Test Output 1**

```
314.0
```

**Sample Test Input 2**

```
2
60
20
```

**Sample Test Output 2**

```
1200
```

#### Exercise 4

Write a Java program to declare a 2D array of size 4 X 3, then take the input from user such that the array contains following elements:

```
12   3    4 
4    34   2
65   1   56
76   24   7
```

After that, using for-each loop find the sum of the whole array and print it.

\*\*\*

## OOP Labsheet 1 Solutions

\


### Exercise Problems:

#### Exercise 1

What happens when we declare multiple classes in the same file and then use javac to compile the file and the file name is any one of the declared classes?

**Solution**

We get .class file corresponding to all the declared classes in the file. To execute any of the class we can just write java with the corresponding class name.

Example: We declare two classes names `Hello` & `World` and the file is named `Hello.java`, once we compile `javac Hello.java` we get `Hello.class` and `World.class`. After that to execute the classes we can call `java Hello` or `java World`.

#### Exercise 2

Write a Java program to compute the final amount a person has to repay for a loan of 10 years with interest rate of 5% per annum. The principal amount is to be taken as input from user and display the final amount.\
Use `double` datatype for principal and final amount.

**Solution**

```java
import java.util.Scanner;

class Loan {
  public static void main(String args[]){
    Scanner prin = new Scanner(System.in);
    double principal = prin.nextDouble();
    double finalAmount = principal * (1 + 0.05 * 10);
    System.out.println(finalAmount);
  }
}
```

#### Exercise 3

Write a Java program to print a menu to the user asking to choose between by entering the corresponding option number:

```
1. Circle
2. Rectangle
```

If `1` (circle) is chosen, take the input of radius (int) and print the area of the circle (take pi = 3.14), otherwise take the input of length (int) and breadth (int) of rectangle and print the area.\
Do this exercise with both if-else and switch statements.

**Solution**

```java
import java.util.Scanner;

class Area {
  public static void circle(){
    Scanner cir = new Scanner(System.in);
    int radius = cir.nextInt();
    System.out.println("Area of circle is: " + (3.14 * radius * radius));
  }

  public static void rectangle(){
    Scanner rec = new Scanner(System.in);
    int len = rec.nextInt();
    int bre = rec.nextInt();
    System.out.println("Area of Rec is: " + (len * bre));
  }

  public static void main(String args[]){
    System.out.println("Choose one of the options:");
    System.out.println("1. Circle");
    System.out.println("2. Rectangle");

    Scanner menu = new Scanner(System.in);
    int option = menu.nextInt();

    // with If-else
    if(option == 1){
      circle();
    }
    else if(option == 2){
      rectangle();
    }
    else{
      System.out.println("Invalid option");
    }

    //OR with Switch Statement:
    switch(option){
      case 1:
        circle();
        break;
      case 2:
        rectangle();
        break;
      default:
        System.out.println("Invalid option");
    }
}}
```

#### Exercise 4

Write a Java program to declare a 2D array of size 4 X 3, then take the input from user such that the array contains following elements:

```
12   3    4 
4    34   2
65   1   56
76   24   7
```

After that, using for-each loop find the sum of the whole array and print it.

**Solution**

```java
class Array {
  public static void main(String args[]){
    int[][] arr = new int[4][3];
    Scanner ele = new Scanner(System.in);
    for(int i=0; i<4; i++){
      for(int j=0; j<3; j++){
        arr[i][j] = ele.nextInt();
      }
    }

    int sum = 0;
    for(int[] i: arr){
      for(int j: i){
        sum += j;
      }
    }
    System.out.println(sum);
  }

}
```
