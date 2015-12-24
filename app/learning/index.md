---
layout: default
markdown: 1
title: Getting started with Yeoman
sidebar: sidebars/learning.md
---

Yeoman is a generic scaffolding system allowing you to create any kind of app. It'll allow you to rapidly get started on new projects and streamline the maintenance of existing projects.

Yeoman is language agnostic. It can generates projects in any languages (Web, Java, Python, C#, etc.)

Yeoman by itself doesn't make any decision. Yeoman runs _generators_ who're making every decision. A generator is basically a plugin in the Yeoman environment. There's more than [1500 publicly available generators](/generators) and you can [create your own](/authoring) if public ones are not matching your team workflow; Yeoman is always the right choice for your scaffolding needs.

Here's a couple common use cases:

- Creating new projects rapidly
- Creating section of your project (how about creating a new controller with unit tests?)
- Creating packages
- Bootstrapping new services
- Enforcing standards and latest best practices in any new app components.
- Promote your project by allowing users to bootstrap new plugins
- Etc, etc

## Getting started

Yo is the Yeoman command line utility allowing you to create projects utilizing scaffolding templates we refer to as generators. You typically install yo and any generators you think you might use via npm.

### Installing yo and some generators

First, using `npm` you'll need to install `yo`:

```sh
npm install -g yo
```

Then you'll need to install a generator. Generators are npm packages named `generator-N`, you can search them on [our website](/generators) or by selecting "install a generator" menu option while running `yo`. To install the `webapp` generator, you'd use:

```
npm install -g generator-webapp
```

*TODO: Add note about troubleshooting installation errors*

*npm is the package manager for [Node.js](https://nodejs.org/) and comes bundled with it.*

*On Windows, we suggest you use an improved command line tool such as [`cmder`](http://cmder.net/) or PowerShell to improve the experience.*


### Basic scaffolding

We'll use `generator-webapp` in our examples below. Replace `webapp` with the name of your generator for the same result.

To scaffold a new project, you'll run:

```sh
yo webapp
```

At this point, most generators will ask you a series of questions to customize your new project. They might also provide options to customize your project further or to allow automation of the scaffolding, to see which options are available you'll run:

```sh
yo webapp --help
```

You'll realize a lot of generators rely on build systems (like Grunt or Gulp), and package manager (like npm and Bower). Make sure to visit your generator site to learn how to run and maintains your new app. You can easily access a generator home page by running:

```sh
npm home generator-webapp
```

Generators scaffolding complex frameworks are likely to provide generators to scaffold smaller part of a project. These generators are usually referred to as _sub-generator_, are are accessed as `generator:sub-generator`. Taking `generator-angular` as example, once you've generated you full angular app, you might wish to add a new controller. You'd do so by running:

```sh
yo angular:controller MyNewController
```


### Other yo commands

Other than the basics covered in the previous section, `yo` is also a fully interactive tools. Simply typing `yo` in your terminal will allow you to select from a list of options to manage everything related to your generators: run, update, install, help and other utilities.

Yo also provide the following commands.

- `yo --help` Access the full help screen
- `yo --generators` List every installed generators
- `yo --version` Get the version


### Troubleshooting

If you run into any issues, start by running

```sh
yo doctor
```

The `doctor` command will diagnose your system and provide steps to resolve the most common issues.


### Creating your own generators

See [Authoring](/authoring).
