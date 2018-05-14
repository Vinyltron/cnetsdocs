 \mainpage Documentation Help
 
## Introduction

Welcome to the CNETS Dochub.
This documentation site uses a combination of plaintext/markdown files and the Doxygen documentation generator to create a HTML site structure that is easily traversible.
Supported languages include:

  * C
  * C++
  * C#
  * Objective-C
  * IDL
  * Java
  * VHDL
  * PHP
  * Python
  * Tcl
  * Fortran
  * D

### Pages

 * \subpage correctSyntaxPage "Syntax to use"
  

\page correctSyntaxPage Syntax to use

Here is some information on the correct syntax to use in order to comment your code to be recognised by the Doxygen system.

See [here](http://www.stack.nl/~dimitri/doxygen/manual/docblocks.html) for full details

  * \subpage cSyntax "Syntax for C style Languages"
  * \subpage pythonSyntax "Syntax for Python"
  * \subpage vhdlSyntax "Syntax for VHDL"

\page vhdlSyntax

\page pythonSyntax

The following Syntax is used to document Python

```python
    ## @package pyexample
    #  Documentation for this module.
    #
    #  More details.
    ## Documentation for a function.
    #
    #  More details.
    def func():
        pass
    ## Documentation for a class.
    #
    #  More details.
    class PyClass:
   
        ## The constructor.
        def __init__(self):
            self._memVar = 0;
   
        ## Documentation for a method.
        #  @param self The object pointer.
        def PyMethod(self):
            pass
     
        ## A class variable.
        classVar = 0;
        ## @var _memVar
        #  a member variable
```

\page cSyntax

The following Syntax is used to document C/C++/C#/Objective-C/PHP/Java languages

You can use the JavaDoc style, which consist of a C-style comment block starting with two *'s, like this:
```
/**
 * ... text ...
 */
```
or you can use the Qt style and add an exclamation mark (!) after the opening of a C-style comment block, as shown in this example:
```
/*!
 * ... text ...
 */
```
In both cases the intermediate *'s are optional, so
```
/*!
 ... text ...
*/
```
is also valid.

A third alternative is to use a block of at least two C++ comment lines, where each line starts with an additional slash or an exclamation mark. Here are examples of the two cases:
```
///
/// ... text ...
///
```
or
```
//!
//!... text ...
//!
```
Note that a blank line ends a documentation block in this case.

Some people like to make their comment blocks more visible in the documentation. For this purpose you can use the following:
```
/********************************************//**
 *  ... text
 ***********************************************/
```
(note the 2 slashes to end the normal comment block and start a special comment block).

or
```
/////////////////////////////////////////////////
/// ... text ...
/////////////////////////////////////////////////
```