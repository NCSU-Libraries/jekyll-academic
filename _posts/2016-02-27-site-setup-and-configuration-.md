---
layout: post
title: (Almost) Everything You Want to Know About Your New Site
excerpt: "What goes where, and how to configure your new site "
modified: 22/29/2016, 7:33:12 
tags: [intro, intermediate, jekyll, tutorial]
comments: true
---

## Step 1: Getting Started
The first step in configuring your new site is to update the two main configuration files for the site. Both of these files are found in the root directory of the site (mysite folder). They are the **_config.yaml** and accent.scss files. The **_config.yaml** contains many of the main configuration settings for your site. It allows you to set a site name, and connect your site to many popular services and platforms such as Github, Twitter and email. The **accents.scss** file allows you to adjust the accent colors of your website (the two lines of color below the navigation). After adjusting these files be sure to safe the files and sync your changes back up to Github.

***

## Step 2: Navigation
The default site template includes navigation items for your home page (recent posts), About Me, Blog Archive and Resume pages. If you would like to add additional pages to the navigation of your site you can do so by creating a copy of the **about** folder and giving the name of the new page you would like. Once that is done, open _data/navigation.yaml and create a new navigation element that points to the folder you just created.

    Example:
    To create a 'Presentations' page
    1) Copy /about and rename to /presentations
    2) Open /_data/navigation.yaml
    3) Add the following lines:
       - title: Presentations
       url: /presentations/
    4) Save the file, sync changes to Github

***

## Step 3: Images

#### Bio Image
There are two main images to be aware of when setting up your new site. They are both included in the /Images/ directory. The first is bio-photo.jpg. This is the photo that appears on the left-hand side of your website. Any 200 x 200 pixel JPEG image can be used. Just be sure to rename the image bio-photo.jpg and place it in the /Images/ directory overwriting the default image that is in that folder.

#### Logo Image
By default the upper left-hand navigation item on your website will default to a text treatment of the name you have given your website. If you would like to use a logo instead of the text treatment simply include a 216 x 34 logo saved as logo.png in the /Images/ directory. Once you have saved your logo image to this directory open up your _config.yaml file and add logo.jpg in the site>logo: setting area.

***

## Posts: Step 4
Chances are you are were drawn to creating this site to use, at least partially, as a blogging platform. That is, after all, what it is designed for. In order to create a new blog post, you can simply copy an existing post from the _posts folder. At the top of the file you will see some settings options. Posts use the 'post' layout. You can set the title, excerpt and tags to whatever you would like. Set the timestamp to the current time (there are many text editor plugins that can do this for you). Save the new post with the same naming convention as the example posts -- e.g. 2016-01-03-New-Post.md. It is important that all posts are saved as Markdown (.md) files.

***

### Folder Structure

    mysite/

    Edit these files first:

    |── _config.yaml                 # main site configuration settings, edit this file **first**
    |── accents.scss                 # set site accent colors, edit this file **second**
    ├── about/                       # sample about page, edit this file **third**
    ├── images/                      # images for posts and pages, use this to set bio image and logo
    ├── index.md                     # sample homepage. lists 5 latest posts
    ├── _posts/                      # MarkDown formatted posts
    ├── _data/navigation.yaml        # Add items to site navigation bar

    These files likely do not need editing unless you plan on making major changes to your site:

    ├── _includes/
    |    ├── _author-bio.html        # bio stuff layout. pulls optional owner data from _config.yml
    |    ├── _browser-upgrade.html   # prompt to install a modern browser for < IE9
    |    ├── _disqus_comments.html   # Disqus comments script
    |    ├── _footer.html            # site footer
    |    ├── _head.html              # site head
    |    ├── _navigation.html        # site top navigation
    |    ├── _open-graph.html        # Twitter Cards and Open Graph meta data
    |    └── _scripts.html           # site scripts
    ├── _layouts/
    |    ├── home.html               # homepage layout
    |    ├── page.html               # page layout
    |    ├── post-index.html         # post index layout
    |    └── post.html               # single post layout
    ├── posts/                       # sample post index page. lists all posts in reverse chronology
    ├── _sass/                       # Sass stylesheets
    ├── _templates/                  # used by Octopress to define YAML variables for new posts/pages
    ├── assets/
    |    ├── css/                    # compiled stylesheets
    |    ├── fonts/                  # webfonts
    |    ├── js/
    |    |   ├── _main.js            # main JavaScript file, plugin settings, etc
    |    |   ├── plugins/            # scripts and jQuery plugins to combine with _main.js
    |    |   ├── scripts.min.js      # concatenated and minified _main.js + plugin scripts
    |    |   └── vendor/             # vendor scripts to leave alone and load as is
    |    └── less/
    ├── 404.md                       # 404 page

***

## Further Customization
If you dig deep enough into the site structure you will find that nearly every element of your site can be customized. This them is based on the wonderful Minimal Mistakes theme by Michael Rose. If you would like more detailed information about the site setup and structure, please visit the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/theme-setup/) theme setup page. Here you will find detailed instructions for nearly every use case.

***

## License

Figure out the best license for us.
