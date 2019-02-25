---
title: Theme Boilerplate
tags:
- Developers
- Theme
- Themes
- Boilerplate
category: developer
menu:
  developer:
    identifier: theme-boilerplate
---

Vanilla provides a [boilerplate](https://www.npmjs.com/package/@vanillaforums/theme-boilerplate) to build custom themes. It contains all files necessary for a theme with customizable styles.

Styles are written in SASS and most of it bases itself in SASS variables and inheritance. Variables are carried through sections and components making the final styles flexible but also consistent throughout the site.

## Getting Started

Node and Yarn are prerequisites to use this tool. Please download and install the latest stable release from the official [Node.js download page](http://nodejs.org/download/) and [yarn](https://yarnpkg.com/en/docs/install).
  
> **Notice**: It is important that you install Node in a way that does not require you to `sudo`.



1. Navigate to your theme folder and add the boilerplate package:

  ```
  yarn add @vanillaforums/theme-boilerplate
  ```

2. Run the installation command:

  ```
  yarn run boilerplate-install my-custom-theme "My Custom Theme"
  ```

  - Replace `my-custom-theme` with your theme key. This should be unique and **must exactly match** the folder name, including capitalization. It should also follow the `dashed-lower-case` naming convention.
  - Replace `My Custom Theme` with your theme name (keep the double quotes). This is the name that appears on the dashboard.

3. This tool also has a build step, provided by the [Vanilla CLI](https://docs.vanillaforums.com/developer/vanilla-cli/). This step is necessary to generate scripts and stylesheets that run in the browser.
   [Make sure the Vanilla CLI is installed](https://docs.vanillaforums.com/developer/vanilla-cli/installation), then run the following command on the theme folder to build:

  ```
  vanilla build
  ```

4. Your theme is ready to be enabled. On your localhost navigate to **Dashboard > Appearance > Themes** and enable your theme.

### Usage

You might want to start taking a look at `src/scss/_variables.scss`. There you can find most of the variables you need to customize your theme.

A good starting point is to create variables containing your brand values on the top of the `_variables.scss`, like colors, font family, sizes, etc.

Once your variables are set, you may start customizing!

To know more about the boilerplate SCSS structure please visit the [variables description](https://docs.vanillaforums.com/developer/theme-boilerplate/sctructure-variables/) page.
There you can find information about what each variable represents, naming conventions and folder structure.

Essentially you can overwrite whatever you like but be careful! Some variables are heavily inherited and not meant to be overwritten. Doing so may break your layout.

### Building Styles / Javascript / Images

The boilerplate frontend assets are built with the [Vanilla CLI](https://docs.vanillaforums.com/developer/vanilla-cli/).
