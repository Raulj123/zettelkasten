# If/Else
same as python just curly braces
``` Go
if x > 5 {
	fmt.Println("x is greater")
} else if x < 5 {
	fmt.Println("less than 5")
}

// COMPACT if, this is common ig
if x := 10; x > 5 {
	fmt.Println("x is greater")
}
```

# Switch
Break statement is auto at the end of each case, evaluates from top -> bottom 

``` Go
fun main(){
	day := "Monday"
	switch day {
	case "Monday":
		fmt.Println("work!")
		fallthrough
		// adding fallthrough will go to the next case
	case "Friday":
		fmt.Println("errm")
	default:
		fmt.Println("hehe")
	}
}
// work!
// errm
```
There is a shorthand for this!

# For loop
In go only one loop 
``` Go
fun main(){
	for i =0; i < 5; i++ {
		fmt.Println(i)
	}
	break
	continue
	// break and continue are a thing
	for ;i<10 {
		// init and post statements are optional
	}
}
```

