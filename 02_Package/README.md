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

### Build your first program
`Notice: ` change your directory to `$GOPATH` and execute the following command
```
go build go_dev/day1/example1 
```

![](https://raw.githubusercontent.com/3lackrush/easy-golang/master/Assets/02_Packages_assets/build.png)