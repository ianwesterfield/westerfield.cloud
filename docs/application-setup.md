<!-- omit in toc -->
# [Westerfield.cloud](../README.md) / [Recipe](./recipe.md) / <b>Application Setup</b>

<!-- omit in toc -->
#### 0.1 Please review [Using This Guide](./recipe.md#1-using-this-guide) before continuing.

<!-- omit in toc -->
## Steps
- [1. New Application](#1-new-application)
- [2. Create Application Shell](#2-create-application-shell)

## 1. New Application
1. Generate a new application: `$ ng g application --name shell --prefix shell --routing --strict --style scss`
2. Follow the [Karma configuration](./karma.md) steps.
3. Follow the [package configuration](./package.md) steps.
4. 🧪✅

## 2. Create Application Shell
[App-Shell Docs](https://angular.io/guide/app-shell)

> 🔥This task only needs to be performed once, and for the DEFAULT workspace application

1. Generate an application shell: `$ ng g app-shell --client-project shell`
2. Build the shell `$ ng run shell:app-shell`, or for production: `ng run my-app:app-shell:production`
3. Open `../dist/shell/browser/index.html` in a browser
4. Everything worked if you see the following markup
5. 🧪✅
