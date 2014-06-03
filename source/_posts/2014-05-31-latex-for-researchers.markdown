---
layout: post
title: "LaTeX for Researchers, Part 3: Figures and Tables"
date: 2014-05-31 09:53:02 -0700
comments: true
categories: 
---

If you're just joining us, it's probably best to start out with my first two
posts:

* [Setting Up](http://www.schuetzler.net/blog/latex-for-researchers-pt-1/)
* [Citations](http://www.schuetzler.net/blog/latex-for-researchers-pt-2/)

Now that we've covered how to do create a document and how to add citations, the
next major items we need to be able to put in a research manuscript are tables
and figures. First we'll talk about differences between LaTeX and Word in how
they handle tables and figures. Then we'll dig into how to make each of them
work.

## Floats in LaTeX

When you have a desire to put a figure or table into a Word document, you throw
it in. Then you keep working on the document, and all of a sudden you have a
figure on a page by itself with a half-empty page before it. Or even better, the
formatting of the document is completely screwed up, and you've got text going
all over the place (these are all personal experiences). And heaven forbid you
want to change a picture, or remove the table. Odds are that will break
everything forever.

LaTeX handles things a bit differently. There are several ways to handle tables
and figures, but the most commonly used is to place them in a "float"
environment. This gives LaTeX the freedom to place them in the place it thinks
is best to make your document look as clean as possible. No pain of half-empty
pages, and no broken formatting. And the best part is that it places them
automatically each time you compile the document. So if you add a paragraph of
text above a figure, LaTeX will figure out how that affects the placement to
make it look nice.

## Figures in LaTeX

Hopefully that description helps you understand what LaTeX is doing when you
tell it to place an image into your file. Now we'll cover how to place an image,
and some of the settings you can tweak to make it look nice.

The first thing to note is that, since LaTeX documents are stored in text, you
are obviously not going to embed the image in the file. 
