<!-- omit in toc -->
# [Westerfield.cloud](../README.md) / [Recipe](./recipe.md) / <b>Application Setup</b>

<!-- omit in toc -->
#### 0.1 Please review [Using This Guide](./recipe.md#1-using-this-guide) before continuing.

<!-- omit in toc -->
## Steps
- [1. New Application](#1-new-application)
- [2. Create Application Shell](#2-create-application-shell)

## 1. New Application
1. Generate a new application: `$ ng g application --name shell --prefix shell --routing true --style scss`
2. Follow the [package configuration](./package.md) steps.
3. Follow the [Karma configuration](./karma.md) steps.
4. 🧪✅

## 2. Create Application Shell

[App-Shell Docs](https://angular.io/guide/app-shell)

> 🔥This task only needs to be performed once, and for the DEFAULT workspace application

1. Generate an application shell: `$ ng g app-shell --client-project shell`
2. 🧪✅
