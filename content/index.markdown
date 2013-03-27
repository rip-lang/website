---
menu:
  text: Home
  position: 0
---

Rip is a functional, object-oriented programming language. Check out this convoluted hello world:

    class {
      @.initialize = -> (name) {
        @.name = name
      }

      @.greet = -> (standard_out) {
        standard_out("Hello, #{@.name}")
      }
    }.new(:World).greet(System.IO.out)

Though this example is overly complex, it does demonstrate several things:

* Classes and lambdas are completely anonymous, just like every other object. To name anything you need to assign it to a reference.
* Lambdas may be passed around like any other object.
* Lambdas are called by adding parenthesis.

Additionally it would be helpful to know that...

* `System` is a predefined object which defines several properties for standard classes.
* Classes have a property, `Class#@` aka the prototype, which is used to define what instances will look like (similar to JavaScript's prototype, but not ugly).
* Lambdas have a property, `Lambda#@`, which is a reference to the current receiver (similar to JavaScript's `this` keyword when used inside a function).

If you like what you see, stay tuned: the rest of this site is forthcoming.
