---
title: 📄 Template documentation
#You can omit this and the creation date will be used
date: 2020-04-11 08:00
excerpt: This document describes the different layouts and parameters in this template and how to use them.
---

This [MIIS](https://miis.azurewebsites.net/) template is based on the [*-folio template](https://github.com/bogoli/-folio) for Jekyll, by [Lia Bogoev](https://github.com/bogoli).

I've added several enhancements to the original template, such as treatment of the images for the projects section, zooom & pan & rotation of images, syntax highlighting of code, social headers, better mobile support, separated SCSS variables...

> :warning: **Important**: This is a sample site with MIIS that is usefull to see the template in action. However the only thing you need to make it work for you is the `-folio` folder. The `bin` folder for the MIIS binaries and the `_shared` folder inside the `templates` folder, **should be get from the latest release of MIIS**, and it's highly recommended that you use the ones there, since the ones in this folder could not be updated to the last version.

## Layouts

### base.html

This is the base layout for the rest of them. You won't normally use this one.

### page.html

The default layout for all the pages.

### postlist.html

This layout is used exclusively to list the available posts in a folder. It need a `paginator` field (in the Front-Matter or global) with the pagination information for the posts you want to list. This can be achieved with the `PaginatorForFolder` Front-Matter Source included in MIIS:

```yml
paginator: !!PaginatorForFolder ./
```

You can have more than one folder with articles and use this layout in the `index.md` or `index.mdh` page for the folders. See the `blog` folder in this sample repository.

### portfolio.html

This is similar to the previous one but generates a tiled list with the files in the folder, showing an image in the background, a title and a subtitle. It's not paginated and needs a `projects` field, that you must get with the `FilesFromFolder` FM source:

```yml
Projects: !!FilesFromFolder ./
```

See the `projects` sample folder.

## Parameters

Apart form the default parameters, this template has several specific parameters that you can use to customize it's behavior:

- **`nav`**: points to a `.md` file with the top bar navigation links. They should be very few and short because that menu is only for small sites and doesn't convert itself to an hamburger menu on mobile. The links can't be lists: just one after (or above) the other. Check the `nav.md` sample file, defined in the root's `web.config` file.
- **`LogoText`**: the text to use in the top-left logo part of the top bar. Can include emojis.
- **`SiteTitle`**: the global title for the site. It's used in the pages' titles.
- **`Copyright`**: the text to show on the footer of the page. Can include HTML code if you encode it as HTML entities (VSCode or Notepad++ allow to do that). See the `web.config` file.
- **`Subtitle`**: if specified it will show its contents under the title of the current page.
- **`ShowMeta`**: if `true` it will show meta-information (date and time and author) under the current page's title. By default it's `false` and it's only enabled on blog posts.
- **`Author`**: the name of the author of the current page.
- **`imgsize`**: in a project file, indicates how to show the main image (`image`) inside the project list tiles. It can have the following values:
  - **`cover`**: the default value. Covers all the available space in the thumbnail. Useful with photos.
  - **`contain`**: fills the thumbnail, but maybe leaves some background areas visible.
  - **`auto`**: uses the image's original size.
- **`redirect`**: a URL to redirect when clicking the tile in the list of projects. If practice, the project file will never be reached from the project list. Useful to send to an external URL for an specific project.
- **`ga-id`**: the Google Analytics ID. If set, the template will include the GA code to track visits.
- **`robots`**: if specified it will add a robots meta-tag to the page. Usefull to prevent some pages to be indexed, using `robots: noindex,nofollow` in the FM.

You can also show contact icons below any page by setting the following self-explanatory parameters:

- **`email`**
- **`GithubId`**
- **`LinkedinID`**
- **`YoutubeId`**
- **`TwitterId`**
- **`ContactCaption`**: an optional text to be shown under the contact icon area.

## Color customization

This template has a main color that is the predominant one in the site. This color is defined in the `_variables.scss` file in the template. You can change it by changing the `$theme-color` variable value in that file. You can set your own color or use one of he many already defined there.

Once you change the main them color you should recompile the SCSS files into a new `main.css` file by opening your command line and writing:

```bash
npm run build:css
```

Obviously, you'll need Node.js installed in your computer.
