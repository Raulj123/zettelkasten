fmt has lots of shi here are the basics
``` Go
fmt.Print("hi","my")
// himy
fmt.Println("my","hi")
//my hi (with new line at end)
```

#### Printfn
aka print formatter
%s - are called annotation verbs tell the function how to format arguments
``` Go
name := "raul"
fmt.PrintF("%s", name)

```

#### Sprint, Sprintln, Sprintf
they return the string instead of printing 
``` Go
s := fmt.Sprintf("hex:%x bin:%b", 10, 10)
fmt.Println(s)
// hex:a bin:1010
```

