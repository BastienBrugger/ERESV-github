## Why [Github Pages](https://pages.github.com/)?

- simplicity
- free and hosted online
- to get up and running quickly
- to have version control on your website, preferably Git
- to be able to share your code so others can easily re-use it
- option of personal website or websites for individual projects; multiple websites can be created with a single account. 

## Two kind of websites

1. Personal website at `<your_username>.github.io` that requires a seperate repository.
2. Project website at `<your_user_name>.github.io/<name_of_repository>` created in the same repository as the project, usually on a separate branch called `gh-pages`.

## Two options for designing/managing the website

1. Use Markdown for content and [Jekyll](https://jekyllrb.com/) theme for styling.
2. Do everything from scratch using HTML (for content) and CSS (for styling) files. You have complete control over the design and there are many super cool design codes available for free online (check [Start Bootstrap](https://startbootstrap.com/) and [Templated](https://templated.co/) for designs; [Unsplash](https://unsplash.com/) for free graphics).

## Why use Markdown+Jekyll?

1. You can use Markdown instead of HTML. Markdown is simpler to read and write.
2. You can add a Jekyll theme to your site without copying CSS files.
3. You can quickly create a new site using the Jekyll Theme Chooser.
4. You can use common templates, such as headers and footers, that are shared across files.
5. You can use a simplified build process to build your site with GitHub Pages.

## Activity: Build a simple website using markdown and a Jekyll theme

1. Create a new repository in your GitHub account called `<your-username>.github.io`. Intialization with README.md is not necessary, but is a good practice to let people know what the repository is about.

2. Create an `index.md` file. This Markdown file is the home-page for the website. Add something simple like `### Welcome to my first website!`. The '###' indicates a heading.

3. You can immediately see what the website looks like by initializing GitHub pages:
  - Go to `Settings > GitHub Pages`.
  - Under `Source`, select `master`.
  - Under `Theme Chooser`, select `Dinky`.
  
4. You will see a *_config.yml* file created in your repository. This file contains any configuration variables specific to your Jekyll theme. To learn more about the configuration options available for Dinky, check out its very own GitHub repository: https://github.com/pages-themes/dinky
  - Try changing the title and description of your website!

5. [Here's](https://github.com/ishan-mishra/sample-website-2) what your repository should look like. Now go to `https://<your-username>.github.io`. You have created your very first page!

6. You can add more simple Markdown files to be used as webpages (much easier than using HTML). Check out [my simple website!](https://ishan-mishra.github.io/).

7. You can customize the CSS and HTML files in your Jekyll theme. Read more about at https://help.github.com/en/articles/customizing-css-and-html-in-your-jekyll-theme. 

## Using Jekyll to create a template of your own

For repeated content like the navigation bar and style related code, which we'd have to edit on every page if we add, remove, or change the location of navigation item, we can create what Jekyll calls a layout that gets used on all our pages. For a detailed tutorial look at [Jonathan McGlone's excellent guide](http://jmcglone.com/guides/github-pages/) and the [associated repository](https://github.com/hankquinlan/hankquinlan.github.io).

## Creating a website from scratch using HTML and CSS

If you prefer to have more/complete control over the website design, its really not that hard! I will demostrate this with a [simple example](https://github.com/ishan-mishra/sample-website-1) that I created. You can also check [Natasha Batalha](https://natashabatalha.github.io/)'s and [Rodrigo Luger](https://rodluger.github.io/)'s awesome websites!


