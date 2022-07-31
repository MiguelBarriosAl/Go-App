![](images\go-logo.PNG)
# **Introducing Goland**

Welcome to the Go wiki, my collection of information about the [Go Programming Language](https://go.dev/). [Awesome Go](http://awesome-go.com/). The purpose of this repository is to acquire and collect the basic knowledge to create a Go application.

# Table of Contents
- [Packages](#introducing-goland)
- [Basic nomenclatures](#basic-nomenclatures)
- [#GOPATH](#gopath)
- [Flags](#flags)
- [Sources](#sources)

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

    - IF...ELSE

    - SWITCH:

        Keyword `switch` and then define all possible cases with `case`. Each of the cases is usually isolated by the reserved word `break`. However, this behavior is already predefined by default in Go. So, we will only explicitly indicate when we want to concatenate two `case` by using the `fallthrough` keyword, as follows:
        https://go.dev/play/p/PXWJuVlZ9sp


## $GOPATH

During the installation of Go we have defined where our $GOPATH will be located, the $GOPATH is nothing more than the path where our workspace will be located, normally it is usually found in:

    ~/go

But we can change it to wherever we want by changing the $GOPATH environment variable.

## Flags
The flag package offers us different types of parses. Note that when we read these options in our console based on the flag package, they will be returned as pointers.
https://blog.friendsofgo.tech/posts/crear-tu-primer-cli-en-go/


## Sources:
- https://pro.codely.com/library/introduccion-a-go-tu-primera-app-43842/89042/about/
- https://blog.friendsofgo.tech/
- https://forum.golangbridge.org/
- https://github.com/golang/go/wiki

