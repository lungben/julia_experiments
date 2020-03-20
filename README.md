# julia_tutorial
Julia Tutorial


## Interesting Links

### Julia documentation

https://julialang.org/

https://discourse.julialang.org/

### Tutorials

https://github.com/crstnbr/JuliaWorkshop19

https://github.com/mfalt/juliacourse

https://www.juliabloggers.com/7-julia-gotchas-and-how-to-handle-them/

Object orientated patterns: https://github.com/ninjaaron/oo-and-polymorphism-in-julia

### University Course Material

http://ucidatascienceinitiative.github.io/IntroToJulia/

https://mitmath.github.io/18337/

http://courses.csail.mit.edu/18.337/2018/

### Cheat Sheet

https://juliadocs.github.io/Julia-Cheat-Sheet/

### Use Cases / References

https://www.hpcwire.com/2020/01/14/julia-programmings-dramatic-rise-in-hpc-and-elsewhere/

### Videos

https://youtu.be/gaJorAU644o

## Comparison of Julia and Python

Python name | Python meaning | Julia name | Julia meaning
---|---|---|---
`def f(x,y):` | named function - duck-typing, no polymorphism | `fuction f(x,y)` | duck-typing, multiple dispatch to methods
`lambda x: x` | anonymous function | `(x) -> x` | anonymous function
`class MyClass(Parent)` | classical OOP class, multiple inheritance | `struct MyStruct{TypeParameters} <: AbstractParent` | data and constructor only, types inside struct can be parametrized, can inherit only from abstract types
`def __init__(self, x):` | constructor of a class, one per class | `MyStruct(x)` (outer constructor), `MyStruct(x) = new(x)` (inner constructor) | Constructor method (multiple constructors can be defined, selected using multiple dispatch)
method | function that belongs to a class (single dispatch on first argument `self`) | method | function implementation for concete parameter types (multiple dispatch on all arguments)
module | namespace - defined as a single `.py` file | `module` | namespace - defined independenly of file strucutre
package | directory with `__init__.py` file | NA | directory structure independent of logical structure
package | bundled and installable, e.g. using `pip`, `conda` | package | includes dependencies (`Project.toml`), installable using `Pkg`, very light-weight
`x = 1 if y>0 else -1` | conditional assignment | `x = y>0 ? 1 : -1` | Ternary operator
NA | NA | `y>0 && println("y positive")`, `y>0 \|\| println("y not positive")` | short-circuit evaluation
NA | NA | `f°g` | function compositioning, `=(f°g)(x)=f(g(x))`
`obj.method1().method2()` | Chaining of methods | `1:10 \|> sum \|> sqrt` | Piping - the output of the previous function is used as input for the following one 
`@decorator` | applies a higher order function to the following `def`, often used for wrappers | `@macro` | transformation which has Julia expressions (code) as input and output (very powerful)
`with` block | context manager, used for opening and teardown of resources | `do` block | content of the block is passed as anonymous function to function before `do` statement
`raise Exception` | raising Exceptions | `throw(Exception)` | raising Exceptions
`try` - `except` - `finally` | Exception handling, can be used as part of normal program workflow | `try` - `catch` - `finally` | Exception handling, should not be part of normal program workflow due to performance reasons

