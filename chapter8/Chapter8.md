#  Increment and Decrement operators +  Introduction to Iteration


## Objectives
- Recap previous session
- Learn about increment and decrement operators
- Combining assignment and arithmetic
- Introduction to Iteration
- For Loops
- Homework Exercises
- Guidelines

## Recap previous sessions
- How does it look the syntax of a simple `if` statement?
- How does it look the syntax of an `if-else` statement?
- Can we have an `if-else` statement inside another conditional statement? If yes, how it is named? If no, why?
- What is a variable?
- Should we always initialize a variable when we declare it?
- What is the difference between a `method call` and a `method declaration`? Give an example
- How can we obtain the remainder of a division operation?


## Learn about increment and decrement operators
- By `increment`, we usually mean adding `1` to another variable/value. For example, in the snippet below, incrementing the age variable simply means adding `1` to it:
    ```JAVA
        int age = 31;
        age = age + 1
    ```
    - What is happening here is that we want to set the new value for the age variable to be the previous value + 1. That's why we are reusing it in the expression on the left handside.
    - There are 2 syntactic sugar expression to the previous increment operations. The first one allows us to skip the usage of the variable name in the left side expression and it looks like:
        ```JAVA
            int age = 31;
            age += 1;
        ```
        - This expression and the previous one are generating the same results.
        - Note: There should be no space between the `+` symbol and the `=` symbol
    - The second syntactic sugar is the most important one and also the most popular in various programming language (and JAVA of course :) ), this is the `++` operator. See the snippet below:
        ```JAVA
            int age = 11;
            age++;
            System.out.println(age); // It will display 12
        ```
    - There is also another usage  of this operator, namely when you place it in front of the variable:
        ```JAVA
            int age = 11;
            ++age;
            System.out.println(age); // It will display 12;
        ```
    - As you can see, in our example they behave the same but there is a very big difference between them which in theory sounds like this:
        - If the `++` symbol is in front of the variable name (`prefix -> ++age`), first the variable is incremented and if on the same line, the variable is used in other expression, it will contain the updated value.
        - If the `++` symbol is after the variable name (`postfix -> age++`), first the variable is used ( if there is an expression containing it) with the old value, and after that, the value is updated.
        - For a better understanding, run the snippet below:
            ```JAVA
                public class Application {
                public static void main(String[] args) {
                    System.out.println("Postfix Operator:");
                    int age = 11;
                    System.out.println(age++);
                    System.out.println(age);
                    
                    System.out.println("Prefix Operator: ");
                    int grade = 12;
                    System.out.println(++grade);
                    System.out.println(grade);
                }
            }
            ```
- By `decrement` we mean subtracting 1 from a certain variable/value. All the same rules as above applies for this decrement operator only that it is a subtraction and not addition.
    - You can also use the `-=` shortcut
    - You can use the postfix decrement operator: `e.g age--`
    - You can use the prefix decrement operator: `e.g --age`
    - Just to clarify it, run the snippet below:
        ```JAVA
            public class Application {

            public static void main(String[] args) {
                System.out.println("Postfix Decrement Operator:");
                int age = 11;
                System.out.println(age--);
                System.out.println(age);
                
                System.out.println("Prefix Decrement Operator: ");
                int grade = 11;
                System.out.println(--grade);
                System.out.println(grade);
            }
        }
        ```

## Combining assignment and arithmetic
- In Java you can combine arithmetic operation and assignment. For example the instruction:
    ```JAVA
        age += 3;
    ```
    is the shortcut for
    ```JAVA
        age = age + 3;
    ```
- Similarly: `items *=2` is a shortcut for  `items = items * 2`;
- This applies to all math operators like: `+`, `-`, `*`, `/`

## Introduction to iteration
- By iteration we mean the way of running the same task for multiple times, until a specific goal is reached.
- There are multiple iteration constructs in the JAVA language, for this session, we will start with the `while` instruction.
- Before making a deep dive into the syntax of the `while` instruction, let's see a simple example.

1. Create a JAVA program which displays in descending order, first `n` numbers read from the keyboard
- Solution:
    ```JAVA
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner keyboard = new Scanner(System.in);
                System.out.print("Enter n: ");
                int n = keyboard.nextInt();
                while (n >= 0) {
                    System.out.println(n + " ");
                    n--;
                }
            }
        }
    ```
    - Now, the explanation for the snippet above is the following:
        - First we read the number from the standard input (or keyboard)
        - Then we use the `while` instruction which executes a block of code repeatedly
            - In our case, the block contains a printing statement and a decrement operations
        - A condition controls how many times the iteration is performed. You can almost read it as plain english: `while n is greater than 0`
        - You can see some similarities between a `while` and an `if` statement as both check for some condition

## Homework exercises
1. Try to imagine what is the result of the following snippets, without using the Eclipse IDE. Afterwards, check it againd the IDE and see if you were right or you need to read the first part again:
    - ```JAVA
        int score = 12;
        System.out.println( score++ * 12 )
        System.out.println(++score);
        ```
    - ```JAVA
        ```