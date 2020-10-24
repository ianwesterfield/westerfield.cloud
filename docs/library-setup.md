<!-- omit in toc -->
# [Westerfield.cloud](../README.md) / [Recipe](./recipe.md) / <b>Library Setup</b>

<!-- omit in toc -->
#### 0.1 Please review [Using this Guide](./recipe.md#1-using-this-guide) before continuing.
<br>

This guide will walk you through creating a namespaced library (`@westerfield-cloud/material` in this example) with optional secondary entrypoints.

<!-- omit in toc -->
## Steps
- [1. Establishing a new library](#1-establishing-a-new-library)
- [2. Configurations](#2-configurations)
- [3. Create a secondary entrypoint for the library](#3-create-a-secondary-entrypoint-for-the-library)

## 1. Establishing a new library

1. Create the library `$ ng g library @westerfield-cloud/material --prefix material`
2. Follow the [package configuration](./package.md) steps
3. Follow the [Karma configuration](./karma.md) steps
4. Rename `./src/public-api.ts` -> `./src/public_api.ts` for sake of convention with ng-packagr
5. Merge the following into `./ng-package.json`
    ```json 
    {
      "lib": {
        "entryFile" : "src/public_api.ts"
      }
    }
    ```
6. 🧪 ✅

## 2. Configurations

1. Merge the following into the workspace `package.json`:
    ```json
    {
      "scripts": {
        "dev:material": "npm run dev:material:build && npm run dev:material:link && npm run dev:material:build-watch",
        "dev:material:build": "ng build @westerfield-cloud/material --prod",
        "dev:material:build-watch": "ng build @westerfield-cloud/material --prod --watch",
        "dev:material:link": "cd dist/enquiren/wc/material && npm link && cd ../../../ && npm link @westerfield-cloud/material"
      }
    }
    ```
2. Merge the following into the workspace `tsconfig.base.json`:
    ```json 
    {
      "compilerOptions": {
        "paths": {
          "@westerfield-cloud/material": [
            "dist/enquiren/wc/components"
          ],
          "@westerfield-cloud/material/*": [
            "dist/enquiren/wc/components/*"
          ]
        }
      }
    ```
3. Merge the following into the library's `tsconfig.lib.json`:
    ```json
    {
      "compilerOptions": {
        "baseUrl": "..",
        "rootDir": ".",
        "paths": {
          "@westerfield-cloud/material": [
              "./"
            ],
            "@westerfield-cloud/material/*": [
              "./*"
            ]
          }
        }
      }  
    }
    ```
4. Merge the following into the library's `./ng-package.json`:
    ```json {
      "deleteDestPath": false
    }
    ```
5. 🧪 ✅

## 3. Create a secondary entrypoint for the library

1. Refer to the [Library Secondary Entrypoints](./library-secondary-entrypoints.md) steps
