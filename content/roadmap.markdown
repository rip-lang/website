---
menu:
  position: 1
---

## Roadmap

The roadmap below is of course subject to change, but these are the milestones I would like to target.

* v0.x
  * working parser
  * well-defined, holistic semantics
  * basic object literals
    * block-based objects
      * class - `class {}`
      * lambda - `=> {}`
      * overload - `-> {}`
    * number
      * integer - `42`
      * decimal - `4.2`
      * rational - `2 / 3`
      * imaginary numbers are accessed with the `i` property on any real number
      * complex - `<42, 3.i>`
    * character - ``a`
    * string - `:symbol`, `'single quoted'`, `"double quoted #{with_interpolation}"`
    * heredoc (with interpolation, same as double quoted string)
    * regular expression - `/regular expression #{also_with_interpolation}/`
    * list - `[1, 2, 3]`
      * type-restricted list - `[1, 2, 3]<System.Integer>`
    * map - `{ :a : 1, lambda() : 5 }`
      * type-restricted map - `{ :a : 1, lambda() : 5 }<System.Object, System.Integer>`
    * key-value - `:key : :value`
    * range - `1..5` or `1...10` (two dots mean inclusive range. three dots mean range end is excluded. `1..9` is essentially the same as `1...10`)
    * date - `2012-02-12` (date, time and datetime literals are always UTC. time and datetime can have an optional +/- timezone offset in hours)
    * time - `00:24:00.0329+0400` (with optional fractional seconds and timezone offset)
    * datetime - `2012-02-12T00:24:00` (literal date and time separated by a capital T)
  * module loaders
    * file - Modules are loaded relative to the module doing the requiring. Absolute paths are also allowed
    * package - Package load path is built from source directory plus vendor source directories
    * url - Just like the file loader, but with full URLs. :)
  * type restrictions for class, lambda, list, map, key-value (similar syntax to C# generics)
    * range is implicitly type restricted
  * lambda overloads

    ```language-rip
     # lambda (`foo`) with two overloads
     #   the second overload takes a single parameter (`a`)
     foo = => {
     	-> {}
     	-> (a) {}
     }
     ```

* v1.0 - In addition to everything above working (and working well), the following items need to be accounted for before the official first release.
  * Standard libraries will be useful enough to build real, production systems with without re-inventing all the wheels.
  * This website will look good, be informative and have tutorials, downloads for all supported platforms and links to external resources (such as integration packs for various editors).
  * The documentation section of the website will cover at least most of the standard library.

* v1.x
  * LINQ keyword support - Syntactical sugar for SQL-like keywords that operate on any kind of collection. Collections will already be lazy-iterated; this only adds keyword support the API already in place.
  * distributed package repository - A website to make finding third-party packages easy. The actual packages will be distributed; only package meta-data will be in the registry.
  * unit object literals (à la CSS)
  * version - `v0.1.3` (as in [SemVer](http://semver.org/) need to evaluate usefulness)

* v2.0
  * concurrency/parallelism/asynchronicy (may need to be addressed sooner)
