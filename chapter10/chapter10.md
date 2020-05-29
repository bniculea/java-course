# Exercises with `for` and `while` instructions

## Objectives

- Recap previous session
- Exercises
- Homework exercises
- Guidelines

## Recap previous session

- What is a `for` instruction? How does it help?
- What is the difference between a `for` and a `while`?
- Can you substitute a `for` loop with a `while` loop?

## Exercises

- Note: each exercises will be first solved using the `for` instruction and then using the `while` instruction such that you will get familiar with both of them

TBD: remove this reference: => PBINFO => Iteration: Page 2

1. Given `n` natural numbers, create a JAVA program which will compute the root mean square ( media patratica) of them.

   - Note: the formula for this is described in the image below:

![Quadratic Mean:](./images/quadraticMean.svg)

- Sample Input:
  - n = 5
  - 1 2 3 4 5
- Sample Output: `The quadratic mean of the entered numbers is 3.3166247903554`
- Solution:

  a. `while`:

  ```JAVA
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner in = new Scanner(System.in);
                System.out.println("How many numbers do you want to read? ");
                int n = in.nextInt();
                int i = 0;
                double sumOfSquares = 0.0;
                while (i < n) {
                    System.out.println("Enter number #" + (i+1));
                    sumOfSquares += Math.pow(in.nextDouble(), 2);
                    i++;
                }

                double quadraticMean =  Math.sqrt(sumOfSquares / n);
                System.out.println("The quadratic mean of the entered numbers is: " + quadraticMean);
            }
        }
  ```

  b. `for`:

  ```JAVA
      import java.util.Scanner;

      public class Application {

          public static void main(String[] args) {
              Scanner in = new Scanner(System.in);
              System.out.println("How many numbers do you want to read? ");
              int n = in.nextInt();
              double sumOfSquares = 0.0;
              for(int i =0; i < n; i++) {
                  System.out.println("Enter number #" + (i+1));
                  sumOfSquares += Math.pow(in.nextDouble(), 2);
              }

              double quadraticMean =  Math.sqrt(sumOfSquares / n);
              System.out.println("The quadratic mean of the entered numbers is: " + quadraticMean);

          }

      }

  ```

  ```

  ```

2.  Given `n`, create a JAVA program wich will compute `10 to the power n`.

    - Sample Input: n = 3
    - Sample Output: 1000
    - Solution:
      a. `while`

      ```JAVA
      import java.util.Scanner;

                public class Application {

                    public static void main(String[] args) {
                        Scanner in = new Scanner(System.in);
                        System.out.print("N = ");
                        int n = in.nextInt();
                        int i = 0;
                        double result = 1;
                        while (i < n) {
                            result = result * 10;
                            i++;
                        }

                        System.out.println("10 to the power " + n + " is: " + result );

                    }

                }
      ```

      b. `for`:

      ```JAVA
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner in = new Scanner(System.in);
                System.out.print("N = ");
                int n = in.nextInt();
                double result = 1;

                for(int i = 0; i < n; i++) {
                    result = result * 10;
                }
      ```


                System.out.println("10 to the power " + n + " is: " + result );

            }

        }

      ```

3.  Given two numbers `a` and `b` read from the keyboard, create a JAVA program which will compute `a` to the power `b`

    - Sample Input:
      - a = 4
      - b = 5
    - Sample Output:
      - 1024
    - Solution:

    a. `while`:

    ```JAVA
         import java.util.Scanner;

         public class Application {

             public static void main(String[] args) {
                 Scanner in = new Scanner(System.in);
                 System.out.print("a = ");
                 int a = in.nextInt();
                 System.out.print("b = ");
                 int b = in.nextInt();
                 double result = 1;
                 int i = 0;
                 while (i < b) {
                     result = result * a;
                     i++;
                 }
                 System.out.println(a + " to the power " + b + " is: " + result );

             }
         }

    ```

    b. `for`:

    ```JAVA
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner in = new Scanner(System.in);
                System.out.print("a = ");
                int a = in.nextInt();
                System.out.print("b = ");
                int b = in.nextInt();

                double result = 1;

                for(int i = 0; i < b; i++) {
                    result = result * a;
                }
                System.out.println(a + " to the power " + b + " is: " + result );

            }

        }

    ```

4.  Given two numbers, not equal to 0, `n` and `p` create a JAVA program which will display in ascending order, powers of `n` which are smaller or equal to `p`

    - Sample Input:
      - n = 2
      - p = 31
    - Sample Output: 0 1 2 3 4
    - Solution:

    a. `while`

    ```JAVA
    import java.util.Scanner;

            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("n = ");
                    double n = in.nextDouble();
                    System.out.print("p = ");
                    double p = in.nextDouble();
                    int i = 0;
                    double power = Math.pow(n, i);
                    while (power <= p) {
                        System.out.print(i + " ");
                        i++;
                        power = Math.pow(n, i);
                    }

                }

            }

    ```

    b. `for`

    ```JAVA
       import java.util.Scanner;
        public class Application {

            public static void main(String[] args) {
                Scanner in = new Scanner(System.in);
                System.out.print("n = ");
                double n = in.nextDouble();
                System.out.print("p = ");
                double p = in.nextDouble();
                for(int i = 0; Math.pow(n, i) < p; i++) {
                    System.out.print(i + " ");
                }
            }
        }
    ```

5.  Create a JAVA program which will compute the first `n` pyramidal numbers, `n` read from the keyboard. A pyramidal number `n` is the sum of the first `n` perfect squares

    - Sample Input:
      - n = 5
    - Sample Output:
      - 55
    - Solution:

    a. `while`:

        ```JAVA
            import java.util.Scanner;

            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("n = ");
                    int n = in.nextInt();
                    double sum = 0;

                    int i = 1;
                    while (i <= n) {
                        sum += (i * i);
                        i++;
                    }
                    System.out.println(sum);

                }

            }

        ```

    b. `for`:

        ```JAVA
            import java.util.Scanner;

            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("n = ");
                    int n = in.nextInt();
                    double sum = 0;

                    for(int i = 1; i <=n; i++) {
                        sum += (i * i);
                    }

                    System.out.println(sum);

                }

            }

        ```

6.  Given a character `c` and a number `n`. Create a JAVA program which will display the following pyramid:

    ```json5
        c
        c c
        c c c
        .......
        c c c ... c
    ```

    - Solution:

    a. `while`:

    ````java
    import java.util.Scanner;
            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("n = ");
                    int n = in.nextInt();
                    System.out.print("c = ");
                    String character = in.next();

                    int line = 1;
                    while ( line <= n) {

                        int i = 0;
                        while (i < line) {
                            i++;
                            System.out.print(character);
                        }
                        System.out.println();

                        line++;
                    }
                }

            }

        ```

    b. `for`:
        ```java
            import java.util.Scanner;

            public class Application {

                public static void main(String[] args) {
                    Scanner in = new Scanner(System.in);
                    System.out.print("n = ");
                    int n = in.nextInt();
                    System.out.print("c = ");
                    String character = in.next();

                    for(int line = 1; line <= n; line++) {

                        for(int i = 0; i < line; i++) {
                            System.out.print(character);
                        }
                        System.out.println();

                    }
                }

            }

        ```
    ````

