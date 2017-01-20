# NSF Challenge

[![Build Status](https://travis-ci.org/mozilla/nsf-challenge.svg?branch=master)](https://travis-ci.org/mozilla/nsf-challenge)
[![Uses Mofo Standards](https://MozillaFoundation.github.io/mofo-standards/badge.svg)](https://github.com/MozillaFoundation/mofo-standards)

## Development

### Setup

**Requirements**: Node, npm, git.

Run the following terminal commands to get started:

- `git clone https://github.com/mozilla/nsf-challenge.git`
- `cd nsf-challenge`
- `npm start`

This will install all dependencies, build the code, start a server at [http://127.0.0.1:2018](http://127.0.0.1:2018), and launch it in your default browser.

### Stack

#### HTML

HTML is generated from [Pug](https://pugjs.org) templates (formerly known as Jade).

Localized strings are pulled from [Java .properties](https://en.wikipedia.org/wiki/.properties) files located in `/locales`.

#### CSS

CSS is generated from [Sass](http://sass-lang.com/). The [Mofo Bootstrap](https://github.com/mozilla/mofo-bootstrap) theme is pulled in by default.

#### React

React is used *à la carte* for isolated component instances (eg: a tab switcher) since this is not a single page application, but rather a static generated website. This precludes the need for Flux architecture, or such libraries as React Router.

To add a React component, you can target a container element from `/source/js/main.js` and inject it.

### File Structure

```
.
├── env <- Environment variables
├── dest <- Compiled code generated from source. Don't edit!
├── locales <- Localized strings (Java .properties syntax)
├── scripts <- Scripts run by npm tasks
└── source <- Source code
    ├── images <- Image assets
    ├── js <- JS code
    ├── pug <- Pug/Jade templates
    └── sass <- Sass code
```

### Deployment

#### Staging

Currently staged builds are hosted via GitHub Pages. A staged build can be deployed to any repo by running:

`npm run stage REMOTE` (Change `REMOTE` to match your desired target)

#### Production

*TBD*
