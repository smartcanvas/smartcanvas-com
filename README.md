## Smart Canvas

### Included out of the box:

* [Polymer](http://polymer-project.org), [Paper](https://elements.polymer-project.org/browse?package=paper-elements), [Iron](https://elements.polymer-project.org/browse?package=iron-elements) and [Neon](https://elements.polymer-project.org/browse?package=neon-elements) elements
* [Material Design](http://www.google.com/design/spec/material-design/introduction.html) layout
* Routing with [Page.js](https://visionmedia.github.io/page.js/)
* Unit testing with [Web Component Tester](https://github.com/Polymer/web-component-tester)
* End-to-end Build Tooling (including [Vulcanize](https://github.com/Polymer/vulcanize))

### Install dependencies

#### Quick-start

With Node.js installed, run the following one liner from the root:

```sh
npm install -g gulp bower && npm install && bower install
```

#### Prerequisites (for everyone)

Major dependencies:

- Node.js, used to run JavaScript tools from the command line.
- npm, the node package manager, installed with Node.js and used to install Node.js packages.
- gulp, a Node.js-based build tool.
- bower, a Node.js-based package manager used to install front-end packages (like Polymer).

**To install dependencies:**

1)  Check your Node.js version.

```sh
node --version
```

The version should be at or above 0.12.x.

2)  If you don't have Node.js installed, or you have a lower version, go to [nodejs.org](https://nodejs.org) and click on the big green Install button.

3)  Install `gulp` and `bower` globally.

```sh
npm install -g gulp bower
```

This lets you run `gulp` and `bower` from the command line.

4)  Install local `npm` and `bower` dependencies.

```sh
cd smartcanvas-com && npm install && bower install
```

This installs the element sets (Paper, Iron, Platinum) and tools required to build and serve the app.

### Development workflow

#### Serve / watch

```sh
gulp serve
```

This outputs an IP address you can use to locally test and another that can be used on devices connected to your network.

#### Run tests

```sh
gulp test:local
```

This runs the unit tests defined in the `app/test` directory through [web-component-tester](https://github.com/Polymer/web-component-tester).

#### Build & Vulcanize

```sh
gulp
```

Build and optimize the current project, ready for deployment. This includes linting as well as vulcanization, image, script, stylesheet and HTML optimization and minification.

## Application Theming

Polymer 1.0 introduces a shim for CSS custom properties. We take advantage of this in `app/styles/app-theme.html` to provide theming for your application. You can also find our presets for Material Design breakpoints in this file.

[Read more](https://www.polymer-project.org/1.0/docs/devguide/styling.html) about CSS custom properties.

## Dependency Management

Polymer uses [Bower](http://bower.io) for package management. This makes it easy to keep your elements up to date and versioned. For tooling, we use npm to manage Node.js-based dependencies.

## Yeoman support

### Element (alias: El)
Generates a polymer element in `app/elements` and optionally appends an import to `app/elements/elements.html`.

Example:
```bash
yo polymer:element my-element

# or use the alias

yo polymer:el my-element
```

**Note: You must pass in an element name, and the name must contain a dash "-"**

One can also include element dependencies to be imported. For instance, if you're creating a `fancy-menu` element which needs to import `paper-button` and `paper-checkbox` as dependencies, you can generate the file like so:

```bash
yo polymer:el fancy-menu paper-button paper-checkbox
```


