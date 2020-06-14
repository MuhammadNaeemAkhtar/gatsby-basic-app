# Notes

SURGE URL: http://gatsby-basic-app-mna.surge.sh/

## Step 0: Set up development environment

npm install -g gatsby-cli   // To install gatsby CLI via npm it lets you to create Gatsby-powered sites quickly

Note: when you install Gatsby and run it for the first time, you’ll see a short message notifying you about 
		anonymous usage data that is being collected for Gatsby commands, you can read more about how that 
		data is pulled out and used in the telemetry doc.

gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world  //Create a new site from a starter:
gatsby new [SITE_DIRECTORY_NAME] [URL_OF_STARTER_GITHUB_REPO]

If you omit a URL from the end, Gatsby will automatically generate a site for you based on the default starter.

gatsby develop //Start the development

Recommend using Prettier, a tool that helps format your code to avoid errors. Search for “Prettier - Code formatter”.

To summarize, in this section you:

- Learned about the command line and how to use it
- Installed and learned about Node.js and the npm CLI tool, the version control system Git, and the Gatsby CLI tool
- Generated a new Gatsby site using the Gatsby CLI tool
- Ran the Gatsby development server and visited your site locally
- Downloaded a code editor
- Installed a code formatter called Prettier

These are some of the main web technologies you’ll use when building a Gatsby site:

- HTML: A markup language that every web browser is able to understand. It stands for HyperText Markup Language. HTML gives your web content a universal informational structure, defining things like headings, paragraphs, and more.
- CSS: A presentational language used to style the appearance of your web content (fonts, colors, layout, etc). It stands for Cascading Style Sheets.
- JavaScript: A programming language that helps us make the web dynamic and interactive.
- React: A code library (built with JavaScript) for building user interfaces. It’s the framework that Gatsby uses to build pages and structure content.
- GraphQL: A query language that allows you to pull data into your website. It’s the interface that Gatsby uses for managing site data.


## STEP 1: Get to know gatsby building blocks

Gatsby uses hot reloading to speed up your development process. Essentially, when you’re running a Gatsby development server,
the Gatsby site files are being “watched” in the background — any time you save a file, your changes will be immediately 
reflected in the browser. You don’t need to hard refresh the page or restart the development server — your changes just 
appear.

Add an image. (In this case, a random image from Unsplash).
https://source.unsplash.com/random/400x200

This hybrid “HTML-in-JS” is actually a syntax extension of JavaScript, for React, called JSX

You’re writing JSX, not pure HTML and JavaScript. How does the browser read that? The short answer: It doesn’t. 
Gatsby sites come with tooling already set up to convert your source code into something that browsers can interpret.

Gatsby is built on React.

For external links to pages not handled by your Gatsby site, use the regular HTML <a> tag.

Deploying a Gatsby site
Gatsby is a modern site generator, which means there are no servers to set up or complicated databases to deploy. 
Instead, the Gatsby build command produces a directory of static HTML and JavaScript files which you can deploy to a 
static site hosting service.

Gatsby Cloud is another deployment option, built by the team behind Gatsby. In the next section, 
you’ll find instructions for deploying to Gatsby Cloud

gatsby build //Next, build your site by running the following command in the terminal at the root of your site

surge public/   //Then finally deploy your site by publishing the generated files to surge.sh. 

For newly-created surge account, you need to verify your email with surge before publishing your site 
(check your inbox first and verify your email).

Gatsby Cloud is a platform built specifically for Gatsby sites, with features like real-time previews, 
fast builds, and integrations with dozens of other tools. It’s the best place to build and deploy sites 
built with Gatsby, and you can use Gatsby Cloud free for personal projects.

When you created a new Gatsby project with a starter, it automatically made an initial git commit, 
or a set of changes. Now, you can push your changes to the new remote location:

In this section you:

- Learned about Gatsby starters, and how to use them to create new projects
- Learned about JSX syntax
- Learned about components
- Learned about Gatsby page components and sub-components
- Learned about React “props” and reusing React components

## STEP 2: Introduction to styling in gatsby

One of the most straightforward ways to add global styles to a site is using a global .css stylesheet.

cd src

mkdir styles

cd styles

touch global.css  //didn't work

Create the gatsby-browser.js
cd ../..
touch gatsby-browser.js
💡 What is gatsby-browser.js? Don’t worry about this too much and for now, just know that gatsby-browser.js is one of a handful of special files that Gatsby looks for and uses (if they exist).

Note: Both CommonJS (require) and ES Module (import) syntax work here. If you’re not sure which to choose, import is usually a good default. When working with files that are only run in a Node.js environment however (like gatsby-node.js), require will need to be used.

Tip: This part of the tutorial has focused on the quickest and most straightforward way to get started styling a Gatsby site — importing standard CSS files directly, using gatsby-browser.js. In most cases, the best way to add global styles is with a shared layout component. Check out the docs for more on that approach.


In this section, you’ll create a new page component and style that page component using a CSS Module.
You’ll notice that the file name ends with .module.css instead of the usual .css. This is how you tell Gatsby that this CSS file should be processed as a CSS module rather than plain CSS.

- You’ll create a <User /> component and style that component using a CSS module.
- Create the file for the CSS at src/pages/about-css-modules.module.css.
- Import the new src/pages/about-css-modules.module.css file into the about-css-modules.js
- Create a new <User /> component inline in the about-css-modules.js page component. Modify about-css-modules.js

