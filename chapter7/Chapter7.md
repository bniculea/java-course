# Recap Variables, Methods, Conditional statements

## Objectives
- Recap previous session
- Recap variables + exercises
- Recap methods + exercises
- More conditional statements exercises
- Homework exercises


## Recap previous session
- What is the type of data that we can use to store `true` or `false` values?
- Can you give an example where this type really helps?
- What do we need in order to read from the Standard Input?
- How can we read `int`, `double` or `String` values?
- Enumerate the boolean operators that comes into your mind.
- What are the logical operators that we learned about?
- How do we make a check in JAVA? For example, if I want to execute a certain statement only if a condition is met, what should I use?
- How many conditional statements can I chain?
- What operator should I use if I want to subtract the remainder of a division?
- Can I  have an If statement inside another If statement? What is this called?


## Recap variables + exercises
- What is a variable?
- Why do we use variables?
- Can you tell the parts of a variable?
- Can you declare a variable without asigning it a value?
- What should you do before using a variable?

### Exercises
1. Create A String variable and do not set a value to it. Now, print this variable. After you fix the issues, call the length method.
    - Solution:
        ```JAVA
            public class Application {

                public static void main(String[] args) {
                    String name = null;
                    System.out.println(name);
                    name.length();
                }
            }
        ```
2. Declare a boolean variable which will hold the result between the comparison of `5` and `4` using the `smaller than` operator. Display the value of the variable using the `println` method.
    - Solution:
        ```JAVA
             public class Application {

                public static void main(String[] args) {
                    boolean comparison = 5 < 4;
                    System.out.println(comparison);
                }
            }
        ```
3. Declare a `double` variable and initialize it with a value of your choice (make sure it is a floating point variable.) Next declare a variable of type `int` and store the value of the `double` variable inside it. Next, print the value of the `int` variable.
    - Solution:
        ```JAVA
            public class Application {

                public static void main(String[] args) {
                    double grade = 55.9;
                    int truncatedGrade = (int) grade;
                    System.out.println(truncatedGrade);
                }
            }
        ```
## - Recap methods + exercises
- What is a method?
- What is the most important method that any JAVA application has it?
- What is the structure of a JAVA method? Give some examples, define random methods.
- Can you have methods that have the same name but different number of arguments?
- Can you have method that have the same name, same number of arguments but different return type?


### Exercises
1. Create a JAVA method which displays a message of your choice.
    - Solution:
        ```JAVA
            public class Application {

                    public static void display() {
                       System.out.println("Simple message");
                    }
                }
        ```
2. Create a JAVA method which displays a message which is received as a parameter of type `String`
    - Solution
        ```JAVA
            public class Application {

                public static void display(String message) {
                    System.out.println(message);
                }
            }
        ```
3. Create a JAVA method, which receives 3 double parameters and returns the smallest one. Do not use `if` statements (Hint: Use `Math.min` method)
    - Solution
        ```JAVA
        public class Application {

                public static double min(double x, double y, double z) {
                    return Math.min(Math.min(x, y), z);
                }
            }
        ```
## More conditional statements exercises

1. Write a JAVA program which reads a letter from the Standard Input. The program should print Vowel or Consonant, depending on the user input. If the user input is not a letter (between a and z or A and Z), or is a string of length > 1, print an error message.
    - Solution:
        ```JAVA
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner in = new Scanner(System.in);
                System.out.println("Enter a letter");
                String letter = in.next();
                if(letter.length() > 1 || Character.isDigit(letter.charAt(0))) {
                    System.out.println("You should enter a letter!!");
                } else if(letter.equalsIgnoreCase("a") || letter.equalsIgnoreCase("e") || letter.equalsIgnoreCase("i") || letter.equalsIgnoreCase("o") || letter.equalsIgnoreCase("u")) {
                    System.out.println("Vowel!");
                } else {
                    System.out.println("Consonant");
                }
            }

        }
        ```
2. Write a JAVA program which allows the user to enter a number between 1 and 10. Next, generate a random number between 0 and 10 and compare it against the number introduced by the user. If the number entered by user is greater, print "Too high", else if the number is smaller, print "Too small" and if the numbers are equal, press "You hit the JackPot". Note, in order to generate a random number between 1 and 10 use the following JAVA snippet: 
    ```JAVA
        Random random = new Random();
        int randomNumber = random.nextInt(11);
    ```
    Bonus: Extra POINTS if you create a method that validates the input entered by the user, meaning that the user is only allowed to enter a number between 0 and 10 inclusive
    - Solution:
        ```JAVA
            import java.util.Random;
            import java.util.Scanner;

            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("Enter a number between 0 and 10: ");
                    int number = in.nextInt();
                    
                    if(isInputValid(number)) {
                        Random random = new Random();
                        int randomNumber = random.nextInt(11);
                        
                        if(number > randomNumber) {
                            System.out.println("Too High!");
                        } else if (number < randomNumber) {
                            System.out.println("Too Low!");
                        } else {
                            System.out.println("You hit the jackpot!!");
                        }
                        
                    } else {
                        System.out.println("Bad Input! Only allowed to enter numbers between 0 and 10");
                    }
                }
                
                public static boolean isInputValid(int number) {
                    return number >=0 && number <=10;
                }
            }
        ```
3. Write a JAVA application which receives two `int` values from the user and asserts whether the first number is a multiple of the second one in the following format:
    - `First number is a multiple of the second number` (if the first number is a multiple of the second one) 
    - `First number is not a multiple of the second number` (if the first number is not a multiple of the second one).
    
    Also, the program should display `false` from the beginning if the second number happens to be 0.
    - Solution:
        ```JAVA
            import java.util.Scanner;

            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("Enter the first number: ");
                    int firstNumber = in.nextInt();
                    System.out.print("Enter the second number: ");
                    int secondNumber = in.nextInt();
                    
                    if(secondNumber == 0) {
                        System.out.println("False!");
                    } else {
                        if(firstNumber % secondNumber == 0) {
                            System.out.println("First Number is a multiple of the second number!");
                        } else {
                            System.out.println("First Number is not a multiple of the second number!");
                        }
                    }
                    
                }
                
                public static boolean isInputValid(int number) {
                    return number >=0 && number <=10;
                }
            }
        ```
4. Create a JAVA program which receives three double values, meaning the possible sides of a right triangle, and return wheter or not the three values can form a right-angled triangle. 
    - Solution:
        ```JAVA
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner in = new Scanner(System.in);
                System.out.print("Enter side a length: ");
                double sideA = in.nextDouble();
                System.out.print("Enter side b length: ");
                double sideB = in.nextDouble();
                System.out.print("Enter side c length: ");
                double sideC = in.nextDouble();
                
                //a b and c should be greater than 0
                
                boolean validRightTriangle = canFormRightTriangle(sideA, sideB, sideC);
                System.out.println(validRightTriangle);
            }
            
            private static boolean canFormRightTriangle(double sideA, double sideB, double sideC) {
                if(sideA <= 0 || sideB <= 0 || sideC <= 0) {
                    return false;
                }
                
                if( (sideA + sideB) <= sideC || (sideA + sideC) <= sideB || (sideB + sideC) <= sideA) {
                    return false;
                }
                
                boolean result = (sideA * sideA + sideB * sideB) == sideC * sideC;
                
                return result;
            }
        }
        ```