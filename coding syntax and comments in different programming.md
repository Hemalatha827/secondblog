# ** Coding Syntax and Comments in Different Langauges**



## Table of Contents :

In this Blog you are going to learn  about the   keywords , Variables, Variables scope like const, let , final in various programming languages.

## Keywords :

Keywords are a set of reserved words that cannot be used as names of functions, labels, or variables as they are already a part of the syntax of programming 
language.Each of the keywords has its own meaning.

## List of Keywords:
```js
while	case	class	void	function	instanceof

throw	export	delete	catch	private	package

true 	debugger	extends	default	interface	super

with	enum	if	return	switch	try

let	yield	typeof	public	for	static

new	else	finally	false	import	var

do	protected	null	in	implements	this

await	const	continue	break	

```
Scope determines the accessibility (visibility) of variables.

It has 3 types:

* Block scope
* Function scope
* Global scope

  ## Block Scope:

   Variables declared inside a { } block cannot be accessed from outside the block.
     The two important new JavaScript keywords: let and const.

  ## Local Scope:

  Variables declared within a JavaScript function, become LOCAL to the function.
  Local variables are created when a function starts, and deleted when the function is completed.

  ## Function Scope:

  Variables declared with var, let and const are quite similar when declared inside a function.
  Variables defined inside a function are not accessible (visible) from outside the function.

  ## javascript:

  In the below example function represents as a keyword . var,let const are the function scopes that has been used.

  ```js
  function myFunction(){
  var carName="Volvo";
  let number=30;
  const value=10;
  }
  ```

  ## TypeScript:

   ```Typescript
  function addNumbers(){
   let num1:number =10;
   let num2:number=20;
   if(true){
   
   let num3:number =15;
   console.log(num3);
  }
   if(true){
   const num4:number =20;
   console.log(num4);
   }
   return num1+num2;
   }
   console.log(addNumbers());
  ```
   ##Explanation for the TypeScript program code:
  
    In this example, we have a function called addNumbers() that adds two numbers num1 and num2 with values 5 and 10, respectively. The function also demonstrates different variable scopes in TypeScript:

## Local variables: 

num1 and num2 are declared within the function scope and are accessible only within the addNumbers() function.

## Block-scoped variables: 

Inside the if blocks, num3 and num4 are declared using let and const, respectively. They are accessible only within their respective block scopes.

## Global variable: 

The function returns the sum of num1 and num2, which is accessible outside the function as it is a global variable.

## Dart:

In the below example we are initializing two global variables globalnum1 ,globalnum2. And we are calling the addNumbers() function. The addNumbers() function add the num1 and num2 values  and return the sum value. Then it can also access and  print global variable values . Global variables can be accessed outside the function.

```Dart
  void main(){

   // Global variables
    int globalnum1 =5;

    int globalnum2=10;

     addNumbers()
   }

  void addNumbers(){
    // Local Variables
    int num1=2;

    int num2=3;

     int sum=num1+num2;

     printf(sum);

   printf("The globalnum1 is :" $ globalnum1);

   printf("The globalnum2 is :" $ globalnum2);
 }  
  ```

## PHP:

Here  first we will be initializing two variables like $number1 ,$number2. Then we are calling addNumbers function. This function will return sum of two values as 8.  The result value can be displayed inside a function. It cannot be accessed outside the function. if we try to print the sum outside the function it will return the value as 0.

 ```PHP
  <? php

   function addNumbers($a ,$b){

    $result=$a+$b;

    echo "Inside function call :" .$result."\n";

    }

    $number1 =5;

    $number2 =3;

    echo "Before function call :" .$result."\n";

    addNumbers($number1 ,$number2);

     echo "After  function call :" .$result."\n";
  ?>
  ```

  ## Java:
   In this example below first we have initalized globalsum. Then we are initializing two  variables as num1 and num2 .We are passing the input data to add function It will store the value in the result variable. The error will occurs if we are trying to access the num1 value outside the add function.

  ```Java
      public class Main(){
       static int globalSum;
      public static void main(String[] args){
          int num1=5;
          int num2=10;

          int sum=add(num1,num2);
          System.out.println("The sum is :"+sum);
          System.out.println("The globalSum is:+globalSum);
          }

          public static int add( int a ,int b){
            int result;
            result=a+b;
            globalSum=result;
            
             return result;
             }
             }
  ```

 ## Kotlin:

  Here in this program the global variables are initalized as number1 ,number2 .Then we are passing these global variables to addNumbers function. Finally it will store the sum of two values in a sum variable and it will be displayed. Here result is a local variable.

  ```kotlin
  fun main() {
    val number1 = 5
    val number2 = 10
    val sum = addNumbers(number1, number2)
    println("The sum is: $sum")
}

fun addNumbers(num1: Int, num2: Int): Int {
    val result = num1 + num2
    return result
}
 
  ```

  ## Swift:
  
  Here in this program func is a keyword. a ,b are the variables which has a variable scope as let . The  scope let keyword can be accessed inside a function.
  It will add a  and b and final value will be stored in the sum.
    
  ```Swift
  func addNumbers() {
    let a = 5 // Local variable within the function
    let b = 10 // Local variable within the function
    let sum = a + b // Local variable within the function
    
    print("Sum: \(sum)")
}

addNumbers() // Calling the function
  ```

##Golang:

we have a global variable globalResult that can be accessed throughout the program. The main function defines local variables num1 and num2, which are passed as arguments to the addNumbers function. 
The addNumbers function has its own local variable result, and the result is assigned to the globalResult variable. Finally, the sum is printed in the main function along with the value of globalResult.

   ```Golang
  // Global variables
var globalResult int

func main() {
	// Local variables within main function
	var num1, num2 int = 10, 20

	// Calling the addNumbers function
	sum := addNumbers(num1, num2)
	fmt.Println("Sum:", sum)

	// Accessing the globalResult variable
	fmt.Println("Global Result:", globalResult)
}

// Function to add two numbers
func addNumbers(a, b int) int {
	// Local variable within addNumbers function
	result := a + b

	// Assigning the result to the globalResult variable
	globalResult = result

	// Returning the result
	return result
}

  ```

## C ,C++, Objective -C:

C
 ```C
  #include<stdio.h>
  int addNumbers(int a, int b) {
    int sum = a + b;
    return sum;
}

int main() {
    int num1 = 5;
    int num2 = 3;
    int result = addNumbers(num1, num2);
    printf("The sum is: %d\n", result);
    return 0;
}
  ```
C++

 ```C++
  # include<iostream>
  int addNumbers(int a, int b) {
    int sum = a + b;
    return sum;
}

int main() {
    int num1 = 5;
    int num2 = 3;
    int result = addNumbers(num1, num2);
    std::cout << "The sum is: " << result << std::endl;
    return 0;
}
  ```

Objective-C
  ```Objective-C
  #import <Foundation/Foundation.h>

NSInteger addNumbers(NSInteger a, NSInteger b) {
    NSInteger sum = a + b;
    return sum;
}

int main(int argc, const char * argv[]) {
    @autoreleasepool {
        NSInteger num1 = 5;
        NSInteger num2 = 3;
        NSInteger result = addNumbers(num1, num2);
        NSLog(@"The sum is: %ld", result);
    }
    return 0;
}

  ```

     




