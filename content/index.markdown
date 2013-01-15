Rip is a functionally-inspired, object-oriented programming language. Here is a basic hello world:

    class {
      @.initialize = -> (name) {
        @.name = name
      }

      @.greet = -> (standard_out) {
        standard_out("Hello, #{@.name}")
      }
    }.new(:World).greet(System.IO.out)

Though this example is overly complex, it does demonstrate several things:

* Classes and lambdas are completely anonymous, just like every other object. To name anything you need to assign it to a variable.
* Instance properties are created by assigning properties to `@` inside a class definition.
* `System` defines several properties for standard classes.
* Lambdas are called by adding parenthesis
