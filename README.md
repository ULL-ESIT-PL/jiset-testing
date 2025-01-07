#  Exploring the way TC39 proposals are checked

## Tools used 

See the dependencies in https://github.com/tc39/ecma262/blob/main/package.json

Appears [ecmarkup](https://github.com/tc39/ecmarkup) is used to generate the HTML files from the markdown files. 
[emu-format](https://github.com/tc39/ecmarkup/blob/main/bin/emu-format.js) is used to format the HTML files.


## Introduction to JISET (deprecated)

### What is JISET?

**JISET** stands for **JavaScript IR-based Semantics Extraction Toolchain**

There is a warning in the README.md:

> **Warning** - This repository is no longer maintained. Instead, please use
> [ESMeta](https://github.com/es-meta/esmeta), a rebranded version of JISET.

**JISET** is a **J**avaScript **I**R-based **S**emantics **E**xtraction
**T**oolchain. It is the first tool that automatically synthesizes parsers and
AST-IR translators directly from a given language specification, ECMAScript.

#### Publications

Details of the JISET framework are available in our papers:
- [ASE 2020] [JISET: JavaScript IR-based Semantics Extraction
  Toolchain](https://doi.org/10.1145/3324884.3416632)
- [ICSE 2021] [JEST: N+1-version Differential Testing of Both JavaScript
  Engines](https://doi.org/10.1109/ICSE43902.2021.00015)
- [ASE 2021] [JSTAR: JavaScript Specification Type Analyzer using
  Refinement](https://ieeexplore.ieee.org/document/9678781)

#### Overall Structure

![image](https://user-images.githubusercontent.com/6766660/124231185-e91d3380-db4a-11eb-95b5-dc43f4341ff2.png)

### Installation

#### Download JISET
```bash
$ git clone https://github.com/kaist-plrg/jiset.git
```

#### Errors during `sbt` execution

After many attempts of installing jiset, the errors persisted during `sbt` execution.
So I donwladed a zip file from https://github.com/sbt/sbt/releases/download/v1.9.8/sbt-1.9.8.zip and it worked.

#### Setting up the environment

Set the environment variables in `.zshrc` as follows:

```
## JISET JavaScript IR-based Semantics Extraction Toolchain
## for JISET https://github.com/kaist-plrg/jiset
export JISET_HOME=/Users/casianorodriguezleon/campus-virtual/2425/learning/compiler-learning/jiset # "<path to JISET>" 
export PATH="$JISET_HOME/bin:$PATH" # for executables `jiset` and etc.
source $JISET_HOME/jiset-auto-completion # for auto completion
```

and

```
➜  jiset git:(analyzer) export SBT_HOME=/Users/casianorodriguezleon/campus-virtual/2425/learning/compiler-learning/jiset/sbt # "<path to JISET>"
export PATH="$SBT_HOME/bin:$PATH" # for executables `sbt` and etc. 
```

#### Simple Examples

Then 

```
➜  jiset git:(analyzer) ✗ sbt
```

The command `assembly` also worked:

```
➜  jiset git:(analyzer) ✗ sbt assembly
...

➜  jiset git:(analyzer) ✗ ls -l bin/                             
total 67624
-rwxr-xr-x@ 1 casianorodriguezleon  staff        56  7 ene 10:28 esparse
-rwxr-xr-x@ 1 casianorodriguezleon  staff        62  7 ene 10:28 extract-trace
-rwxr-xr-x@ 1 casianorodriguezleon  staff  33909054  7 ene 12:05 jiset
-rwxr-xr-x@ 1 casianorodriguezleon  staff        59  7 ene 10:28 mimic-test
-rwxr-xr-x@ 1 casianorodriguezleon  staff        60  7 ene 11:35 unicode-gen
```

Then the first command `jiset` worked without errors:

```
➜  jiset git:(analyzer) ✗ jiset gen-model -extract:version=es2021
========================================
 extract phase
----------------------------------------
version: es2021
parsing spec.html... (11.053 ms)
========================================
 gen-model phase
----------------------------------------
generating models... (836 ms)
```

then I went to another vscode workspace in this project:

```
/Users/casianorodriguezleon/campus-virtual/2122/learning/compiler-learning/jiset-testing
```

and set the environment variables in `.env` for the terminal:


```
➜  jiset-testing git:(main) ✗ cat .env
export JISET_HOME=/Users/casianorodriguezleon/campus-virtual/2425/learning/compiler-learning/jiset # "<path to JISET>" 
export PATH="$JISET_HOME/bin:$PATH" # for executables `jiset` and etc.
source $JISET_HOME/jiset-auto-completion # for auto completion
export SBT_HOME=/Users/casianorodriguezleon/campus-virtual/2425/learning/compiler-learning/jiset/sbt
export PATH="$SBT_HOME/bin:$PATH
```
```
➜  jiset-testing git:(main) ✗ source .env
```

The parsing worked:

```
➜  jiset-testing git:(main) ✗ jiset parse sample.js 
========================================
 parse phase
----------------------------------------
var x = 1 + 2 ; print ( x ) ;

➜  jiset-testing git:(main) ✗ time jiset eval sample.js -silent
3.0
jiset eval sample.js -silent  10,47s user 1,07s system 308% cpu 3,743 total
```

The times are awful. The `debug` command produces a lot of output.  [A 763883 chars output](debug.log.md):

```
➜  jiset-testing git:(main) ✗ wc debug.log.md 
   16737   61702  763883 debug.log.md
```

### Basic Commands

See the output of [jiset help](jiset-help.md).