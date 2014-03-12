tsc.1.man
=========

Simple man page for the TypeScript compiler.

# Installation

Copy the `tsc.1` file to your systems manual repository folder.

In Ubuntu 13.10, the following works:

```bash
$ git clone https://github.com/pingrat/tsc.1.man

# should be pretty quick...

$ cd tsc.1.man
$ sudo gzip tsc.1 /usr/share/man/man1/tsc.1.gz
```

I have no idea if this is the correct way of adding a manual. There's probably some way to add it for only your own user without resorting to `sudo`.

# Usage

To view the manual page for tsc:

```bash
$ man tsc
```

To recompile the markdown source you need *the* **boss markup transgulfer** [pandoc])(http://johnmacfarlane.net/pandoc/).

# TODO

More examples?

# LICENSE

MIT

