<!-- omit in toc -->
# <b>Westerfield.cloud<b>

<!-- omit in toc -->
## Contents
- [1. Why?](#1-why)
- [2. Development](#2-development)
  - [2.1. Environment](#21-environment)
  - [2.2. Tools](#22-tools)
  - [2.3. Material Design System](#23-material-design-system)
  - [2.4. Steps to Reproduce](#24-steps-to-reproduce)
  - [2.5. Development server](#25-development-server)
  - [2.6. Code scaffolding](#26-code-scaffolding)
  - [2.7. Build](#27-build)
  - [2.8. Running unit tests](#28-running-unit-tests)
  - [2.9. Running end-to-end tests](#29-running-end-to-end-tests)
  - [2.10. Further help](#210-further-help)

## 1. Why?
This effort is motived by three concerns:
  - **Boilerplate**: I want a themed, future-proof, full-stack boilerplate for deeply integrated sandboxes or other projects I have in mind.
  - **Documentation**: A project to pool my knowledge and preferred techniques into a single location for easy reference.
  - ❤️ A chance to give something back to the community.

## 2. Development
<br/>

### 2.1. Environment

```shell
$ng v

     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/


Angular CLI: 10.0.4
Node: 10.13.0
OS: win32 x64

Angular:
...
Ivy Workspace:

Package                      Version
------------------------------------------------------
@angular-devkit/architect    0.1000.4
@angular-devkit/core         10.0.4
@angular-devkit/schematics   10.0.4
@schematics/angular          10.0.4
@schematics/update           0.1000.4
rxjs                         6.5.5
```

### 2.2. Tools
#
* [Angular CLI](https://cli.angular.io/)
  * global installation
* [VS Code](https://code.visualstudio.com/download) & Recommended Extensions 💯
  * [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
  * [file-tree-generator](https://marketplace.visualstudio.com/items?itemName=Shinotatwu-DS.file-tree-generator)
  * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
  * [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
  * [JSON to TS](https://marketplace.visualstudio.com/items?itemName=MariusAlchimavicius.json-to-ts)
  * [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  * [Path Intellisense]([https://link](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense))

### 2.3. Material Design System
#
* [Material.io](https://material.io)
* [Web Guide](https://material.io/develop/web)
* [Components Catalog](https://material-components.github.io/material-components-web-catalog/#/)
* [Color Tool](https://material.io/resources/color/#!/?view.left=0&view.right=0&primary.color=3F51B5&secondary.color=c1c1c1)
* [Example Angular Material.io integration](https://github.com/trimox/angular-mdc-web/tree/master/packages)
<br/>

### 2.4. Steps to Reproduce

Follow my [Recipe](./docs/recipe.md) to recreate this entire application - top to bottom, front to back! (yeah, step one really is step 1.2.4.1 😉)

### 2.5. Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

### 2.6. Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### 2.7. Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

### 2.8. Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### 2.9. Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

### 2.10. Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
