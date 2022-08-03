---
title: "On Hugo Site Maintenance"
date: 2022-07-27T21:34:27+01:00
draft: true
---

As much as I LOVE hugo for their fast and lightweight static site generation, their documentation sucks. And I don't think I'm the minority here. It took me ages to figure out their basic site structure and the dependencies among files even longer. And I am still confused every now and then, especially when returning to it after a while that I haven't used it.

Given my lack of front-end experience, it could be just me. So I am going to write this hugo site maintenance guide for myself as a reference to prevent the next episode of opening up 20+ tabs to look up a simple feature - but I'd be even happier if you also find this piece helpful.

## Hugo site structure

- *archetypes*: holds a default.md file, the template for new md documents when we do `hugo new [doc name]`.
- *assets*: 
  - can be used to hold a css folder with custom and override css files
    - I might have done something wrong here, but I never successfully overrode anything in these files  
  - can also hold all sorts of media files, like the `static` folder.
- *static*: 
  - holds media files.
  - However, when I render the page, all the files will appear directly in the `public` folder - that is, the root directory of the website.
- *content*: where all the pages and posts should go.
  - `posts` is the default folder that holds all our blog files (single pages)
  - We can use page bundles to create new pages like the "posts" entry page. For instance, I created `newsletter`, and `projects`, along with the other default page bundles.
  - I also created `images` and `files` folders to hold the media files in a more structured manner.
- *data*:
  - Mine is left empty
- *docs*: 
- *layouts*:
  - On the creation of the `newsletter` folder in the theme under `layouts`, a `newsletter` directory also appeared here, but empty.
- *themes*: holds the theme directories.
  - I am making direct modifications based on the FeelIt theme, which is not the best practice but so much easier.
- *resources*:
- *public*: updates everytime we make modifications to the contents/themes/configurations and run `hugo` (or when we are using a server with `hugo server`).
- *config.toml*: Configuration file that contains all the parameters that hugo renderer and template needs. For instance, attributes under the tag `[params.footer]` can be accessed with 

## Hugo themes and templating

- Choosing a theme: 

## FAQ

1. Deployed site not refreshing following a new push?
   - Very likely the browser has cached the previous version. Hard refresh by `ctrl` + `F5`.
2. Drafts showing in deployed hugo site?
   - If you don't clear the previously deployed files, they will not go away. Build with the flag instead
      ```
      hugo --cleanDestinationDir
      ```