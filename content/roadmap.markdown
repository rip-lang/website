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
    * block-based objects - class, lambda, if et cetera
    * number
      * integer - `42`
      * decimal - `4.2`
    * character - ``a`
    * string - `:symbol`, `'single quoted'`, `"double quoted #{with_interpolation}"`
    * regular expression - `/regular expression #{also_with_interpolation}/`
    * list - `[1, 2, 3]`
    * map - `{ :a : 1, lambda() : 5 }`
    * key-value - `:key : :value`
    * range - `1..5` or `1...10` (two dots mean inclusive range. three dots mean range end is excluded. `1..9` is essentially the same as `1...10`)
    * date - `2012-02-12` (date, time and datetime literals are always UTC. time and datetime can have an optional +/- timezone offset in hours)
    * time - `00:24:00.0329+0400` (with optional fractional seconds and timezone offset)
    * datetime - `2012-02-12T00:24:00` (literal date and time separated by a capital T)
  * module loaders
    * file - This will be the most common module loader. The file loader is pretty much does the same thing node's `require` keyword does.
    * url - Just like the file loader, but with full URLs. :)
    * other - Support for any kind of module loader will be available for projects to load code from pretty much anywhere, such as a database.

* v1.0 - In addition to everything above working (and working well), the following items need to be accounted for before the official first release.
  * Standard libraries will be useful enough to build real, production systems with without re-inventing all the wheels.
  * This website will look good, be informative and have tutorials, downloads for all supported platforms and links to external resources (such as integration packs for various editors).
  * The documentation section of the website will cover at least most of the standard library.

* v1.x
  * LINQ keyword support - Syntactical sugar for SQL-like keywords that operate on any kind of collection. Collections will already be lazy-iterated; this only adds keyword support the API already in place.
  * distributed package repository - A website to make finding third-party packages easy. The actual packages will be distributed; only package meta-data will be in the registry.
  * advanced object literals (or sooner if easy)
    * heredoc (with interpolation)
    * version - `v0.1.3` (as in [SemVer](http://semver.org/) need to evaluate usefulness)
  * unit object literals (à la CSS)
    * Also need a way to register new units that fits in with current language semantics

* v2.0
  * concurrency/parallelism/asynchronicy (may need to be addressed sooner)
  * type restrictions for collection types (syntax similar to C# generics)
