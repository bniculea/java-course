# Introduction to Object Oriented programming

## Objectives

- Introduction to Classes
- Homework exercises
- Guidelines

## Introduction to Classes

- Classes are the fundamental components of `Object Oriented Programming`
- Before moving on, we need to understand what `objects` are, they are the key to understanding the object oriented terminology.
- Now, just to play a bit, turn your head and look around you. You will find many examples of real world objects. For example I am looking around me and I can see the following:
  - A computer
  - A monitor
  - A chair
  - A keyboard
  - A door
  - A phone
  - Headphones
  - etc
- Real world objects have two major characteristics:
  - state
  - behavior

Now, let's pick the following object, the `computer` and analyze its characteristics:

- State:
  - The amount of RAM
  - The Operating System that it runs
  - The Hard Drive capacity
  - The size of the monitor
  - etc.
- Behavior:
  - Booting up
  - Shutting down
  - Beeping
  - Printing
  - Playing movies
  - Playing music
  - etc.

Let's take another real world example, like a `car`:

- State:
  - Color
  - Make
  - Model
  - Engine capacity
  - Seats number
  - Doors number
  - Year of fabrication
  - etc.
- Behavior:
  - Starts the engine
  - Moving
  - Starts the AC
  - Driving
  - etc.

When coming to Software Objects, they are inspired from the real world objects. This means that they also have state and behavior.

- The `state`, in objects is represented by `fields` or `attributes` (they are also referred to as properties but we will stick to the `fields` notation)
- The `behavior` of the software objects is exposed via `methods` (we talked about them in the beginning of the course)

Now you might think, `ok, we know about objects but the lesson is about classes`, well, the class is like the `template` or the `blueprint` for creating objects.

- For example, let's suppose you want to make some cakes but for that, you need a cake shape where you can pour all the ingredients.
- Here, you can see the Cake Shape as the `Class`, the ingredients as the `fields` or `attributes` and the resulting `cake` as the object

- Just think for the class that it is responsible for creating objects. There are a lot of different definitions about what a class is over the internet, they all mean the same thing but using different words :)

- Until now, we have used classes for every single exercies that we performed, for example, the following snippet might look familiar to you:
  ```java
      public class Main{
          public static void main(String[] args){
              // Code goes here
          }
      }
  ```
- Now you might think: "Well, why do I need classes as I managed to do it before them until now?"
- The answer is in the name of the data types that we have used so far, namely the `primitives`. There is so little that you can do with them and thus, you can only describe basic things. If you want, for example, to describe a person, you can, for sure, to declare variables for holding the age, sex, nationality, etc but it will be very hard for you to observe from the first that this is referring to a person.
- Classes can be seen like a custom data type, inspired from the real world, where you will use primitives in order to describe the state and the behavior of the future objects resulting from a certain class.

- Now, let's create a new class:
  - The steps for creating a class are very simple:
    1. Right click the `src` folder or the `package` where you want to class to be saved
    2. Select `New->Class`
    3. Choose a Name
    4. As we want to create a class that represents something from the real world, we don't need the main method inside it, thus, do not check the box that it will create the main method

## Homework exercises

1. Take an animal of your choice, and imagine it as an object. Try to describe its behavior and state as in the class examples

## Guidelines
