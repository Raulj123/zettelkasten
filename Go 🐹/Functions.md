Short hand if parameters have the same type
``` Go
fun myFuntion(s1, s2 string)
```

### Returning one or more values
``` Go 
fun returnOne(num int) int {
	return num + 2
}
fun returnMore(s1, s2 string) (string, int) {
	num := 26
	return s1, num
}
```

### Named returns
return values can be named and treated as their own variables inside the func
```Go
fun returnMe(s1 string) (s2 string, num int){
	s2 := "hi"
	num := 32
	return // known as naked return(i dont like this tho)
}
```

### Functions as values
aka functions are treated as values! What it says 
``` Go
fun main(){
	myFun := func() int {
		num := 2
		return num
	}
	myFun()
	// OR make it an anonymous function
	myFun := fun() {
		fmt.Println("print")
	}()
}
```

# Some definitions to know my G
* ### Scope
	* region of code in which a variable is available to use
	* #### File scope (global variables)
		* variable available throughout the file/program, global scope
	* #### Block scope (local variables)
		* In c idk if Go but define a code block by {} and if you access a var in the code block outside that block will through error
	* #### Function scope
		* var in a function once function ends var goes out of scope and gets deleted from memory
	* #### Prototype scope
		* 
### Closures
so function that returns a fun with a int param and that func returns an int
so when you first call it you have a reference to that what is being called 
hard to understand still have a hard time tbh, var doesn't get killed
``` Go
func myFunction() func(int) int {
	sum := 0

	return func(v int) int {
		sum += v

		return sum
	}
}

```go
add := myFunction()

add(5)
fmt.Println(add(10))
``` will print 15 

```
### Variadic Functions

### init

### Defer