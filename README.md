##Introduction
This template utilizes Jekyll, an open source static website generator, as well as a theme based largely off of the Minimal Mistakes theme by Michael Rose. The purpose of this template is to provide you with a simple, well designed website that is optimized for hosting on Github pages. We aim to reduce the technological know-how and time that is usually required for maintaining a personal or professional website.

####Why Should I Use This?
By using this template you will have a website that is well designed, easy to maintain, free to host and easy to update. While there are many options out there for personal and professional websites, most are dependant on the platform on which they were built, and cannot be easily migrated. This template, while built for Github Pages integration, provides flexibility should you choose to host it elsewhere.

##First Steps
In order to get started you will need to first create your own Github account by going to [github.com](https://github.com/). You will be prompted to choose an account type, choose the Free account option. After creating your account you will need to create a new repository. **You must name your repository [username].github.io** (replacing [username] with the username of your Github account). If you have any troubles creating a repository please refer to the [Github Pages](https://pages.github.com/) documentation.


![Create a Repository] (https://github.com/toddstoffer/jekyll-academic/blob/master/%20createrepo.gif)

####Copying the Template
Once you have created your new repository you will be taken to a setup page. At the bottom of that page you should see the **Import Code** button. Click on this button. The following page has a place for you to put the URL of an existing repository, copy and paste the following into that space:
`https://github.com/NCSU-Libraries/jekyll-academic`

After the import is complete you can then visit [username].github.io and you will see your newly created website. On this page you will see a variety of posts that contain more detailed information on editing, modifying and updating your new website.

##Next Steps
After you have imported the files into your repository you will want to clone the files to your desktop using GitHub Desktop, or any other tool that you are comfortable with. For more information on using GitHub Desktop click [here](https://desktop.github.com/). This will give you a working set of files that you can edit to personalize your website.

####Editing the config.yaml File
The config.yaml file that is in the root directory of the project is the first file that you will want to edit. This file allows you to set the website title, your email address and add in account information for a variety of social media services.

####Editing the accent.scss File
The accent.scss file allows you to modify the accent colors of your website. The default colors (red and black) can be set to any hexadecimal color that you would like. [W3Schools.com](http://www.w3schools.com/colors/colors_picker.asp) provides a good color picker that allows you to find the corresponding hex number for any color you wish to use.

####Editing the About Me and Resume Pages
These pages are each found in their corresponding directories (/about /resume). Simply open the index.md file from within each of these directories and begin making edits. Pay special attention to the formatting of the resume file. It makes use of single quotes ( \' ) and underscores ( \_ ) in the markdown markup language to format various aspects of the resume, including dates and university names.

####Editing Posts
Posts are all located in the \_posts folder. This folder contains sample posts that address in more depth the site structure and the markdown syntax. These posts are good to reference (by opening in a text editor of your choice) in order to get a better understanding of markdown. When you are ready to add a new post, simply copy one of the existing posts and edit it. Be sure to update the information at the top of the post, such as the title and timestamp. You will also want to rename the file to follow the same naming convention of the other post files (yyyy-mm-dd-post-title.md).

##Syncing Changes
After you have made changes to your site you will need to commit those changes to your repository for those changes to take effect. For more information on making commits please take a look at this [GitHub Cheat Sheet](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf). If you would prefer, you can also use GitHub Desktop to commit your changes, or drag-and-drop the changed files directly into your GitHub repository in the browser window. 
