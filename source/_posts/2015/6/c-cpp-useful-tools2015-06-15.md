---
title: c/cpp-useful-tools
date: 2015-06-15 11:57:15
categories: technique
tags: c/c++
keywords: [c, c++, tool]
toc:
---

### cdecl

 Cdecl  (and  c++decl) is a program for encoding and decoding C (or C++) type declarations.

 [cdecl online website](http://cdecl.org/)

### size(on mac)

size -- print the size of the sections in an object file.
`size -x(print by hex) -l -m a.out`

<!-- more -->
### otool(on mac)

otool -- object file displaying tool.
`otool -s __TEXT(which segment) __text(which section) a.out`

### nm(on mac)
see the symbol table
`nm libwens.so`

### strings
find the printable strings in a object, or other binary, file 
