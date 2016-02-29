---
layout: post
title: How to edit your Jekyll site and make posts
excerpt: "Edit your site and make posts "
modified: 2/29/2016, 8:24:22
tags: [intro, beginner, jekyll, tutorial]
comments: true
---

This article will cover the basics on how to edit the features of your site and make new posts. To do this, you will need a text editor. Here are some examples:
* [Atom](https://atom.io)
* [Sublime Text](https://www.sublimetext.com)
* [Notepad++](https://notepad-plus-plus.org)

## Editing the configuration of your Jekyll site
The _config.yml file stores data about you and your site, such as your contact information and your site's title and URL. You will want to edit your _config.yaml file to contain your information. The information in this file sets the site title, contact email address and links to various social media accounts that you may have. To add a social media account, simple replace #username with your actual username for that service on the line next to the service.


<pre><code>
# Site wide configuration

title:            Your Site Title
locale:           en_US
url:

. . .

# Site owner
owner:
  name: Your Name
  avatar: bio-photo.jpg
  bio: "Hi I am a librarian."
  email: youremail@emailaddress.com
  disqus-shortname:
  twitter: #username
  facebook: #username
  google:
    plus: #username

</code></pre>

You can edit this file by opening it in a text editor, editing the information, and then saving it into the repository folder, replacing the older version of the file. You will then need to commit the changes to your Github repository so that the changes will show up on your Jekyll site. For more information on how to manage files and commit them to your Github repository, see this getting started [guide](http://guides.github.com/introduction/getting-your-project-on-github).


## Adding posts
Each post is its own file saved in the _posts folder. All you have to do to add a new post is to create a file and drop it into the _posts folder, and sync that to your github repository. However, you have to format the title of the post with the date included in the title at the beginning. The file is saved as a .md file because it is written in [markdown](http://daringfireball.net/projects/markdown/). Here's an example:

<pre><code>
2011-12-31-new-years-eve-is-awesome.md
</code></pre>


## Formatting posts

Each post must have a header that tells Jekyll how to display it, along with some supporting data about the post, like tags and date modified. The header looks like this:

  <pre><code>
    ---
    layout: post
    title: Your Title
    excerpt: "Edit your site and make posts "
    modified: 2016-02-15 11:00:29
    tags: [intro, beginner, jekyll, tutorial]
    comments: true
  ---
  </code></pre>

Make sure to use the three dashes at the top and bottom of the header. Then you can write your post below the dashes.

## Editing accent colors on your page

The accent.scss file is the place where you can edit the accent bar top and bottom colors on your site. The default colors are indicated by hex code #CC0000. Change the hex codes next to $highlightcolor and $lowlightcolor to your desired colors. For more hex codes, see [here](http://www.w3schools.com/colors/colors_picker.asp).

<pre><code>
$highlightcolor : #CC0000;
$lowlightcolor  : #000000;
</code></pre>


## Adding a photo to your site
In the _config.yml file, you can add a photo that will be featured on the home page. To update your bio picture you can create a 200px x 200px image and place it in the images folder. In the site owner section, change "bio-photo.jpg" to the name of the picture you placed in the images folder.

<pre><code>
# Site owner
owner:
  name: Todd Stoffer
  avatar: bio-photo.jpg
</code></pre>
