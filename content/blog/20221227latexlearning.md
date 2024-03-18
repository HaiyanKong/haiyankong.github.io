---
title: "My LaTex Learning Note"
date: 2022-12-27
author: Haiyan Kong
slug: 20221227/latexlearning
draft: false
tags: latex
---

# Basic Grammar

## Front style

```latex
\\textbf{bold}
\\underline{underline}

\\usepackage{ulem}
\\uuline{doubleunderline}
\\sout{deleteline1}
\\xout{deleteline2}
\\uwave{waveline}
```

## Split

`\\noindent\\hfil$*$\\hfil$*$\\hfil$*$\\hfil$*$\\hfil$*$\\hfil$*$\\hfil$*$\\hfil`

`\\rule[10pt]{7.5cm}{0.05em}`

## Spcae

### Regular Space

In text, use two consecutive spaces or `\ ` to insert a regular space.
Example: This is a regular\ space.

### Specified Length Space

Use `\hspace{length}` command to insert a space of specified length.
Example: `\hspace{1cm}` will insert a space of 1 centimeter in length.

### Flexible Space

Use `\hfill` to insert a flexible space within a line, ensuring even distribution of text.
Example: Left\hfill Right will insert a flexible space between "Left" and "Right".

### Non-Breakable Space

Use the `~` symbol to insert a non-breakable space that won't be separated at line breaks.
Example: This is a non-breakable~space.

### Inserting Multiple Spaces

If you need to insert multiple consecutive spaces, you can repeat `\ ` or use the `\hspace{length}` command.
Example: This is\ \ \ \ multiple consecutive spaces. Or `\hspace{2cm}`.



# To do list

[LaTeX - Kuroko](https://kuroko.info/category/latex/)

[Tips for LaTeX3 Beginners](https://blog.fkynjyq.com/tips-for-latex3-beginners)

{{< badge "edit" >}}
Update: 18 March 2024
{{< /badge >}}