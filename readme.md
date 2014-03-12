tsc.1.man
=========

Simple man page for the TypeScript compiler.

# Installation

Copy the `tsc.1` file to your systems manual repository folder.

In Ubuntu 13.10, the following works:

```zsh
$ git clone https://github.com/pingrat/tsc.1.man

# should be pretty quick...

$ cd tsc.1.man
$ sudo gzip tsc.1 /usr/share/man/man1/tsc.1.gz
```

I have no idea if this is the correct way of adding a manual or if it will eventually burn your house down and stab you while you sleep. There's probably some way to add it for only yourself.

# Usage

To view the manual page for tsc:

```bash
$ man tsc
```

To recompile the markdown source you need *the* **boss markup transgulfer** [pandoc](http://johnmacfarlane.net/pandoc/).

# TODO

Not a GOD DAMN THING. Stupid TypeScript.

# LICENSE

MIT

