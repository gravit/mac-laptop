Laptop
======

Laptop is a script to set up an OS X laptop for web development.  This is a
hacked/simplified version of the original
[laptop](https://github.com/thoughtbot/laptop) project from Thoughtbot.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Requirements
------------

We support:

* OS X Mavericks (10.9)
* OS X Yosemite (10.10)
* OS X El Capitan (10.11)

Older versions may work but aren't regularly tested. Bug reports for older
versions are welcome.

Install
-------

Download, review, then execute the script:

```sh
curl --remote-name https://raw.githubusercontent.com/gravit/mac-laptop/master/mac
less mac
sh mac 2>&1 | tee ~/laptop.log
```

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`.
Read through it to see if you can debug the issue yourself.

What it sets up
---------------

Mac OS X tools:

* [Homebrew] for managing operating system libraries.

[Homebrew]: http://brew.sh/

Unix tools:

* [OpenSSL] for Transport Layer Security (TLS)
* [Tmux] for saving project state and switching between projects

[OpenSSL]: https://www.openssl.org/
[Tmux]: http://tmux.github.io/


Programming languages and configuration:

* [Ruby] v1.9.3-p194 for our current code bases
* [Bundler] v1.11.2 for managing Ruby libraries
* [Rbenv] for managing versions of Ruby
* [Ruby Build] for installing Rubies

[Bundler]: http://bundler.io/
[Rbenv]: https://github.com/sstephenson/rbenv
[Ruby Build]: https://github.com/sstephenson/ruby-build
[Ruby]: https://www.ruby-lang.org/en/

Databases:

* [MySQL] v5.5 for storing relational data

[MySQL]: https://www.mysql.com/

It should take less than 15 minutes to install (depends on your machine).

Customization
-------

You can customize/add to what gets installed via the  `~/.laptop.local` script, which is run at the end of the Laptop script.  See [Thoughtbot's README](https://github.com/thoughtbot/laptop) for more details.


License
-------

Laptop is © 2011-2016 thoughtbot, inc.
It is free software,
and may be redistributed under the terms specified in the [LICENSE] file.
This version has no additional licensing restrictions.

[LICENSE]: LICENSE


