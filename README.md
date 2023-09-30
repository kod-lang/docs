
# The Kod Programming Language

Welcome to the official documentation for the Kod programming language!

> **Note:** This project is a work in progress.

## Why another programming language?

Kod aims to strike a unique balance: it's designed to be both easy to learn and practical to use. Moreover, its architecture is straightforward, making it an excellent educational resource for those interested in learning about compiler design and language implementation. However, don't mistake it for a mere educational toy; Kod is a fully functional programming language capable of powering real-world applications. It draws inspiration from well-established languages like Lua, Python, and JavaScript, yet stands on its own merits.

## What does it look like?

To give you a taste of Kod, here's a simple "Hello, World!" script:

```js
println("Hello, World!");
```

For a more complex example, consider this function to calculate factorials:

```js
function factorial(n) {
  if (n == 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
```

As you can see, Kod's syntax is reminiscent of JavaScript, while its semantics share similarities with Python. However, Kod is not intended to be a clone of either language; it aims to carve out its own niche, complete with its own unique features.

## What are its features?

Here are some of Kod's standout features:

- **Lightweight:** Designed for lightweight implementation and simple syntax, Kod is easy on system resources.

- **Embeddable:** Kod can easily be embedded into other applications, boasting a simple C API reminiscent of Lua's industry-leading model.

- **Interoperability:** Seamless communication between Kod and C is made possible through interoperability features, allowing data to be exchanged effortlessly.

- **Cross-platform:** Written in C, Kod offers support for Windows, macOS, and Linux, and can be easily ported to other platforms.

- **Imperative with functional flair:** Primarily an imperative language, Kod also supports functional programming paradigms, offering flexibility in choosing the most suitable approach for each task.

- **Dynamic typing:** Kod employs dynamic typing, allowing variables to be assigned a type at runtime for increased flexibility. However, this comes at a performance trade-off.

- **Optional type annotations:** You can optionally annotate variable types, as well as parameter and return value types, for improved type safety.

- **Lexical scoping:** Variable scope is determined by its placement within the source code, enabling nested functions and facilitating the creation of closures.

- **Interfaces:** The language includes support for interfaces, letting you define a set of methods that a type must implement. This provides a form of polymorphism without relying on inheritance.

- **First-class citizens:** Functions, classes, and interfaces are all first-class citizens in Kod. This design choice allows them to be passed around and manipulated like any other data type.

- **Mutable Value Semantics:** Kod employs mutable value semantics, which restrict the sharing of mutable states between variables and across different scopes.

- **Generators:** The language supports specialized functions that can pause and resume their execution. This functionality allows for the creation of custom iterators.

- **Reference Counting:** Memory management is handled through reference counting, freeing up memory as soon as it is no longer needed and obviating the need for a tracing garbage collector.

## License

Kod is licensed under the [MIT](https://choosealicense.com/licenses/mit) license. For more information, please refer to the [LICENSE](LICENSE) file.