. Other CSS options
Gatsby supports almost every possible styling option (if there isn’t a plugin yet for your favorite CSS option, please contribute one!)
-    Typography.js
-    Sass
-    JSS
-    Stylus
-    PostCSS

and more!

## STEP 3: Creating nested layout components

In this part, you’ll learn about Gatsby plugins and creating “layout” components.


## //////////////////////////////////

 Auto Generated

## //////////////////////////////////


<!-- AUTO-GENERATED-CONTENT:START (STARTER) -->
<p align="center">
  <a href="https://www.gatsbyjs.org">
    <img alt="Gatsby" src="https://www.gatsbyjs.org/monogram.svg" width="60" />
  </a>
</p>
<h1 align="center">
  Gatsby's hello-world starter
</h1>

Kick off your project with this hello-world boilerplate. This starter ships with the main Gatsby configuration files you might need to get up and running blazing fast with the blazing fast app generator for React.

_Have another more specific idea? You may want to check out our vibrant collection of [official and community-created starters](https://www.gatsbyjs.org/docs/gatsby-starters/)._

## 🚀 Quick start

1.  **Create a Gatsby site.**

    Use the Gatsby CLI to create a new site, specifying the hello-world starter.

    ```shell
    # create a new Gatsby site using the hello-world starter
    gatsby new my-hello-world-starter https://github.com/gatsbyjs/gatsby-starter-hello-world
    ```

1.  **Start developing.**

    Navigate into your new site’s directory and start it up.

    ```shell
    cd my-hello-world-starter/
    gatsby develop
    ```

1.  **Open the source code and start editing!**

    Your site is now running at `http://localhost:8000`!

    _Note: You'll also see a second link: _`http://localhost:8000/___graphql`_. This is a tool you can use to experiment with querying your data. Learn more about using this tool in the [Gatsby tutorial](https://www.gatsbyjs.org/tutorial/part-five/#introducing-graphiql)._

    Open the `my-hello-world-starter` directory in your code editor of choice and edit `src/pages/index.js`. Save your changes and the browser will update in real time!

## 🧐 What's inside?

A quick look at the top-level files and directories you'll see in a Gatsby project.

    .
    ├── node_modules
    ├── src
    ├── .gitignore
    ├── .prettierrc
    ├── gatsby-browser.js
    ├── gatsby-config.js
    ├── gatsby-node.js
    ├── gatsby-ssr.js
    ├── LICENSE
    ├── package-lock.json
    ├── package.json
    └── README.md

1.  **`/node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages) are automatically installed.

2.  **`/src`**: This directory will contain all of the code related to what you will see on the front-end of your site (what you see in the browser) such as your site header or a page template. `src` is a convention for “source code”.

3.  **`.gitignore`**: This file tells git which files it should not track / not maintain a version history for.

4.  **`.prettierrc`**: This is a configuration file for [Prettier](https://prettier.io/). Prettier is a tool to help keep the formatting of your code consistent.

5.  **`gatsby-browser.js`**: This file is where Gatsby expects to find any usage of the [Gatsby browser APIs](https://www.gatsbyjs.org/docs/browser-apis/) (if any). These allow customization/extension of default Gatsby settings affecting the browser.

6.  **`gatsby-config.js`**: This is the main configuration file for a Gatsby site. This is where you can specify information about your site (metadata) like the site title and description, which Gatsby plugins you’d like to include, etc. (Check out the [config docs](https://www.gatsbyjs.org/docs/gatsby-config/) for more detail).

7.  **`gatsby-node.js`**: This file is where Gatsby expects to find any usage of the [Gatsby Node APIs](https://www.gatsbyjs.org/docs/node-apis/) (if any). These allow customization/extension of default Gatsby settings affecting pieces of the site build process.

8.  **`gatsby-ssr.js`**: This file is where Gatsby expects to find any usage of the [Gatsby server-side rendering APIs](https://www.gatsbyjs.org/docs/ssr-apis/) (if any). These allow customization of default Gatsby settings affecting server-side rendering.

9.  **`LICENSE`**: Gatsby is licensed under the MIT license.

10. **`package-lock.json`** (See `package.json` below, first). This is an automatically generated file based on the exact versions of your npm dependencies that were installed for your project. **(You won’t change this file directly).**

11. **`package.json`**: A manifest file for Node.js projects, which includes things like metadata (the project’s name, author, etc). This manifest is how npm knows which packages to install for your project.

12. **`README.md`**: A text file containing useful reference information about your project.

## 🎓 Learning Gatsby

Looking for more guidance? Full documentation for Gatsby lives [on the website](https://www.gatsbyjs.org/). Here are some places to start:

- **For most developers, we recommend starting with our [in-depth tutorial for creating a site with Gatsby](https://www.gatsbyjs.org/tutorial/).** It starts with zero assumptions about your level of ability and walks through every step of the process.

- **To dive straight into code samples, head [to our documentation](https://www.gatsbyjs.org/docs/).** In particular, check out the _Guides_, _API Reference_, and _Advanced Tutorials_ sections in the sidebar.

## 💫 Deploy

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gatsbyjs/gatsby-starter-hello-world)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/gatsbyjs/gatsby-starter-hello-world)

<!-- AUTO-GENERATED-CONTENT:END -->
