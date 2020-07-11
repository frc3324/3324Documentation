# Classes
## What are classes?
Classes are a way for you to create your own objects with both *state* (class variables) and *behavior* (methods). 
You can have state and methods separately of course, for example: structs let you have state and functions have behavior, but classes enable you to couple things together and use OOP concepts such as polymorphism.
Alright, so lets look at a class:
```kotlin
class DoesNothing() { // Note: class name is in upper camel case
}
```
This class, as the name describes, does nothing. 
Let's make a class with some state:
```kotlin
class State(val x: Double, val y: Double) { 
}
```

Here we make a class that takes in two doubles and stores them. 
If you omit the `val` before either variable, the variables will only be used in the "constructor" (we'll get to constructors later).

Let's look at what it'll look like if you wanted to use this class in your code:
```kotlin
fun main() {
	val newClass = State(1.0, 2.0)
	println(newClass.x) // prints 1.0
}
```
Ok, neat, but how do we add behavior that interacts with the state?
Let's try another example of a class with behavior:
```kotlin
class State(val x: Double, val y: Double) {
	fun printX() {
		println(x);
	}
}
```
And the corresponding code in main:
```kotlin
fun main() {
	val newClass = State(1.0, 2.0)
	newClass.printX()
}
```

## Ok but why
> "Managing complexity is the most important technical topic in software development. 
> In my view, it's so important that Software's Primary Technical Imperative
> has to be managing complexity. 
> Complexity is not a new feature of software development."
> -Steve McConnell

In Kotlin/Java, classes are *required*. 
There are no structs (but there are data classes in Kotlin) so all state needs
to stored be in a class.
Arguments for whether state should be coupled with behavior in this way are more nuanced, but we will do it regardless on the team, so it's worth learning.

## Further Steps
To learn more check out the data classes chapter and the chapter on inheritance/polymorphism.
