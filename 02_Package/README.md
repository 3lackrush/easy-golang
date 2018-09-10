## First Golang Program

```go
package main

import (
  "fmt"
)

func main() {
  fmt.Println("Hello world")
}
```

## Package in go

- We put the code with same function in a single directory like we do in python. We call this directory as package.  
- Package could be referenced by other packages.
- Main package is used to generate executable file and every program has only one main package.
- The main purpos of the package is to improve the reusability of the code.

## Directory Structure
### The standard directory structure in golang project as follow.
```
D:\project
├─bin
├─pkg
├─src
│  └─go_dev
│      └─day1
│          └─example1
└─vender
```
> Explanation
> `bin` directory is used to store executable binary file
> `src` directory is used to store source code
> `pkg` is used to  store static library
> `vender` is used to store third-party packages


### Set GOPATH in your system environment
![](https://raw.githubusercontent.com/3lackrush/easy-golang/master/Assets/02_Packages_assets/GoPATH.png)

### Build your first program
`Notice: ` change your directory to `$GOPATH` and execute the following command
```
go build go_dev/day1/example1 
```

![](https://raw.githubusercontent.com/3lackrush/easy-golang/master/Assets/02_Packages_assets/build.png)

### Another sample project
The project structure is as follow
```
D:.                               
└─project_sample                  
    ├─bin                         
    ├─pkg                         
    ├─src                         
    │  └─go_dev                   
    │      └─day1                 
    │          ├─example1         
    │          └─package_example  
    │              ├─calc         
    │              └─main         
    └─vendor                      
```
Source code of `add.go`
```
package calc

func Add(a int, b int) int {
      return a + b
}
```

Source code of `sub.go`
```
package calc

func Sub(a int, b int) int {
    return a - b
}

```
Source code of `main.go`
```
package main

import (
    "go_dev/day1/package_example/calc"
    "fmt"
)

func main() {
	sum := calc.Add(100, 300)
	sub := calc.Sub(100, 300)

	fmt.Println(sum)
	fmt.Println(sub)
}

```
`If you want to call function from a package. The function name must be uppercase!`
