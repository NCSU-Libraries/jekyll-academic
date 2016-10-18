# Getting Started with Jekyll Academic

## Required Software
In order to edit your Jekyll Academic website you will need the following pieces of software:

1) A text editor. Any text editor will do, our favorite is [Atom](https://atom.io/)

2) [GitHub Desktop](https://desktop.github.com/). This is used to sync files between your local computer and the GitHub repository that is acting as your website host.


## Quickstart Guide
This quickstart guide is geared to getting you up and running quickly. Following the directions below will result in you having a Jekyll Academic website hosted on GitHub pages live on the web. Before you begin working through the quickstart guide you may want to familiarize yourself with the following technologies that will be used to create your Jekyll Academic website:

* [Jekyll](https://jekyllrb.com/)
* [Markdown](https://daringfireball.net/projects/Markdown/)
* [GitHub](https://github.com/)
* [GitHub Pages](https://pages.github.com/)
****

#### 1) Register for a GitHub Account
*Skip this step if you have already setup your GitHub account*

* In a web browser, navigate to GitHub.com
* Fill Out Username, Email Address and Password
* Click Sign up for GitHub button
* Click the Finish Sign Up button
* Navigate to the email account you used to sign up
* Verify your email address by clicking on the “Verify email address” button in the email you received from GitHub
#### 2) Setting Up your Jekyll Academic Repository:
* After signing in to GitHub click on New Repository
* Give your repository the following name [username].github.io (username is the username of your account)
* Click on Create Repository
* Click on Import Code
* Paste the following URL in the “Your old repository’s clone URL - https://github.com/NCSU-Libraries/jekyll-academic
* Click on Begin Import
* Once import is complete navigate to [username.github.io] in your web browser

#### 3) Connect your GitHub Repository to GitHub Desktop
* Download GitHub Desktop from https://desktop.github.com/ (skip this step if you already have GitHub Desktop installed)
* Double-click on downloaded file to begin the installation
* While on the Welcome screen click on Continue
* Sign in using the username you created in step one of this activity
* Click Sign In
* Click Continue
* Click Continue one more time
* Click on the plus sign in the upper left-hand corner of the screen to add a repository to Github Desktop
* Click Clone
* Find the ‘[username].github.io’ repository you created earlier and click Clone Repository
* Select the location where you would like to save the repository (e.g. Documents)
* Once the clone is finished you can click on the name of the repository on the left-hand side of Github Desktop to see any uncommitted changes (there shouldn’t be any yet)

#### 4) Update Website \_config.yml File and Sync Changes
* See your live Website by opening your web browser and going to [username].github.io
* Open \_config.yml using Atom
* Edit the following entries of the \_config.yml file
  * Title
  * Name
  * Bio
  * Email
  * Twitter
  * Facebook
  * GitHub
* Save the \_config.yml file
* Commit Changes to GitHub Repo
* Open GitHub Desktop
* Click to see Uncommitted Changes (at the top center portion of the screen)
* Add commit message to the summary field that says what changes you made
* Click Commit to Master
* Click Sync
* Refresh the browser window with your website and note the changes


## Important Files and Folders
In order to better understand how everything in your site works, there are a few files and folders that you need to be aware of. These files control the main elements of your site, including your logo, bio photo and navigation. Full documentation of the directory structure can be found [here](https://jekyllrb.com/docs/structure/). 

* **\_config.yml** - This is your websites main configuration file. It allows you to set a site title, links to your social media accounts as well as a logo and bio photo image.

* **accent.scss** - This file is used to set the colors of your site. The site is set up to accept two colors (highlight, lowlight). The main impact of the color choice  

* **\_posts** - This folder holds all of the posts for your website. It includes both blog posts as well as presentation posts. There are two sample posts in this directory to get your started. One for a blog post and one for a presentation post.

* **images/bio-photo.jpg** - This is the photo that appears on the home page of the website. The recommended image size is 200px x 200px.

* **images/logo.png** - If you wish to use a logo for your site, include logo.png in the images folder. You will also need to add logo.png under the 'Logo:' section of the \_config.yml file.

* **\_data/navigation.yml** -This is the file that allows you to manage your navigation elements. By default all available navigation items are shown. If you wish to hide any items, simply delete them from this file.

## Adding Blog posts
To add a new blog post to your site you simply create a new Markdown file. Jekyll requires that you follow the yyyy-mm-dd-title.md naming convention. Once you have the blank Markdown file you will need to add the header information so that Jekyll knows it is a blog file. Add the following to the top of your Markdown file:
      ---
      layout: post
      title: Add Your Title Here
      excerpt: "Add an excerpt here, the excerpt will appear underneath the blog title"
      modified: 2016-01-13 20:41:38
      tags: [intro, beginner, jekyll, tutorial]
      comments: true
      category: blog
      ---
      # Start your content here
The important thing to note is that you need to make sure that the category is set to 'blog'. This ensures that this post will appear on the blog page. You can then add your blog content using Markdown as your markup language for the rest of the file.

## Adding Presentations
In Jekyll Academic presentations are actually set up as posts, just with a few different settings in the header. This means that your presentation files live in the same \_posts folder as your blog posts. The only differences between presentations and posts is the layout and category section in the header.

#### Adding Reveal.js Presentations
To add a Reveal.js presentation to your site you first will need to create a new Markdown file in your \_posts folder. At the top of your new file you will want to add the following header. Notice that you need to set the layout to 'slide' and the category to 'presentation'

      ---
      layout: slide
      title: Add Your Title Here
      excerpt: "Add an excerpt here, the excerpt will appear underneath the blog title"
      modified: 2016-01-13 20:41:38
      tags: [intro, beginner, jekyll, tutorial]
      comments: true
      category: presentation
      ---
      <section data-markdown>
      # Add reveal.js slide content here, following the reveal.js format
      </section>

#### Linking to External Presentations
To add a presentation post that appears on the presentation page, but is not a reveal.js slide deck you follow similar instructions as above. You will create a new Markdown file in your \_posts folder and add the following header to it. Notice that you keep 'post' as the layout and 'presentation' as the category. This will create a blog post style post where you can link to external presentations.

      ---
      layout: post
      title: Add Your Title Here
      excerpt: "Add an excerpt here, the excerpt will appear underneath the blog title"
      modified: 2016-01-13 20:41:38
      tags: [intro, beginner, jekyll, tutorial]
      comments: true
      category: presentation
      ---
