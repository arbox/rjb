# `Rjb` is Ruby-Java Bridge
[![RubyGem](https://img.shields.io/gem/v/rjb.svg)](https://rubygems.org/gems/rjb)

RJB is a Bridge library which connects Ruby and Java code using the Java Native Interface.

Besides this `README` you can find information on `Rjb` in the following ressources:

* the [Ruby Kaigi 2010](http://www.slideshare.net/artonx/j-ruby-kaigi-2010)
  Presentation on `Rjb`;
*  short [introduction](https://www.artonx.org/collabo/backyard/?RubyJavaBridge)
   in English;
* some [examples](https://www.artonx.org/collabo/backyard/?RjbQandA) in
  Japanese, but the source code is clear for everybody.

An in depth [introduction](https://www.artonx.org/collabo/backyard/?RjbMechanism)
into the internals of `Rjb` is recommended for developers.

# How to install

An older [description](https://www.artonx.org/collabo/backyard/?HowToBuildRjb)
how to build `Rjb` by `@arton` could be a very good starting point.

You need to install Java2 sdk, and setup `JAVA_HOME` enviromental
varible except for OS X. I assume that OS X's `JAVA_HOME` is reported
by calling `/usr/libexec/java_home`.

This done please proceed with:

``` bash
ruby setup.rb config
ruby setup.rb setup
```

``` bash
# (in Unix)
sudo ruby setup.rb install
```

or

``` bash
# (in win32)
ruby setup.rb install
```

# Tutorial



# How to test

On Windows based machines:

``` bash
cd test
ruby test.rb
```

On Unix based machines plese see `test/readme.unix`. You need to set
`LD_LIBRARY_PATH` environmental variable to run `rjb`.

# Notice for opening non-ASCII 7bit filename

If you'll plan to open the non-ascii character named file by Java
class through Rjb, it may require to set LC_ALL environment variable
in you sciprt.

For example in Rails, set above line in `production.rb` as your environment:

``` bash
ENV['LC_ALL'] = 'en_us.utf8' # or ja_JP.utf8 etc.
```

cf: http://bugs.sun.com/view_bug.do?bug_id=4733494
   (Thanks Paul for this information).

# Contact
artonx@yahoo.co.jp
