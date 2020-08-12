<!-- omit in toc -->
# [Westerfield.cloud](../README.md) / [Recipe](./recipe.md) / <b>Library Setup</b>

<!-- omit in toc -->
#### 0.1 Please review [Using this Guide](/recipe.md#1-using-this-guide) before continuing.
<br>

This guide will walk you through the steps to create a namespaced library called `@westerfield-cloud/components`.

<!-- omit in toc -->
## Steps
- [1. Establishing a new library](#1-establishing-a-new-library)
- [2. Create a secondary entrypoint for the library](#2-create-a-secondary-entrypoint-for-the-library)
- [3. Configurations](#3-configurations)

## 1. Establishing a new library

1. Generate the library `$ ng g library @westerfield-cloud/components --prefix wc-cmp`
2. Follow the [package configuration](./package.md) steps
3. Follow the [Karma configuration](./karma.md) steps
4. Rename `./src/public-api.ts` -> `./src/public_api.ts` for sake of convention with ng-packagr
5. Merge the following update into the`./ng-package.json`:
    ```json 
    {
      lib": {
        "entryFile" : "src/public_api.ts"
      }
    }
    ```
6. 🧪✅

## 2. Create a secondary entrypoint for the library

1. Refer to the [Library Secondary Entrypoints](./library-secondary-entrypoints.md) steps

## 3. Configurations

1. Merge the following into the workspace `package.json`:
    ```json
    {
      scripts: {
        "dev:wc-cmp": "npm run dev:wc-cmp:build && npm run dev:wc-cmp:link && npm run dev:wc-cmp:build-watch",
        "dev:wc-cmp:build": "ng build @westerfield-cloud/components --prod",
        "dev:wc-cmp:build-watch": "ng build @westerfield-cloud/components --prod --watch",
        "dev:wc-cmp:link": "cd dist/wc/components && npm link && cd ../../../ && npm link @westerfield-cloud/components"
      }
    }
    ```
2. Merge the following to the `compilerOptions.paths` collection of the workspace `tsconfig.base.json`:
    ```json
    "@westerfield-cloud/components": [
      "dist/wc/components"
    ],
    "@westerfield-cloud/components/*": [
      "dist/wc/components/*"
    ]
    ```
3. Merge the following into the `compilerOptions` object of the library's `tsconfig.lib.json`:
    ```json
    "baseUrl": "..",
    "rootDir": ".",
    ```
4. Merge the following into the `compilerOptions.paths` collection of the library's `tsconfig.lib.json`:
    ```json
    "@westerfield-cloud/components": [
        "./"
      ],
      "@westerfield-cloud/components/*": [
        "./*"
      ]
    }
    ```
5. Merge the following into the library's `./ng-package.json`:
    ```json
    "deleteDestPath": false
    ```
6. 🧪✅
7. You should now be able to import this library into other projects or even other library members
