# INSTALLATION

Cloned from [mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes).

***

## DEPENDENCIES

Intall Ruby and Gem:

- [Ruby](https://www.ruby-lang.org/en/downloads/) version 2.5.0 or higher, including all development headers (check your Ruby version using `ruby -v`).
- [RubyGems](https://rubygems.org/pages/download) (check your Gems version using `gem -v`).

We use Jekyll and it's built-in SCSS compiler for the associated CSS, so the first thing you'll need is Jekyll itself, so follow these steps:

```bash
gem install jekyll bundler # This is going to install Jekyll and Bundler
jekyll -v # To make sure it is instaled correctly

# navigate to the project's folder
bundle install # This is going to install all gem dependencies

# if you are using windows, run:
# To correct a problem with the "--livereload" option
gem uninstall eventmachine
gem install eventmachine --platform ruby
```

***

## USAGE

Once you have the required gems from [dependencies](#dependencies), you can go ahead and clone [our repository](https://github.com/devopschefs/blog).

To run the website locally:

```bash
bundle exec jekyll serve --livereload
```

Jekyll should now be generating our content! If you need more help see the Jekyll page [here](https://jekyllrb.com/docs/).

***

## ADDING POSTS

- Create a .markdown file inside `_posts` folder.
- Name the file according to the format YY-MM-DD-[short name for your post].
  - `2016-03-30-i-love-design.md`
- Write the *Front Matter* and content in the file, following the example:

```markdown
---
title: "Post Example" # name on UI
excerpt: "Excerpt post example" # Unique excerpt descriptions for each post for improved SEO and archive listings.
toc: true # Table of contents (https://mmistakes.github.io/minimal-mistakes/docs/layouts/#table-of-contents) - Can be "false" if you don't need one
toc_sticky: true # To enable the TOC to go down as you read the post - If "toc: false" you don't need this
toc_label: Content # Keep, for consistency across posts - If "toc: false" you don't need this
last_modified_at: 2020-11-24
author: # Alex Giannotti | Max Fernandes
header:
  overlay_image: "/assets/images/posts_header/examplepost.jpg"
  overlay_filter: 0.5 # Can also be an RGB color
  teaser:  "/assets/images/posts_header/examplepost.jpg" # Image for tumbnail - Should be the same as the "overlay_image"
show_overlay_excerpt: true # Show excerpt over main image
categories:
  - example # devops | cloud | iac | more # Choose only one category
tags: # subjects your post covers beyond the categories
  - processos
  - azure
  - modelo

# OPTIONALS
# caption: "Photo credit: [**Unsplash**](https://unsplash.com)" # Header image credits
# actions: # Use if you need to provide something for the reader to download
# - label: "Download"
#     url: "https://github.com"
---
```

***

## IMAGES

To place new images in the repository, please mind the folders bellow.

```markdown
├── assets                        # => Main folder for the projects assets
│   └── images                    # => Folder to hold all images used in **PAGES**
|       └── authors               # => Only for author's pictures
│       └── favicon               # => For the project's icons
│       └── other_images          # => All images that aren't being used in the project, but are worth saving
│       └── posts_header          # => All images used in **POSTS** headers
│       └── posts_images          # => All images used in **POSTS** bodies
```

***

## CREATE PAGES

- Create a `<example>.md` file in the `/docs/_pages` directory.
- Write the *Front Matter* and content in the file, following the example:

```markdown
---
permalink: /comment-policy/ # folder path
title: Comment Policy # name on UI
#excerpt: "Excerpt example." # Best if pages don't have it
last_modified_at: 2020-11-24
header:
  overlay_image: "/assets/images/<image_name>"
  overlay_filter: 0.50

---
```

- Pages should always have (added as global settings in `_config.yml`):
  - `sitemap: true` so they can be searched at the sitemap feature.
  - `classes: wide` so they fill the whole page without a content sidebar.

***

## ARCHIVE PAGES

You can display a list of all the posts corresponding to a particular category on a standalone page using the `ARCHIVE` layout.

- Create a .md file in the `_pages` directory.
- Name the file with the category name.
    `\_pages\devops.md`
- Write the *Front Matter* and content in the file.

### FORMAT

```markdown
---
permalink: /devops/
title: "DevOps"
layout: collection
collection: devops
entries_layout: grid
classes: wide

---
```

***

## ABOUT

To create your contact badge from LinkedIn follow these steps:

- From your profile, click on See contact info.
- Click on the pencil to edit.
- Click on the arrow next to your LinkedIn Profile URL.
- Scroll and click on the create the public profile badge button.
- Copy the code in step one and paste it in the HTML about page.
- Choose a badge, copy that code and paste it below the first line of code.

***
