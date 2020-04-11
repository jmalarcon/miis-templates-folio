---
title: Powerful things you can do with the Markdown editor
subtitle: This is a simple sample post
#I've defined a general author name in the folder's web.config. This overwrites it:
author: Jane Doe
#You can omit this and the creation date will be used
date: 2020-04-10 08:00
#These will be used for the social headers
image: https://images.unsplash.com/photo-1528784351875-d797d86873a1?ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80
excerpt: There are lots of powerful things you can do with the Markdown editor. If you've gotten pretty comfortable with writing in Markdown, then you may enjoy some more advanced tips about the types of things you can do with Markdown!
---

There are lots of powerful things you can do with the Markdown editor. If you've gotten pretty comfortable with writing in Markdown, then you may enjoy some more advanced tips about the types of things you can do with Markdown!

As with the last post about the editor, you'll want to be actually editing this post as you read it so that you can see all the Markdown code we're using.

## Special formatting

As well as bold and italics, you can also use some other special formatting in Markdown when the need arises, for example:

+ ~~strike through~~
+ ==highlight==
+ \*escaped characters\*

## Writing code blocks

There are two types of code elements which can be inserted in Markdown, the first is inline, and the other is block. Inline code is formatted by wrapping any word or words in back-ticks, `like this`. Larger snippets of code can be displayed across multiple lines using triple back ticks:

```css
.my-link {
    text-decoration: underline;
}
```

## Reference lists

The quick brown jumped over the lazy.

Another way to insert links in markdown is using reference lists. You might want to use this style of linking to cite reference material in a Wikipedia-style. All of the links are listed at the end of the document, so you can maintain full separation between content and its source or reference.

## Video

With MIIS you can embed a video (YouTube, Vimeo) just like an image in Markdown. It'll have the `.youtube` or `.vimeo` class applied in the `<iframe>`:

![](https://vimeo.com/400522741)

But you can use MIIS's special YouTube tag to make it 16:9 full-width and the "no cookies" version of the video in YouTube (no cookies until the visitor plays the video):

{% youtube Cniqsc9QfDo %}
