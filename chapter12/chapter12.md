# Multidimensional arrays

## Objectives

- Recap previous session
- Introduction
- Class exercises
- Homework exercises
- Guidelines

## Recap previous session

- What is an Array?
- Why and when do we need an array?
- An array of int, is a primitive or an object? Why?

## Introduction

- A two-dimensional array can be declared as follows:

  ```java
      int [][] chessTable = new int[8][8];
  ```

  - This declares the chessTable array with 8 sets of 8 integers elements each. Note how each dimension is between its own pair of square brackets
  - You can visualize a two-dimensional array as a rectangular arrangement like, in our previous example, a table which has `8 rows` and each row has `8 columns`.

- Even though we can visualize them as rows and columns, in memory, all the elements are stored sequentially.
  - For example, let's suppos we have the following two-dimensional array: `int numbers[3][3]`
  - In memory, the elements are stored sequentially as follows:
    - `numbers[0][0] | numbers[0][1] | numbers[0][2] | numbers[1][0] | numbers[1][1] | numbers[1][2] | numbers[2][0] | numbers[2][1] | numbers[2][2]`
- Another way of visualizing a two-dimensional array is like an array of elements where each element is an array itself
  - A simple array is also called a `one-dimensional` array of elements
- A 2 Dimensional array is also called a matrix

### Initializing Multidimensional arrays

- If you remember from the previous lesson, a simple array can be initialized as follow:

  ```java
        double[] arr = new double[] {1.2, 2.3, 2.6, 2.8, 2.9};
  ```

- Now, in order to extrapolate, 2D array, can be initialized in a similar manner:

  ```java
      double[][] arr = new double[][] {
                  {1.0, 2.3, 3.4},
                  {1.1, 3.3, 4.4}
              };
  ```

  - Here, each element is an array itself, that's why we are saying that a matrix or a 2D array is an array of arrays.

- Another way of initializing a 2D array is to process all elements using a repetitive instruction (loop). In order to iterate through all elements, a nested loop is needed. See the snippet below where we initialize each element with a random number between 1 and 10 and then we display the matrix:

  ```java
      import java.util.Random;

      public class Application {

          public static void main(String[] args) {
              int[][] matrix = new int[3][3];
              Random random = new Random();

              for(int i = 0; i < matrix.length;i++) {
                  for(int j = 0; j < matrix[i].length; j++) {
                      int randomInt = random.nextInt(11);
                      matrix[i][j] = randomInt;
                  }
              }

              displayMatrix(matrix);
          }

          public static void displayMatrix(int[][]matrix) {
              for(int i = 0; i < matrix.length;i++) {
                  for(int j = 0; j < matrix[i].length; j++) {
                      System.out.print(matrix[i][j] + " ");
                  }
                  System.out.println();
              }
          }

      }
  ```

- Now, let's get through each of the lines from the previous JAVA snippet:

TODO: - Explain length - Explain Random - Explain sorting - Add examples with sorting
