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
    5. After the class is created, it should automatically be opened by the Eclipse IDE

- Note: there is a convention to name the classes starting with an uppercase letter and then, each following word from its name, to start with a capital letter. See the examples below:
  ```json
      Good        Bad
      Car         car
      DataStore   dataStore
                  DATASTORE
                  data_store
  ```
  - also, if you remember from our previous lessons, there are some rules when speaking about the characters that can be used in the name of a class.
- After your class is created, it should look similar to the one below: (of course, the name might vary but the structure should be similar):

  ```java
      public class Car {

      }
  ```

- If you want to see more details about what happened behind the scene, right click the class in the package explorer, select `Show in -> System explorer`
- This will take you to the exact location, on your disk, where this java class has been created and here you can open the class file with any editor of your choince
- Now, you might wonder what is the `public` keyword about, well, this is called an `access modifier` and simply refers to what access do we want to allow others to have to this new class.
  - Long story short, `public` means unrestricted access to the class
  - In the future, we will go in details about other access modifiers, until then, just use `public` for your classes
- The next part, in making our newly created class useful, is to create some variables that are part of this class

  - Until now, you have only seen variables created in methods (main method and other custom method), these variables are called `local variables` because they are local to that specific method, meaning that once you get out of the method, the variables do not exist anymore.
  - Classes allow us to create variables that are accessbile to all the methods in the class. These are also known as `member variables` but as we spoked at the beginning of this lesson, most commonly they are referred to as `fields`.

  - Regarding the declaration of a class `field`, we also can (and should) use access modifiers here. Unlike for classes which most commonly are `public`, fields usually have the `private` access modifier. This is because you should always adhere to the principle of `encapsulation` which is a key fundamental rule of `object-oriented programming`. In a very short sentence, `encapsulation` refers to hiding the internal state of an object from the outside eyes, and only expose the functionality that we want. Remember, an object is an entity created from our blueprint, from our class.

  - Now, let's create a new class field for our brand new class `Car`. The field will hold the brand of the car. First, let's take a look at how it is looking and then we will take each part and discuss it:

```java
    public class Car {
        private String brand;

    }
```

- Now, we have talked about the `private` keyword, it simply means that no one from the outside of this class can access this field
- The following should look pretty similar to what you have done so far, countless time, when declaring a variable. As you can see, after we specify the `access modifier` we have to specify the type and the name of the `field`, which we will use when referring to it, while using it across the class
- Another very important thing that you should notice is the positioning of the `field`. The fields are placed inside the class's braces and usually at the top of the class, starting with the very first line after the opening brace of the class
- The name of the field should follow the same rules as for simple variables, you should start with a lowercasee letter and then, each following word should use an uppercase letter. If you want to know more about the naming, you can revisit the lesson that we had in the very beginning of this course.
- The fields of a class can be seen as the characteristics of that specific class. In our example, the brand field indicates us what brand does a specific car has. Of course, we can create as many field as we want. And that's why we will create a few more fields for our class as in the snippet below:

```java
    public class Car {
	    private String brand;
	    private String model;
	    private int doors;
	    private int engineCapacity;
	    private String color;
}
```

- Now the class has more characteristics that we can use in order to create our own `Car` objects. Just notice that apart from the `private` keyword, they look like basic variable

## Homework exercises

1. Take an animal of your choice, and imagine it as an object. Try to describe its behavior and state as in the class examples

## Guidelines
