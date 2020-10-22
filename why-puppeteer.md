
## Puppeteer - Web Scraping with a Headless Browser
It’s a Node.js library which provides a high-level API to control headless Chrome or Chromium or to interact with the DevTools protocol. It’s maintained by the Chrome DevTools team and an awesome open-source community.

## How to install Puppeteer
https://www.toptal.com/puppeteer/headless-browser-puppeteer-tutorial

## Code examples 
https://github.com/puppeteer/examples
https://github.com/checkly/puppeteer-examples
https://github.com/facebook/jest/tree/master/examples
https://puppeteersandbox.com/

## Jest Docs
https://jestjs.io/docs/en/cli
https://jestjs.io/docs/en/cli.html#runinband
https://jestjs.io/docs/en/using-matchers#arrays-and-iterables
https://codewithhugo.com/run-jest-sequentially/
https://github.com/facebook/jest/issues/6194#issuecomment-419837314

## JEST CLI
https://www.thetopsites.net/article/50827216.shtml

## Jest-Puppeteer Docs
https://jestjs.io/docs/en/puppeteer
https://jestjs.io/docs/en/expect#tocontainitem
https://github.com/xfumihiro/jest-puppeteer
https://github.com/smooth-code/jest-puppeteer

## Puppeteer API
https://github.com/puppeteer/puppeteer/blob/v2.0.0/docs/api.md#puppeteerlaunchoptions
https://pptr.dev/#?product=Puppeteer&version=v4.0.1&show=api-class-elementhandle
https://paulkode.com/notes/puppeteer-notes/
https://nitayneeman.com/posts/getting-to-know-puppeteer-using-practical-examples/#handling-events
https://github.com/puppeteer/puppeteer/issues/4506#
https://devhints.io/xpath
https://flaviocopes.com/puppeteer/

## Puppeteer Examples
https://help.apify.com/en/articles/3339492-waiting-for-dynamic-content
https://try-puppeteer.appspot.com/
https://www.tools4testing.com/contents/puppeteer/puppeteer-relative-xpath-by-attribute

## Sample usecase Jest, puppeteer
https://blog.logrocket.com/end-to-end-testing-react-apps-with-puppeteer-and-jest-ce2f414b4fd7/

## ag-grid Testing
https://github.com/LouisMoore-agGrid/react-jest-enzyme-ag-grid-v22
https://github.com/AhmedAGadir/ag-grid-react-testing-library-example/
https://github.com/seanlandsman/ag-grid-testing/blob/master/src/ag-grid.utils.ts

## Trade-Off
Based on following references, restricting options to pupeteer+jest over cypress.
https://www.npmtrends.com/nightmare-vs-puppeteer-vs-slimerjs-vs-webdriverio-vs-cypress-vs-nightwatch-vs-testcafe-vs-selenium-webdriver
https://medium.com/welldone-software/an-overview-of-javascript-testing-in-2019-264e19514d0a
https://www.godaddy.com/engineering/2018/05/07/moving-from-webdriver-to-puppeteer/
https://docs.cypress.io/guides/references/bundled-tools.html#Mocha
https://docs.cypress.io/guides/references/trade-offs.html#Permanent-trade-offs-1

## Run Jest using vscode
https://code.visualstudio.com/docs/nodejs/nodejs-debugging

## Steps to setup JEST BABEL and ES6 modules support
Babel is needed with Jest:
to understand ES6 modules (no import statement in Node). Babel will be used to transpiler the import statement of Es6.
to supports TypeScript

`yarn global add jest`
`yarn add --dev jest`

`yarn add --dev babel-jest @babel/core babel-cli`
# For es module
`yarn add --dev @babel/preset-env` 
# For typescript
`yarn add --dev @babel/preset-typescript` 
`yarn add --dev @types/jest` 

## Setup jest.config.js file
`jest --init`

## Below npm package to support transform es6 using babel
`npm install --save-dev @babel/plugin-transform-modules-commonjs`

## Jest config
https://jestjs.io/docs/en/configuration#testenvironment-string
https://jestjs.io/docs/en/getting-started

## Add ts-jest npm - if needed
`yarn add --dev ts-jest`
It's needed because typeScript support in Babel is transpilation, Jest will not type-check the tests as they are run.

## Enable preset in babel.config.js
https://datacadamia.com/web/javascript/test/jest_ts_configuration

# Basic rules
```
Rule #1
All methods in Puppeteer are async, don’t forget to await them.
Rule #2
In the script, in most cases, you should ask the Puppeteer to wait for something such as a request, response, an element, or for a moment.
Rule #3
Write the script rationally. Imagine you want to make a script to google something. How do you do it?
Rule #4
You cannot click on an element that is not visible! Imagine a menu with some items. First, you need to open the list; then, you can click on the sub-items.
Rule #5
Some webpages have their code or events (like jQuery events). You need to eval some JS to make them work.
Rule #6
If you are not familiar with CSS selectors, please go and learn them a bit.
Rule #7
When you navigate to a page like https://example.com/users/, don’t forget the tailing /.
```

## Sample package.json
```
"devDependencies": {
  "chai": "^4.2.0",
    "mocha": "^7.1.0",
    "chalk": "^4.1.0",
    "eslint": "^6.7.2",
    "eslint-config-prettier": "^6.7.0",
    "eslint-plugin-import": "^2.19.1",
    "@babel/core": "^7.10.4",
    "@babel/preset-env": "^7.10.4",
    "babel-jest": "^26.1.0",
    "babel-cli": "^6.26.0",
    // extra stuff
    "babel-preset-es2015": "^6.24.1",
     "@testing-library/jest-dom": "^4.2.4",
    "@testing-library/react": "^9.4.0",
    "@testing-library/user-event": "^7.2.1",
  },

// npm scripts  
"build": "babel --presets es2015 -d build/src tests/ src/pages",
"testmocha": "./node_modules/mocha/bin/mocha --timeout=30000 ./tests",
   
// jest config moved from package.json
"jest": {
    "//": "Comment goes here",
    "verbose": false,
    "scriptPreprocessor": "<rootDir>/node_modules/babel-jest",
    "transform": {
      "^.+\\.js?$": "babel-jest"
    }
    "setupFiles": [
      "<rootDir>/setup.js"
    ],
    "setupFilesAfterEnv": [
      "<rootDir>/defaultTimeout.js"
    ]
  }
```

## Puppeteer Examples
- https://devhints.io/xpath
- https://flaviocopes.com/puppeteer/
- https://github.com/puppeteer/puppeteer/issues/4733
- https://stackoverflow.com/questions/50963104/try-catch-unable-to-catch-unhandledpromiserejectionwarning
- https://medium.com/@JonasJancarik/handling-those-unhandled-promise-rejections-when-using-javascript-async-await-and-ifee-5bac52a0b29f
- https://blog.ramosly.com/how-ive-been-using-puppeteer-b8010e374ff7
- https://help.apify.com/en/articles/3339492-waiting-for-dynamic-content

- https://stackoverflow.com/questions/49538478/is-there-a-way-to-get-puppeteers-waituntil-networkidle-to-only-consider-xhr