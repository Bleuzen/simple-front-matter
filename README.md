# simple-front-matter
Minimalistic front-matter for JavaScript

## Why another front-matter library?

While the other libraries depend on a big yaml parser, this one has no dependencies and is ultra lightweight.  
It is mainly made for small client-side applications where you want to keep the app size small and load times fast.  
Off course this comes with some limitations.

## Limitations

Since there is no real yaml parser in use, you can't use all yaml features.  
Front parsing is very basic.  
You are limited to one line per attribute.

## Original source

This library is a modified version of front-matter by jxson.  
You can find the original source code here:  
https://github.com/jxson/front-matter
