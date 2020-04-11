---
title: Sample Project
subtitle: This project shows you a few tips and tricks to use images and other elements
description: This has the default background image size (cover)
date: 2020-04-10 08:00
author: José Alarcón
image: images/bm-001.jpg
---

Every project has a beautiful feature showcase page. It's easy to include images, in a flexible 3-column grid format. Make your photos 1/3, 2/3, or full width.

## Front-Matter

To give your project a background in the portfolio page, just add the `image` field to the front-matter like so:

```yml
---
layout: post
title: Project
description: This has the background image as "auto"
image: /images/bm-001.jpg
#The size of the image
imgsize: auto
# Valid values:
# cover (default): covers all the available space in the thumbnail. Useful with photos
# contain: fills the thumbnail but leaves some background areas visible
# auto: uses the image's original size
---
```

{.img_row}
![Image 01](images/bm-001.jpg){.col .one}
![Image 01](images/bm-002.jpg){.col .one}
![Image 01](images/bm-003.jpg){.col .one}

Caption photos easily. On the left, Bill Murray in the Ghostbusters. Middle, a close-up shoot of Bill Murray. Right, BM in th Groundhog day film. {.col .three .caption}

{.img_row}
![Image 01](images/bm-002.jpg){.col .three}

This image can also have a caption. It's like magic. {.col .three .caption}

You can also put regular text between your rows of images. Say you wanted to write a little bit about your project before you posted the rest of the images. You describe how you toiled, sweated, *bled* for your project, and then.... you reveal it's glory in the next row of images.

{.img_row}
![Image 01](images/bm-002.jpg){.col .two}
![Image 01](images/bm-003.jpg){.col .one}

You can also have artistically styled 2/3 + 1/3 images, like these. {.col .three .caption}

The code is simple. Just add a `{.col}` to your image, and another class specifying the width: `.one`, `.two`, or `.three` columns wide. Here's the code for the last row of images above:

```markdown
{.img_row}
![Image 01](images/bm-002.jpg){.col .two}
![Image 01](images/bm-003.jpg){.col .one}
```
