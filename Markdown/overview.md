# Markdown Quick Reference
```md
**Bold**

_Italic_

~~Strikethrough~~
```

# Headings

```md
# H1
## H2
### H3
#### H4
```

# Links

### A basic link:

```md
<https://www.github.com/extrajp2014>
```

### Text link:

```md
[My  Github Repo](https://www.github.com/extrajp2014)
```

### Keys in paragraphs:

```md
Go to [link 1][1].

[1]: https://www.github.com/extrajp2014
```

Go to [link 1][1].

[1]: https://www.github.com/extrajp2014

# Images

```md
# Image
![alt](link)

# Image with separate key
![alt][key]

[key]: link to picture

# HTML
<img src="source.jpg" width="50px" height="50px" alt="alt text">
```

# Code Blocks

### Here is a code block:

````python
# Wrap codeblock in ```language
x = 50000;
y = 3;
# End codeblock in ```
````

### Write code in a sentence:

```js
// Wrap the code in ` `
Did you try `x += y` ?
```

### Show code diff:

````python
# Wrap the diff in ```diff
# Show error with - code
# Show correction with + code
````

```diff
let x = 1000;
- let y = 2000;
+ let y = 3000;
```

# Lists

### Unordered list

```md
+ item
+ item
+ item
```

+ item
+ item
+ item

### Ordered list

```md
1. first
1. second
1. third
```

1. first
2. second
3. third

### Nested list

```md
+ item
  * item
    * item
+ item
  * item
```

+ item
  * item
    * item
+ item
  * item

# Line Breaks

```md
// Words don't follow each other because of <br>
Sentence<br>
Sentence
```
Sentence<br>
Sentence

# Horizontal Rules

```md
Words
// space
--- //hr
// space
More Words
```

Words

---

More Words

# Block Quotes

```md
> "Any fool can write code that a computer can understand. Good programmers write code that humans can understand." 
> 
> Quote
```

> "Any fool can write code that a computer can understand. Good programmers write code that humans can understand." 
>
> Quote

# Tables

```md
|Col1|Col2|
|:--:|---:|
|Cell|Cell|
|Cell|Cell|
```

| Col1  | Col2 |
| :---: | ---: |
| Cell  | Cell |
| Cell  | Cell |

# Check boxes

```md
**Todo**
* [ ] First
* [x] Second
* [ ] Last
```

**Todo**
* [ ] First
* [x] Second
* [ ] Last