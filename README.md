![](/images/gologo.png)

# **Introducing Goland**

Welcome to the Go wiki, my collection of information about the [Go Programming Language](https://go.dev/). [Awesome Go](http://awesome-go.com/). The purpose of this repository is to acquire and collect the basic knowledge to create a Go application.

# Table of Contents
- [Packages](#introducing-goland)
- [Basic nomenclatures](#basic-nomenclatures)
- [#GOPATH](#gopath)
- [Flags](#flags)
- [Sources](#sources)
- [Data](#data)


## Packages

A set of Go (.go) files headed by the 'package package-name' statement and residing in the same directory.
When importing other packages, we can do it in several ways, all of them using the `import` keyword, either in its individual version or in its bulk version:

https://go.dev/play/p/ms0xZrON7dt

The different ways to import packages are:

- The standard way (using `import` and the package name).
- The dot imports (to avoid having to put the package name in the code).
- Underscore imports (to import packages that are not explicitly referenced).
- Aliases (to rename the imported package, e.g. in case of name collision).

## Basic nomenclatures
- VARIABLE
    - The short format (using `:=`)
    - The long format (using `var`)
- FUNCTIONS

    The use of upper or lower case letters in the name of the name will define its visibility at the packet level.
    To define a function we will make use of the keyword ' func'. The arguments of the function will be defined in the following order: variable name and type, being able to concatenate several variables of the same type. In addition, we will also define the return type of the function, which can be implicit or explicit:

    https://go.dev/play/p/WmHexwyGwE1

- LOOPS

    When programming loops, in Go we will use the `for` keyword. This can be used in several ways:

    In the traditional way, following the format: initialization; completion; iteration.
    Together with the `range` keyword (e.g. for traversing data structures)

    https://go.dev/play/p/KIyhreDZGRW

- CONDITIONS

    A la hora de escribir código condicional, tenemos algunas de las opciones habituales en la mayoría de lenguajes de programación:

    - IF/ELSE
    - SWITCH

        Keyword `switch` and then define all possible cases with `case`. Each of the cases is usually isolated by the reserved word `break`. However, this behavior is already predefined by default in Go. So, we will only explicitly indicate when we want to concatenate two `case` by using the `fallthrough` keyword, as follows:
        https://go.dev/play/p/PXWJuVlZ9sp


## $GOPATH

During the installation of Go we have defined where our $GOPATH will be located, the $GOPATH is nothing more than the path where our workspace will be located, normally it is usually found in:

    ~/go

But we can change it to wherever we want by changing the $GOPATH environment variable.
Similar to how Python looks for imported libraries in the Python path, Go searches the GOPATH for the same. A notable difference between Python and Go paths is that Go expects all your Go projects to live within the GOPATH, specifically /go/src. Contrast this with Python where projects can live anywhere.

The GOPATH directory is made up of 3 subdirectories:

![](/images/2022-07-31-22-08-19.png)

## Flags
The flag package offers us different types of parses. Note that when we read these options in our console based on the flag package, they will be returned as pointers.

## Data
- **SLICE**

    Is a representation above an array
    This representation is contained in the following information:

    - Pointer to the first element of the underlying array.
    - Slice length
    - Slice capacity

            func main(){
                beers := make([]string, 3)
                fm.Println("empty slice:", beers)
                beers[0] = "estrella"
                beers[1] = "buckler"
                beers[2] = "mahou"
                fmt.Println("beers:", beers)
            }

        https://go.dev/play/p/tZ_gd59MKu4

- **MAPS**

   Key-value structure which, in Go, are implemented by means of a HashMap.

        func main(){
            b := make(map[string]float32)
            b["mahou"] = 0.59
            b["buckler] = 0,60
            fmt.Println("beers", b)
        }

    https://go.dev/play/p/6AtqM9utZne

- **STRUCTS**

    They are data structures formed by lists of attributes characterized by a name and a type. The way to declare a struct is by using the struct keyword with its definition following between braces ({ }). It is important to remember that the case-sensitive rule also applies here to determine whether the attributes are public or private.
    https://go.dev/play/p/V32fuTZXbYD

- **INTERFACES**

    Keywork: Interfaces

        func send(encrypter interface{ Encrypt([]byte) string }) {
        // method implementation
        }

    Function called `send` with a parameter `encrypter`, which is a variable that is an `interface` that has an `Encrypt` method, which receives an array of `bytes` and returns a `string`.

- **DEFINED TYPES**

    The defined types also known as type alias are types created from the definition of other basic or native types of the language (e.g. string, struct, interface, func, channel, etc).

    The way to define a defined type is by using the reserved word type and then the type it represents. This allows us to give semantics to our code

        package main

        import "time"

        type page struct {
            number int
            header string
            text   string
        }

        type book struct {
            title       string
            autor       string
            releaseDate *time.Time
            pages       []page
        }



    

## Sources:
- https://pro.codely.com/library/introduccion-a-go-tu-primera-app-43842/89042/about/
- https://blog.friendsofgo.tech/
- https://forum.golangbridge.org/
- https://github.com/golang/go/wiki
- https://hackersandslackers.com/create-your-first-golang-app/
    