7.  Create a JAVA program which will display a square of `n` rows and `n` columns, where each element is equal to the character `c` read from the keyboard.

    - Sample Input:
      - n = 4
      - c = r
    - Sample Output:
      ```json5
          r r r r
          r r r r
          r r r r
          r r r r
      ```
    - Solution:
      a. `while`:

            ```java
                import java.util.Scanner;

                public class Application {

                    public static void main(String[] args) {
                        Scanner in = new Scanner(System.in);
                        System.out.print("n = ");
                        int n = in.nextInt();
                        System.out.print("c = ");
                        String character = in.next();
                        int line = 0;
                        while(line < n) {
                            int column = 0;
                            while(column < n) {
                                System.out.print(character + " ");
                                column++;
                            }
                            System.out.println();
                            line++;
                        }
                    }

                }

            ```

      b. `for`:

            ```java
                import java.util.Scanner;

                public class Application {

                    public static void main(String[] args) {
                        Scanner in = new Scanner(System.in);
                        System.out.print("n = ");
                        int n = in.nextInt();
                        System.out.print("c = ");
                        String character = in.next();

                        for(int line = 0; line < n; line++) {

                            for(int column = 0; column < n; column++) {
                                System.out.print(character + " ");
                            }
                            System.out.println();
                        }
                    }

                }

            ```

## Homework exercises

1. Create a JAVA program which will read n numbers from the keyboard and it will determine their sum
   - Sample Input:
     - n = 3
     - 1 2 3
   - Sample Output: 6
2. Create a JAVA program which will read numbers from the keyboard until the user presses 0. In the end, the program should return their sum
   - Sample Input:
     - 1 2 3 0
   - Sample Output: 6
3. Create a JAVA program which will read numbers from the keyboard until the user presses two consecutive identical numbers. The program should compute their sum
   - Sample Input:
     - 1 2 3 4
   - Sample Output: 14

Note: try to resolve the homework with both `for` and `while` instructions.

## Guidelines

- Try to redo each of the class exercises, both with while and for instructions. Then, compare your solution with the one provided in our session
- Do not forget that there are multiple solution to a problem, thus, if your solution differ than the one described, it is NOT wrong.
- At the end of each lecture, try to note everything that was new such that, if it not clear, we can talk about it in the next lesson.
