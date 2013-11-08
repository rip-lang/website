---
menu:
  text: Getting Started
  position: 1
published: false
---

## Getting Started

1. Clone the repo: `$ git clone git://github.com/rip-lang/rip.git`
2. Change into directory: `$ cd rip`
3. Install system dependencies (OSX specific, sorry):
   * Install Ruby 2. Use Homebrew to install `rbenv` and `ruby-build`, then `$ rbenv install ruby-2.0.0-p0`
   * Install LLVM: `$ brew install llvm --enable-shared --enable-jit`
4. Install Ruby dependencies: `$ gem install bundler; bundle install`
5. Verify everything installed correctly by running `$ bundle exec rspec` to run the tests

Rip comes with a command-line executable at `./bin/rip`. Type `./bin/rip help` for usage details. Some [examples are on GitHub](https://github.com/rip-lang/samples) to get you going. Please note that some of theses may be outdated; pull-requests are welcome :). If you get an error, please [open an issue](https://github.com/rip-lang/rip/issues) with the exact Rip source code and a copy of the error message. Also let me know if you have any trouble or are unsure about something; I will be happy to help!
