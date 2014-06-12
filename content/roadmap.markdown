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
      * class - <code class="language-rip">class {}</code>
      * lambda - <code class="language-rip">=> {}</code>
      * overload - <code class="language-rip">-> {}</code>
    * number
      * integer - <code class="language-rip">42</code>
      * decimal - <code class="language-rip">4.2</code>
      * rational - <code class="language-rip">2 / 3</code>
      * imaginary numbers are accessed with the <code class="language-rip">i</code> property on any real number
      * complex - <code class="language-rip"><42, 3.i></code>
    * character - <code class="language-rip">`a</code>
    * string - <code class="language-rip">:symbol</code>, <code class="language-rip">'single quoted'</code>, <code class="language-rip">"double quoted #{with_interpolation}"</code>
    * heredoc (with interpolation, same as double quoted string)
    * regular expression - <code class="language-rip">/regular expression #{also_with_interpolation}/</code>
    * list - <code class="language-rip">[1, 2, 3]</code>
      * type-restricted list - <code class="language-rip">[1, 2, 3]<System.Integer></code>
    * map - <code class="language-rip">{ :a : 1, lambda() : 5 }</code>
      * type-restricted map - <code class="language-rip">{ :a : 1, lambda() : 5 }<System.Object, System.Integer></code>
    * key-value - <code class="language-rip">:key : :value</code>
    * range - <code class="language-rip">1..5</code> or <code class="language-rip">1...10</code> (two dots mean inclusive range. three dots mean range end is excluded. <code class="language-rip">1..9</code> is essentially the same as <code class="language-rip">1...10</code>)
    * date - <code class="language-rip">2012-02-12</code> (date, time and datetime literals are always UTC. time and datetime can have an optional +/- timezone offset in hours)
    * time - <code class="language-rip">00:24:00.0329+0400</code> (with optional fractional seconds and timezone offset)
    * datetime - <code class="language-rip">2012-02-12T00:24:00</code> (literal date and time separated by a capital T)
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
  * version - <code class="language-rip">v0.1.3</code> (as in [SemVer](http://semver.org/) need to evaluate usefulness)

* v2.0
  * concurrency/parallelism/asynchronicy (may need to be addressed sooner)
