% TSC(1) tsc Manual
% pingrat <http://pingrat.github.io/>
% March 12, 2014

# NAME

tsc - TypeScript compiler

# SYNOPSIS

tsc [*OPTIONS*] \[*sources*]...

# DESCRIPTION

TypeScript is a typed superset of JavaScript that also provide classes, modules, and interfaces. It compiles to plain ECMAScript 3 or ECMAScript 5 compliant JavaScript.

TypeScript is open source and developed by Microsoft with the motto 'Any browser. Any host. Any OS.' and can be used in virtually any ECMAScript 3-capable JavaScript host.

One typical host could be Node.js, a popular implementation using the V8 JavaScript engine. Compiling TypeScript for Node is simple:

    tsc -t ES5 -m commonjs --out output.js source.ts

Here saying we want to have ECMASCript 5 code generated and use the CommonJS module format since Node handles both. You can also combine multiple input files, which will be concatenated in output.js:

    tsc -t ES5 -m commonjs --out output.js source1.ts source2.ts source3.ts

Or, if you want to preserve the file structure of your TypeScript sources, the following creates three files, **build/source1.js**, **build/source1.js**, **build/source3.js**:

    tsc -t ES5 -m commonjs --outDir build/ source1.ts source2.ts source3.ts

Finally you can define sources by globbing:

    tsc -t ES5 -m commonjs --out output.js src/**/*.ts

# OPTIONS

-d, \--declaration
:   Generates corresponding .d.ts file.

-h, \--help
:   Print help message.

\--mapRoot *LOCATION*
:   Specifies the location where debugger should locate map files instead of generated locations.

-w, \--watch
:   Watch input files.

(compiler support/features)

-v, \--version
:   Print the compiler's version, e.g. `Version 0.9.7.0`.

-t, \--target *STRING*
:   Specify ECMAScript target version: **ES3** (default), or **ES5**).

-m, \--module *STRING*
:   Specify module code generation: **commonjs** or **amd**.

\--noImplicitAny
:   Warn on expressions and declarations with an implied **any** type.

\--removeComments
:   Do not emit comments to output.

\--sourcemap
:   Generates corresponding .map file.

\--sourceRoot *LOCATION*
:    Specifies the location where debugger should locate TypeScript files instead of source locations.

(files)

\--out *FILE*
:   Concatenate and emit output to single file.

\--outDir *DIRECTORY*
:   Redirect output structure to the directory.

# NOTES ON OPTIONS

Theoretically, code should run with improved characteristics when specifying the target version to be ECMAScript 5 although this can be completely implementation-specific.

# SEE ALSO

The TypeScript website for partial documentation and example code can be found at <http://www.typescriptlang.org/>.

The TypeScript open source project is hosted on CodePlex at <https://typescript.codeplex.com/>.

# DISCLAIMER

This manual was created by user pingrat, <https://pingrat.github.io/>, who have zero affiliations with Microsoft or the TypeScript core team. Deemed up to date as of TypeScript compiler version 0.9.7.0.

<!--
Version 0.9.7.0
Syntax:   tsc [options] [file ..]

Examples: tsc hello.ts
          tsc --out foo.js foo.ts
          tsc @args.txt

Options:
  -d, --declaration             Generates corresponding .d.ts file.
  -h, --help                    Print this message.
  --mapRoot LOCATION            Specifies the location where debugger should locate map files instead of generated locations.
  -m KIND, --module KIND        Specify module code generation: 'commonjs' or 'amd'
  --noImplicitAny               Warn on expressions and declarations with an implied 'any' type.
  --out FILE                    Concatenate and emit output to single file.
  --outDir DIRECTORY            Redirect output structure to the directory.
  --removeComments              Do not emit comments to output.
  --sourcemap                   Generates corresponding .map file.
  --sourceRoot LOCATION         Specifies the location where debugger should locate TypeScript files instead of source locations.
  -t VERSION, --target VERSION  Specify ECMAScript target version: 'ES3' (default), or 'ES5'
  -v, --version                 Print the compiler's version: 0.9.7.0
  -w, --watch                   Watch input files.
  @<file>                       Insert command line options and files from a file.
 -->
