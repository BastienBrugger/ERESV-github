## Why Github Pages?

- simplicity
- Free and hosted online
- to get up and running quickly
- to have version control on your website, preferably Git
- to be able to share my code so others can easily re-use it
- option of personal website or websites for individual projects

## Two kind of websites

1. Personal website at `<your_username>.github.io` that requires a seperate repository.
2. Project website at `<your_user_name>.github.io/<name_of_repository>` created in the same repository as the project, usually on a separate branch called `gh-pages`

## Two options for designing/managing the website

1. Use markdown for template and Jekyll theme for styling.
2. Do everything from scratch using HTML (for content) and CSS (for styling) files. You have complete control over the design and there are many super cool design codes available for free online (more on this later!)

## Why use Jekyll?

1. You can use Markdown instead of HTML. Markdown is simpler to read and write.
2. You can add a Jekyll theme to your site without copying CSS files.
3. You can quickly create a new site using the Jekyll Theme Chooser.
4. You can use common templates, such as headers and footers, that are shared across files.
5. You can use a simplified build process to build your site with GitHub Pages.

## Activity: Build a simple website using markdown and a jekyll theme

1. Create a new repository in your GitHub account called `<your-username>.github.io`. Intialization with README.md is not necessary, but is a good practice to let people know what the repository is about.

2. Create an `index.md` file. This Markdown file is the home-page for the website. Add something simple like `### Welcome to my first website!`. The '###' indicates a heading of 

3. You can immediately see what the website looks like by initializing GitHub pages. 
  - Go to `Settings > GitHub Pages`. 
  - Under `Source`, select `master`
  - Under `Theme Chooser`, select `Dinky`
  
4. You will see a _config.yml file created in your repository. This file contains any configuration variables specific to your Jekyll theme. To learn more about the configuration options available for Dinky, check out its very own GitHub repository: https://github.com/pages-themes/dinky
  - Try changing the title and description of your website!

5. Now go to `https://<your-username>.github.io`. You have created your very first page!

6. You can then use simple markdown files as webpages (much easier than using HTML). Check out [this](https://github.com/ishan-mishra/sample-website-2) simple example. 


