---
draft: true
title: "Theme"
slug: "theme"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

# TOC

To enable it, all you need to do when creating a new post at the very top is to insert the code:
```toml
toc = true
tocBorder = true
```

# Details

{{< details summary="Click me" >}}
A lot of text or something else.
{{< /details >}}

```markdown
{< details summary="Click me" >}
A lot of text or something else.
{< /details >}
```

# Styles

`/config.toml`
  ```toml
  appearance = "auto"
  ```
  you can change it to 2 predefined styles: **light** and **dark**. It can be also set to **auto** and the color scheme will match the user's system style.
- you can add new style or modify **auto** option, just edit CSS in ../themes/nostyleplease/assets/main.scss :-). It's easy, if you are able to operate Hugo - you can do it.

# Link

{{< link "https://www.bing.com/" >}}Bing{{< /link >}}


```markdown
{< link "https://www.bing.com/" >}Bing{< /link >}
```

# <a name="top"></a>Table of Contents by Hand

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.

* [The start](#the-start)
* [hr](#hr)
* [Heading](#heading)
* [Paragraph](#paragraph)
* [List](#List)
* [Blockquote](#blockquote)
* [Thematic break](thematic-break)
* [Code](#Code)
* [Table](#table)
* [Image](#image)

# hr

***
---

# Heading

# Heading one

Sint sit cillum pariatur eiusmod nulla pariatur ipsum.

## Heading two

Sint sit cillum pariatur eiusmod nulla pariatur ipsum.

### Heading three

Sint sit cillum pariatur eiusmod nulla pariatur ipsum.

#### Heading four

Sint sit cillum pariatur eiusmod nulla pariatur ipsum.

##### Heading 5

###### Heading 6

# Paragraph

Incididunt ex adipisicing ea ullamco consectetur in voluptate proident fugiat tempor deserunt reprehenderit ullamco id dolore laborum.

Officia dolore laborum aute incididunt commodo nisi velit est est elit et dolore elit exercitation. Enim aliquip magna id ipsum aliquip consectetur ad nulla quis. Incididunt pariatur dolor consectetur cillum enim velit cupidatat laborum quis ex.

# List

## Ordered List

1. Longan
2. Lychee
3. Excepteur ad cupidatat do elit laborum amet cillum reprehenderit consequat quis.
    Deserunt officia esse aliquip consectetur duis ut labore laborum commodo aliquip aliquip velit pariatur dolore.
5. Melon
    - Cantaloupe
    - Honeydew
6. Miracle fruit

## Unordered List

- Olive
- Orange
    - Blood orange
    - Clementine
- Ut aute ipsum occaecat nisi culpa Lorem id occaecat cupidatat id id magna laboris ad duis. Fugiat cillum dolore veniam nostrud proident sint consectetur eiusmod irure adipisicing.

# Blockquote

The following is a blockquote:

> Suspendisse tempus dolor nec risus sodales posuere. Proin dui dui, mollis a consectetur molestie, lobortis vitae tellus.

# Thematic break

Mauris viverra dictum ultricies[^2]. **You can put some text inside the horizontal rule like so.**

---
{data-content = "with text"}

**Or you can just have an clean horizontal rule.**

---

# Code

## Highlighted

{{< highlight javascript >}}
const ultimateTruth = 'this theme is the best!';
console.log(ultimateTruth);
{{< / highlight >}}

```go
package main

import (
    "fmt"
    "net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hi there, I love %s!", r.URL.Path[1:])
}

func main() {
    http.HandleFunc("/", handler)
    http.ListenAndServe(":8080", nil)
}
```

## Inline code

And here is some `inline code`!

# Table

Table1

| Table Heading 1 | Table Heading 2 | Center align    | Right align     | Table Heading 5 |
| :-------------- | :-------------- | :-------------: | --------------: | :-------------- |
| Item 1          | Item 2          | Item 3          | Item 4          | Item 5          |
| Item 1          | Item 2          | Item 3          | Item 4          | Item 5          |

# Image

## simple image

![Super wide](/image/logo.png)

## image with caption

{{< figure 
    src="/image/logo.png"
    alt="alt-test"
    caption="caption-test"
    >}}

## image with link

[![Manny Pacquiao](/image/logo.png)](https://youtu.be/s6bCmZmy9aQ)

Logo of *no style, please!* theme[^3]

---
{data-content = "footnotes"}

[^1]: this is a footnote. It should highlight if you click on the corresponding superscript number.
[^2]: this is another footnote.
[^3]: this is a very very long footnote to test if a very very long footnote brings some problems or not. I strongly hope that there are no problems but you know sometimes problems arise from nowhere.

[Back to Top ↑](#top)