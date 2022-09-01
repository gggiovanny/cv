# My Cool CV

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Contributing](../CONTRIBUTING.md)

## About <a name = "about"></a>

A simple use of the CLI tool
[kissmyresume](https://github.com/karlitos/KissMyResume) for local building my own
CV in to multiple formats by using a [Json Resume](https://jsonresume.org/) theme
as input. Also includes hosting in [Github Pages](https://pages.github.com/).

## Getting Started <a name = "getting_started"></a>

Clone the repo and install the NPM dependencies with:
```
npm install
```

You can build my included CV into different formats with:

```
npm run build
```

Start a local server with live reloading:

```
npm start
```

Create or publish an `index.html` in the `/docs` directory for making it
available through [Github Pages](https://pages.github.com/).

```
npm run publish
```

You can test a themes and save each version in a folder with the same
name as theme (inside `/test` folder):
```
theme=<theme-name> npm run test 
```

### Prerequisites

If the below commands doesn't work for you, try to install kissmyresume
globally:

```
npm install -g kiss-my-resume
```

And after that, you will need to restart your terminal.


## Usage <a name = "usage"></a>
If you want to make your own CV, feel free to fork this repo and edit the input
JSON file with your own info. 

The default input file is `/resume/base.json`, but you can create a new empty
[Json Resume](https://jsonresume.org/) file with the all the posible fields with
the following command:
```
kissmyresume new <your-resume-name>
```

## Publish in Github Pages
If you run `npm run publish`, a `/docs` folder will be created with an
`index.html` with your CV. Just configure your repo following [this
guide](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site)
to point to your `docs` folders. And that's it! Now you have your new and shiny
resume available in `https://<your-github-username>.github.io/<your-cv-repo>/`.

## Find more themes
You can use any of the dozens of [compatible JSON Resume
themes](https://npmsearch.com/?q=jsonresume-theme).

And you can specify which one use with the local variables described below, or
direct executing the [kissmyresume
commands](https://github.com/karlitos/KissMyResume#usage).


## NPM local variables
Inside the `package.json`, in the `config` section, you can change the variables
for the following things:
+ **resumefile:** The input JSON Resume file.
+ **themepath:** Path of the theme to use in building, local serve, etc.
+ **buildpath:**: The desired path for generated output files.
+ **publishpath:**: The desired path to contain the index.html file of the CV.
  The default one is one recognized by Github Pages, so you don't need to create
  a special branch just for hosting your CV.

