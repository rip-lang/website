---
title: Project Layout
menu:
  position: -1
---

## Standard Rip Project Layout

* global installs are not necessary or encouraged (for development)
* ./bin and ./vendor/bin should be added to PATH (not required for binary compiles)
* ./lib and ./vendor/\*/lib are added to Rip's load paths
* a rip package is a collection of modules with a package module at the root
* package modules live in ./lib


<pre>
project_dir/
|-bin/
| `-project_bin
|-docs/
|-lib/
| `-project_name/
|-tests/
| |-integration/
| |-support/
| `-unit/
|-public/
|-vendor/
| |-bin/
| | `-dependency_two -> ../dependency_two/bin/dependency_two
| |-dependency_one/
| | `...
| `-dependency_two/
|   `...
|-LICENSE.markdown
|-package.rip
`-README.markdown
</pre>
