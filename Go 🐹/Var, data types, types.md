## Variables
If no value is given will default to 0 

``` Go
var first, last string = "raul", "j"
var (
    first string = "raul"
    last string = "j"
)

var foo = "hi foo"     // Inferred
foo := "hi foo"        // var and type is implicit (only in func blocks)


```

## Data Types
#### String
a sequence of bytes
``` Go
var foo string = "hi"
var foo string = ` this is another way.
                    can do this too`
```

#### Bool
``` Go
var t bool = true
fmt.Println(a && b) // false (because one of them is false)
fmt.Println(a || b) // true (because at least one is true)
fmt.Println(!a) // false (negation of true)****
```

#### Int
``` Go
var i int = 32
```

### **Size Comparison**

| Type             | Size              | Range                               |
| ---------------- | ----------------- | ----------------------------------- |
| `byte` (`uint8`) | 8 bits (1 byte)   | `0` to `255`                        |
| `rune` (`int32`) | 32 bits (4 bytes) | `-2,147,483,648` to `2,147,483,647` |

#### Byte and Rune 
``` Go
var b byte = 'a'
var r rune = ':pizza:'
```

#### Floats
default is float64
``` Go
var f32 float32 = 1.7812 // IEEE-754 32-bit
var f64 float64 = 3.1415 // IEEE-754 64-bit
```

## Operators
Go provides several operators for performing operations on numeric types.

|Type|Syntax|
|---|---|
|Arithmetic|`+` `-` `*` `/` `%`|
|Comparison|`==` `!=` `<` `>` `<=` `>=`|
|Bitwise|`&` `\|` `^` `<<` `>>`|
|Increment/Decrement|`++` `--`|
|Assignment|`=` `+=` `-=` `*=` `/=` `%=` `<<=` `>>=` `&=` `\|=` `^=`|
# Type Conversion
In order to print a type 
``` Go
var foo string = "foo"
fmt.Printf("%T", foo)
```

# Alias
Allow to provide an alternate name to an existing type(string, bool, int, etc.) and use it interchangeably with underlying type
Just another name for string
``` Go
type Mine = string
func main(){
    var foo Mine = "see how I replaced string w Mine"
}
```

# Defined Types
Do not use a =, unlike alias. BUT what's the difference??
 Defined types **create a brand-new type** based on an existing one. This new type **is not interchangeable** with the original type
``` Go
type MyDefined string // MyDefined is a new type based on string

func main() {
    var def MyDefined = "Hello"
    var normalString string = def // :x: ERROR: cannot use def as string

    fmt.Println(normalString)
}
```