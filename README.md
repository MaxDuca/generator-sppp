# generator-sppp (SharePoint Pull-n-Push Generator) - alfa

> [Yeoman](http://yeoman.io/) generator for SharePoint client-side applications

[![npm version](https://badge.fury.io/js/generator-sppp.svg)](https://badge.fury.io/js/generator-sppp)

Yeoman generator for SharePoint - lets you quickly set up a project with sensible defaults for pulling and pushing files between SharePoint asset library and local projects sources.

Generated project allows immediately start developing SharePoint client-side solutions in Visual Studio Code or any other editor with instant publishing changes to SharePoint web site and downloading specific assets from SP Document library folder to local project assets which can be enforced with Git Diff algorithm for tracking changes.

## Supported SharePoint versions:
- SharePoint Online
- SharePoint 2013
- SharePoint 2016

## How to use:

### Install:

To use Yeoman, one need to has Node.js and NPM installed on the computer. Basic installation process description can be found in [this blog post](https://www.linkedin.com/pulse/preparing-development-machine-client-side-sharepoint-mac-koltyakov?trk=pulse_spock-articles).

Alter Node.js and NPM are staffed, install `Gulp`, `Bower`, `Yeoman` and `generator-sppp` globally in your Node.js environment.

```bash
npm install -g gulp bower yo generator-sppp
```

### Generate:

Make a new directory or clone a blank Git project of your own and navigate to the created folder.

Inside project directory execulte:

```bash
yo sppp [YourProjectName]
```

Then follow the the Yoman wizard instructions:

![Generator in action](http://koltyakov.ru/images/generator-sppp-demo.gif)

### Sync with SharePoint:

Now you can run gulp [sppull](https://www.npmjs.com/package/sppull) task:

```bash
gulp sppull-all
```

![SPPull in action](http://koltyakov.ru/images/generator-sppp-demo-2.gif)

It will deliver all files from assets folder from SharePoint to local directory.

Run gulp watch task before starting editing files:

```bash
gulp watch-assets
```

On files change they are uploaded and published to SharePoint with use of [gulp-spsave](https://www.npmjs.com/package/gulp-spsave).

> This is the first version of the project is welcomed to leave feature requests on [GitHub](https://github.com/koltyakov/generator-sppp/issues).