---
title: Introduction to Operating Systems
excerpt: how-to-learn-go-when-you-already-know-typeScript-very-well
publishDate: "Oct 8 2024"
tags:
  - OS
  - 
seo:
---

## Introduction

For TypeScript developers, diving into Go can be an exciting venture into a new paradigm of programming. Both languages are known for their efficiency and performance but differ significantly in syntax, design principles, and use cases. If you're well-versed in TypeScript and are looking to expand your skill set to include Go, this guide will help bridge the gap between the two languages. <br/> <br/>

In this article, we'll employ a comparison-based method to explore the differences between the two languages. By directly contrasting TypeScript and Go across various aspects, you'll gain a clearer understanding of how Go's features and design principles compare to what you're already familiar with in TypeScript.

## Understanding the differences

Before you dive into the code, it's essential to grasp the fundamental differences between TypeScript and Go:

- **Typing System:** TypeScript is a superset of JavaScript that adds static types, allowing for type safety and robust tooling. Go, on the other hand, has a statically typed nature but is designed to be simpler and more minimalistic.   
- **Concurrency:** Go shines with its built-in support for concurrency through goroutines and channels. TypeScript relies on asynchronous programming using promises and async/await.   
- **Object Orientation:** TypeScript supports classes and inheritence, while Go uses structs and interfaces, focusing more on composition rather than inheritence.

## Basic Syntax Comparison

- Defining variables <br/>
  
  TypeScript
  
  ```typescript
    let message: string = "Hello devs!";
  ```

  Go
  
  ```go
    var message string = "Hello devs!"
  ```
- Defining functions <br/> <br/>
  
  TypeScript
  
  ```typescript
    function add(num1: number, num2: number): number {
      return (num1+num2);
    }
  ```

  Go
  
  ```go
    func add(num1 int, num2 int) int {
      return (num1+num2)
    }
  ```
- Structs & Interfaces <br/> <br/>
 
  TypeScript
  
  ```typescript
    interface Student {
      name: string;
      rollNumber: number;
    }
  ```

  Go
  
  ```go
    type Student {
      Name string
      RollNumber int
    }
  ```

- Importing modules <br/> <br/>
  
  TypeScript
  
  ```typescript
    import { SomeClass } from "./SomeModule"
  ```

  Go
  
  ```go
    import "github.com/user/repo/SomePackage"
  ```

## More on Modules and Packages

1. Definition and Purpose  
   In Go, a package is a collection of related Go source files that are compiled together. Each Go source file begins with a 'package' declaration that specifies the package it belongs to whereas in TypeScript, a module is a file that exports its contents using 'export' statements and can import from other modules using 'import' statements.

2. Syntax and Structure <br/> <br/>
  
   TypeScript

   ```typescript
     // mymodule.ts
     export function myFunction() {
        // implementation
     }

     // main.ts
     import { myFunction } from './mymodule';

     myFunction();
   ```
   
   Go

   ```go
     // mypackage.go
     package mypackage

     func MyFunction() {
        // implementation
     }

     // main.go
     import "path/to/mypackage"

     func main() {
        mypackage.MyFunction()
     }
   ```

4. Visibility and Encapsulation <br/> <br/>
   
   **TypeScript Modules** <br/>
 
   In TypeScript, one controls visibility through 'export' and 'import'. Members that are exported can be accessed by importing modules, while non-exported members remain private to the module.

   ```typescript
      // mymodule.ts
      export class PublicClass {
        // implementation
      }

      class PrivateClass {
        // implementation
      }
   ```
   
   **Go Packages** <br/>

   In Go, identifiers (variables, functions, types) that start with an uppercase letter are exported (public) and accessible from other packages. Those that start with a lowercase letter are not exported (private).

   ```go
    // mypackage.go
    package mypackage

    // exported function
    func PublicFunction() {
      // implementation
    }

    // unexported function
    func privateFunction() {
      //implementation
    }
   ```

  ![Image](https://images.pexels.com/photos/26312405/pexels-photo-26312405/free-photo-of-man-with-bicycle-relaxing-over-lake-in-summer.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)
 
## Conclusion

In conclusion, I would like to offer some advice on learning a new programming language. The experience you gain while learning a new language is influenced by the languages you have previously mastered and your approach to understanding new concepts. Each individual's learning journey is unique.

Comparing the syntax of a new language with that of a language you are already familiar with can indeed facilitate quicker comprehension. However, it is crucial not to base your understanding on the logic of the previous language. Each programming language is distinct, with its own methods for solving problems, and it is unproductive to assume that concepts will translate directly from one language to another.

Approaching a new language with an open mind is beneficial. It is more effective to compare how different languages address similar problems rather than trying to interpret the new language through the lens of concepts from a language you already know.
