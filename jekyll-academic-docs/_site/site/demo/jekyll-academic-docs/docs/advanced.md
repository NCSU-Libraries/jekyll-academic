# Advanced Features
The quickstart guide was intended to provide you with the easiest possible setup of Jekyll Academic. The integration with GitHub Pages allows you to fully set up Jekyll Academic without ever installing Jekyll locally. However, many users may wish to make advanced modifications to their site. If you wish to do so, you would benefit from installing Jekyll locally. The following instructions are based on using Mac OSX as your operating system.

## Setting Up Jekyll Locally
GitHub Pages has been designed to work with Jekyll allowing you to upload your 'raw' site files and have GitHub interpret them and create your site. This works well for any user that wants to use GitHub Pages. However, there are additional features that can be utilized if you wish to install Jekyll locally. Local installation allows you to preview the changes made to your site without committing them to GitHub. It also allows you to create new posts from the command line.

To set up Jekyll locally you will need to install the following three things:

* [Ruby](https://www.ruby-lang.org/en/downloads/)
* [RubyGems](https://rubygems.org/pages/download)
* [Jekyll](https://jekyllrb.com/docs/installation/)

### Installing Ruby
Probably the easiest way to install Ruby on a Mac is using [Homebrew](http://brew.sh/). Once you have Homebrew installed you can install ruby using the command `brew install ruby`. If you are using another operating system, or wish to have a more advanced ruby setup, you may find the instructions listed [here](https://www.ruby-lang.org/en/documentation/installation/) useful. After installing ruby on your system you will need to install **RubyGems** this can be completed by following the instructions on the [RubyGems](https://rubygems.org/pages/download) website.
### Installing Jekyll
Jekyll can be installed using RubyGems once you have ruby and RubyGems installed you can install Jekyll using the command `gem install jekyll`.

## Using Jekyll Locally
Jekyll is an incredibly powerful tool. It also has a ton of great documentation written about it already that can be found at the [Jekyll](https://jekyllrb.com/) website. We highly recommend you take a look at that site to get a better idea of the advanced features that are available. Two of the most common Jekyll commands are described below.

* **Jekyll Serve** - The primary advantage of installing Jekyll locally is that it allows you to make updates to your site and preview those changes before pushing them to GitHub. In order to view changes that you are making to your site in a preview development server run `jekyll serve` from your project directory and then navigate to http://localhost:4000/.

* **Jekyll Build** - If you wish to host your website somewhere other than GitHub Pages it will require that you create a site folder containing valid HTML and CSS files. You can do this by running `jekyll build` from the root folder of your project directory. That will result in the creation of a \_site folder. That folder can then be uploaded to the webhost of your choosing.


## Adding Navigation Items
You may want to add additional navigation items that point to different types of content or individual pages. This can be accomplished by adding a new navigation item. In order to add a new navigation item you will:

1) Copy the folder of an existing navigation item (e.g resume) and paste it into the root directory of your project. Rename this folder with the name of the new navigation item.

2) Navigate to \_data/navigation.yml and add a new navigation item by copying the layout of an existing navigation item.

3) Take a look at some of the existing index.md files for other navigation items. Take note of the 'layout' element declared in the frontmatter. This will help you determine which layout is appropriate for your newly created page (e.g. Page or Resume)


## Understanding Layouts
One of the fundamental elements of Jekyll is the ability to utilize different layouts for different types of pages. The layouts are found in the \_layouts folder. These are .html files that drive the layout of any particular page. For example the 'slide' layout contains all of the necessary includes to power reveal.js slides. The current available layouts in Jekyll Academic are:

* **home** - This layout is the layout for the homepage of your website. It automatically includes your 5 most recent blog posts in the space to the right of the social media section.
* **page** -  This layout is used for any individual page, like the 'About Me' page. It is a blank page that can be formatted using Markdown.
* **post-index** -  This layout is used on the blog archive. It lists every blog post chronologically separated by year.
* **post** - This layout is used for blog posts. It includes a few more functionality elements than the 'page' layout.
* **resume** -  This layout is used for the Resume page.
* **presentation-post-index** - This layout is identical to the post-index layout except it is used on the presentations index to post all presentations you have on your site in one location, chronologically.
* **slide** -  This layout is used for creating a reveal.js slide deck.
