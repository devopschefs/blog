# INSTALLATION

Cloned from [hemangsk/Gravity](http://github.com/hemangsk/Gravity/).

***

## DEPENDENCIES

Intall Ruby and Gem:

- [Ruby](https://www.ruby-lang.org/en/downloads/) version 2.5.0 or higher, including all development headers (check your Ruby version using ```ruby -v```).
- [RubyGems](https://rubygems.org/pages/download) (check your Gems version using ```gem -v```).

Gravity uses Jekyll and it's built-in SCSS compiler for the associated CSS, so the first thing you'll need is Jekyll itself:

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

Once you have the required gems, you can go ahead and clone the
[Gravity repository](https://github.com/hemangsk/Gravity) or [download](https://github.com/hemangsk/Gravity/archive/master.zip)
a zip of the master branch.

Run :

```bash
bundle exec jekyll serve --livereload
```

Jekyll should now be generating your content!

If you need more help see the Jekyll page [here](https://jekyllrb.com/docs/).

***

## ADDING POSTS

- Create a .markdown file inside `_posts` folder.
- Name the file according to the format YY-MM-DD-[short name for your post].
  - `2016-03-30-i-love-design.md`
- Write the *Front Matter* and content in the file, following the example:

```markdown
---
title: "Post Example"
excerpt: "Excerpt post example."
toc_label: TOC Label example # Table of contents label
header:
  overlay_image: "/assets/images/<image_name>"
  overlay_filter: 0.5 # Can also be an RGB color
show_overlay_excerpt: true
categories:
  - categories-example
tags:
  - tags-example

# OPTIONALS
# caption: "Photo credit: [**Unsplash**](https://unsplash.com)" # Header image credits
# actions: # Use if you need to provide something for the reader to download
# - label: "Download"
#     url: "https://github.com"
---
```

***

## CREATE PAGES

- Create a `<example>.md` file in the `/docs/_pages` directory.
- Write the *Front Matter* and content in the file, following the example:

```markdown
---
permalink: /comment-policy/
title: Comment Policy
#excerpt: "Comment policy."
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

## ABOUT

To create your contact badge from LinkedIn follow these steps:

- From your profile, click on See contact info.
- Click on the pencil to edit.
- Click on the arrow next to your LinkedIn Profile URL.
- Scroll and click on the create the public profile badge button.
- Copy the code in step one and paste it in the HTML about page.
- Choose a badge, copy that code and paste it below the first line of code.

## ARCHIVE PAGES

**You can display a list of all the posts corresponding to a particular category on a standalone page using the `ARCHIVE` layout**

- Create a .md file in the root directory.
- Name the file. Preferred name will be the name of the category.
    \*`life.md`
- Write the *Front Matter* and content in the file.

### FORMAT

```markdown
---
layout: archive ARCHIVE PAGE LAYOUT
title: String TITLE OF THE WEBPAGE
permalink: / String / PERMALINK FOR THE WEBPAGE
tagline: String TAGLINE FOR THE PAGE
category: String NAME OF THE CATEGORY OF WHICH THE PAGE WILL SHOW POSTS
---

---
layout: archive
title: "Design"
permalink: "Design"
tagline: "It's all about perception"
category: "design"
---
```

***

## DIRECTORY STRUCTURE

```markdown
├── css                                         # => Output of the combined SASS files
│   └── style.scss
├── _includes                                   # => Contains partials that can be used with your layouts
│   ├── footer.html
│   ├── header.html
│   ├── head.html
│   ├── icon-github.html
│   ├── icon-github.svg
│   ├── icon-twitter.html
│   └── icon-twitter.svg
├── _layouts                                    # => Layout related HTML files
│   ├── archive.html
│   ├── default.html
│   ├── page.html
│   └── post.html
├── _posts                                      # => posts, dynamic content. Follow the format: YEAR-MONTH-DAY-title.MARKUP
│   ├── 2016-03-30-design-stories.markdown
│   ├── 2016-03-30-science0.markdown
│   ├── 2016-03-30-science.markdown
│   └── 2016-03-30-welcome-to-jekyll.markdown
└── _sass                                       # => SASS partials for styling
|   ├── _base.scss
|   ├── _layout.scss
|   └── _syntax-highlighting.scss
├── about.md
├── _config.yml                                 # => Configuration options or flags for your site go here
├── design.md
├── download.md
├── feed.xml
├── index.html
├── LICENSE.txt                                 # => Licensing information
├── README.md
└── science.md
```
