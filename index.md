## Welcome to Web Labs

You can use the [editor on GitHub](https://github.com/prajavk/web-lab/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

# Why React?
```
-------------------------------------------------------
Choose          |    REACT        |   ANGULAR
-------------------------------------------------------
Components      | in-built        |   in-built
Testing         | Jest, Mocha     |   in-built
HTTP library    | Fetch, Axios    |   in-built
Routing         | React Router    |   in-built
I18n            | react-inlt      |   in-built
Animation       | react-motion    |   in-built
Form Validation | react-forms     |   in-built
CLI             | create-react-app|   in-built
------------------------------------------------------
```

How React components splited in a big page
1. ratings, navLink, authorPhoto
2. CourseSummary [course name, desc, ratings]
3. AuthorSummary [ authorPhoto, author profile]
3. AuthorCourses [ courseSummary]
4. SidebarNav [navLink]
5. Page [SidebarNav, AuthorSummary, AuthorCourses]

## React Basic Packages
1.react
2.react-dom
3.react-redux router
4.react-thunk
5.react-axios
6.redux
7.react-bootstrap

## Must Know Topics
ES6, Promise, Axios, React basics, Redux

## ESlint cmds
https://eslint.org/docs/user-guide/command-line-interface

## How to use npm scripts better than gulp, grunt?
https://medium.freecodecamp.org/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8

## Search for npm packages
https://libraries.io/

## Example to know npm scripts
https://github.com/coryhouse/react-slingshot

Example of npm scripts- The scripts below will run in order based on their prefix.
https://app.pluralsight.com/library/courses/npm-build-tool-introduction/table-of-contents
```
{
"name": "npm-scripts-example",
"version": "1.0.0",
"description": "npm scripts example",
"scripts": {
"prebuild": "echo I run before the build script",
"build": "cross-env NODE_ENV=production webpack",
"postbuild": "echo I run after the build script"
	}
}
```

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/prajavk/web-lab/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
