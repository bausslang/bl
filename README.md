# bl
The primary frontend compiler for bausslang.

---

Bausslang is a statically typed programming language created as a simple learning project. The goal is to create a C-like programming language inspired by D, C#, Rust, Go, C and C++.

Eventually the goal is to write the compiler in itself.

It will intiailly use a C compiler as the backend but will be abstract enough to have that changed in the future.

The language should be as safe as possible, not just memory-wise.

Memory safety will be guaranteed with RAII, cleaning up when scopes end, as well check all variables set if they are cleaned somewhere in the code and emit errors when something has a possibility to leak memory.

For memory critical sections manual memory management can be enabled but only in unsafe code which can only be called from unsafe scopes themselves, which limits unsafe functionality to a subset of the language.

---

### Hello World!

```
fn main()
{
  import std.stdio : writeln;
  
  writeln("Hello World!");
}
```

```
fn int main()
{
    ...

    return 0;
}
```

```
fn main(string[]:const args)
{
    ...
}
```

---

### Current Status

**Tokenization**: Done

**Tokenized Grouping**: Done

**Parser**: In Progress

**-- Module Statement**: Done
  
**-- Import Statement**: Done

**-- Variable Declaration**: Not Started

**-- Type Information**: Done
  
**-- Functions**: Done

**-- Function Body**: Done

**---- Return Expressions**: Done

**-- Expressions**: Done

**-- Arrays**: Done

**-- Associative Arrays**: Done

**-- Function Calls**: Done

**---- Chained Function Calls**: Not Started

**-- If/Else/Else If Statements**: Not Started

**-- Switch Statements**: Not Started

**-- For Statements**: Not Started

**-- Foreach Statements**: Not Started

**-- While Statements**: Not Started
  
**CTFE**: Not Started

**Semantic Analysis**: In Progress

**Parse Code To C**: Not Started

**Compile Parsed C Code**: Not Started
