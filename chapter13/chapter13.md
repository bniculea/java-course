# Exercises with Arrays and Matrices

## Objectives

- Recap previous session
- Exercises with arrays
- Exercises with matrices
- Homework exercises
- Guidelines

## Recap previous session

- Give an example of a real life situation where sorting helps
- How can we swap the value of two variables?
- What is a multidimensional array?
- What is the difference between a simple array and a 2D array?
- How do you access an element from an array?
- How do you access an element from a 2D array?

## Exercises with arrays

1. Given an array with `n` elements, create a JAVA program which will compute the absolute difference between the number of even numbers and number of odd numbers.

   - Sample Input:
     - n = 5
     - 15 245 28 33 11
   - Sample Output:
     - 3
   - Solution:

   ```java
       import java.util.Scanner;

       public class Application {

           public static void main(String[] args) {
               Scanner keyboard = new Scanner(System.in);
               System.out.println("Enter n: ");
               int n = keyboard.nextInt();
               int[] numbers = new int[n];
               for(int i = 0; i < numbers.length; i++) {
                   System.out.println("Enter a number: ");
                   numbers[i] = keyboard.nextInt();
               }

               int numberOfEvenElements = 0;
               int numberOfOddElements = 0;
               for(int i = 0; i < numbers.length; i++) {
                   if(numbers[i] % 2 == 0) {
                       numberOfEvenElements++;
                   } else {
                       numberOfOddElements++;
                   }
               }

               int difference = Math.abs(numberOfEvenElements - numberOfOddElements);
               System.out.println(difference);
           }
       }
   ```

2. Given an array with `n` elements, create a JAVA program which will display the elements which are multiples of the last element of the array.

   - Sample Input:
     - n = 5
     - 7 4 9 6 2
   - Sample Output: 4 6 2
   - Solution:

     ```java
         import java.util.Scanner;

         public class Application {

             public static void main(String[] args) {
                 Scanner keyboard = new Scanner(System.in);
                 System.out.println("Enter n: ");
                 int n = keyboard.nextInt();
                 int[] numbers = new int[n];
                 for(int i = 0; i < numbers.length; i++) {
                     System.out.println("Enter a number: ");
                     numbers[i] = keyboard.nextInt();
                 }

                 for(int i = 0; i < numbers.length; i++) {
                     if(numbers[i] % numbers[numbers.length-1] == 0) {
                         System.out.print(numbers[i] + " ");
                     }
                 }
             }
         }
     ```

3. Given an array with `n` elements, create a JAVA program which will display the elements with even indices in the ascending order of the indices, and the elements with odd indices, in the descending order of the indices.

   - Sample Input:
     - n = 5
     - 7 9 2 6 8
   - Sample Output:
     - 7 2 8
     - 6 9
   - Solution:

     ```java
        import java.util.Scanner;

        public class Application {

            public static void main(String[] args) {
                Scanner keyboard = new Scanner(System.in);
                System.out.println("Enter n: ");
                int n = keyboard.nextInt();
                int[] numbers = new int[n];
                for(int i = 0; i < numbers.length; i++) {
                    System.out.println("Enter a number: ");
                    numbers[i] = keyboard.nextInt();
                }

                for(int i = 0; i < numbers.length; i++) {
                    if(i % 2 == 0) {
                        System.out.print(numbers[i] + " ");
                    }
                }

                System.out.println();

                for(int i = numbers.length-1; i  > 0; i--) {
                    if(i % 2 != 0) {
                        System.out.print(numbers[i] + " ");
                    }
                }
            }
        }
     ```

4. Given an array with `n` elements, create a JAVA program which will display the elements of the array in the following order: first, last, second, second to last, etc

   - Sample Input:
     - n = 4
     - 2 9 1 5 8
   - Sample Output:
     - 2 8 9 5 1
   - Solution:

     ```java
         import java.util.Scanner;

         public class Application {

             public static void main(String[] args) {
                 Scanner keyboard = new Scanner(System.in);
                 System.out.println("Enter n: ");
                 int n = keyboard.nextInt();
                 int[] numbers = new int[n];
                 for(int i = 0; i < numbers.length; i++) {
                     System.out.println("Enter a number: ");
                     numbers[i] = keyboard.nextInt();
                 }

                 int lastIndex = numbers.length-1;

                 for(int startIndex = 0; startIndex < lastIndex; startIndex++, lastIndex--) {
                     System.out.print(numbers[startIndex] + " " + numbers[lastIndex] + " ");
                 }

                 if(numbers.length % 2 != 0)  {
                     System.out.print(numbers[numbers.length/2]);
                 }
             }
         }
     ```

5. Given an array with `n` elements, create a JAVA program which will display the numbers between the element with the minimum value and the element with the maximum value, including both of them (closed interval)

   - Sample Input:
     - n = 5
     - 7 9 6 2 8
   - Sample Output:
     - 9 6 2
   - Solution:

     ```java
         import java.util.Scanner;

         public class Application {

             public static void main(String[] args) {
                 Scanner keyboard = new Scanner(System.in);
                 System.out.println("Enter n: ");
                 int n = keyboard.nextInt();
                 int[] numbers = new int[n];
                 for(int i = 0; i < numbers.length; i++) {
                     System.out.println("Enter a number: ");
                     numbers[i] = keyboard.nextInt();
                 }

                 int minPos = findMinPos(numbers);
                 int maxPos = findMaxPos(numbers);
                 displaySection(numbers, minPos, maxPos);
             }

             private static void displaySection(int[] numbers, int minPos, int maxPos) {
                 int startIndex = Math.min(minPos, maxPos);
                 int endIndex = Math.max(minPos, maxPos);

                 for(int i = startIndex; i <= endIndex; i++) {
                     System.out.print(numbers[i] + " ");
                 }

             }

             private static int findMinPos(int[] numbers) {
                 int minPos = 0;
                 for(int i =0; i < numbers.length; i++) {
                     if(numbers[i] < numbers[minPos]) {
                         minPos = i;
                     }
                 }
                 return minPos;
             }

             private static int findMaxPos(int[] numbers) {
                 int maxPos = 0;
                 for(int i =0; i < numbers.length; i++) {
                     if(numbers[i] > numbers[maxPos]) {
                         maxPos = i;
                     }
                 }
                 return maxPos;
             }
         }
     ```

## Exercises with matrices

## Homework exercises

## Guidelines

- Each recap section contains topics that we discussed in previous meetings
- It is best that you answer them and write them down, not to learn it by hard but it will speed the process of learning due to visualization.
- Everything that is new, should be noted and maybe discussed in the following session(s) in case if it is not well understood
- Of course, at each session, you can choose to speak about a certain topic that you are interested in.
