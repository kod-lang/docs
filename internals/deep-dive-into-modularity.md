
# Deep dive into modularity

This guide will lead you to a deeper understanding of how modularity works in the Kod programming language, including implementation details and usage examples.

## What is modularity?

Before we begin, let's define what modularity is. Modularity is the ability of a system to be divided into smaller parts, known as modules, which can be combined to form a larger system.

## Modules in Kod

In Kod, a module is a source code file (`.kod` file) that contains definitions of functions, classes, interfaces, variables, etc. A module can be imported by other modules, allowing them to access the definitions within it.

## How to import a module?

To import a module, use the `import` keyword followed by the path of the module file. For example, to import the `foo.kod` module located in the `bar` directory within the current directory, you can do the following:

```js
import "bar/foo.kod";
```

This form is known as "local module import". There are two more ways to import a module: global module import and package import.

## Global module import

The language carries along with it a set of modules in the global scope called Core Modules. These modules are imported simply by specifying the module's name, as in the example below:

```js
import io;
```

> Note the absence of quotes around the module name.

The import mechanism depends on the `KOD_HOME` environment variable, which should point to the root directory of the Kod installation. If this variable is not customized, a runtime error will occur: "unable to find modules".

## Package import

A package is a directory that contains one or more modules (`.kod` files). Importing a package is similar to importing a local module in that it uses quotes, but the package path is preceded by an `@`:

```js
import "@foo";
```

In this case, the module import mechanism will be governed by the `KOD_PATH` environment variable. If this variable is not customized, the `main module` of the `foo` package in the `dependency directory` within the current directory will be imported.

The default value for `KOD_PATH` is `deps/?/main.kod`. This means that the main module is `main.kod` and the dependency directory is `deps`. The `?` is a wildcard character that will be replaced by the package name.

So, the full path to the main module of the `foo` package will be `deps/foo/main.kod`.
