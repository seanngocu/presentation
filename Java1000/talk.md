# Java 1000

* Introductions


# Lambda Expressions

* Part of Java 8


# Why Java needs Lambda expressions?

* Objects are the base of Java
* Cant have stand-alone functions


# Why Java needs Lambda expressions?

* Allows Java to act like a functional programming language
* CAN have stand alone functions


# Pre-Lambda expression
```Java
public class Foo{
	public int Add(int a, int b){
	return a + b
	}
}
```
* This is how you traditionally wrote functions in Java


# Pre-Lambda expression 

```Java
	Foo F = new Foo()
	F.Add(4,5)
```
* You would have to create an instance of the class to call the function

 
# What is a Lambda epression?

* Esentially it is a function without a declaration 
* allows you to write the function in the same place you are using it

# What is a Lambda expression?
```Java
 (arguments) -> {body} 
```

* This is the format for Lambda expressions

# Example code

```java
(String first, String second)
     -> Integer.compare(first.length(), second.length())
```

# Why Lambda Expressions?

* Functional Programming
* Simplified syntax for streamlined coding

# When to use Lambda Expressions?

* The ability execute the code later in time
* When the code could be used multiple times

# Syntax

* Optional type declaration
* Optional parenthesis around parameter

# Syntax

* Optional curly braces
* Optional return keyword


# Convience of Lambda expressions
```Java 
	String[] nba = {"Kobe Bryant", "Lebron James", "Steph Curry", "Kevin Durant", "Klay Thompson"};
	List<String> players =  Arrays.asList(nba);
       
	// Old looping
	for (String player : players) {
	    System.out.print(player + "; ");
	}
       
	// Using lambda expression and functional operations
	players.forEach((player) -> System.out.print(player + "; "));
 
	// Using double colon operator in Java 8
	players.forEach(System.out::println);
```



* makes iterating through a list very easy


# Effects of Lambda expressions

* Flexibility
* Adaptability


# Restrictions to Lambda expression

* No more than one abstract method 
* Java 8 or higher


# seventeenth slide

* This is the third slide
* There are 17 more slides after this one
* Good luck with your presentation!
* 


# eighteenth slide

* This is the third slide
* There are 17 more slides after this one
* Good luck with your presentation!
* 


# Conclusion

* Functional Programming in Java
* flexable modeling allows for easy coding


# twentyth slide

* http://www.drdobbs.com/jvm/lambda-expressions-in-java-8/240166764



