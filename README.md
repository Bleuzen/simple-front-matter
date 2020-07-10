# simple-front-matter
Minimalistic front-matter for JavaScript & TypeScript

## Install

```bash
npm install -S simple-front-matter
```

## Example

If you have a file called `example.md`:

```
---
title: Hello world
description: Just an example post
---

This is the content of the post
```

Then you can do this:

```javascript
const matter = require('simple-front-matter')
const fs = require('fs')

fs.readFile('./example.md', 'utf8', (err, data) => {
    if (err) throw err
    const post = matter(data)
    console.log(post)
})
```

To get an object like this:

```javascript
{
  attributes: {
    title: 'Hello world',
    description: 'Just an example post'
  },
  body: 'This is the content of the post',
  bodyBegin: 6,
  frontmatter: 'title: Hello world\ndescription: Just an example post'
}
```

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
