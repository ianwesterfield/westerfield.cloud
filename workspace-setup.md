<!-- omit in toc -->
# [Westerfield.cloud](./README.md) / [Recipe](./recipe.md) / <b>Workspace Setup</b>
### 0.1. Please review [1. Using This Guide](./recipe.md#1-using-this-guide) before continuing.
<br />

<!-- omit in toc -->
## Steps
- [1. Establish the workspace](#1-establish-the-workspace)
- [2. Disable Ivy](#2-disable-ivy)

## 1. Establish the workspace
1. Navigate to a directory in which you want to create this project
2. Create an Angular workspace `$ ng new --name westerfield-cloud --create-application false`
3. ⏩ workspace `package.json`:
    ```
    "scripts": {
      "qaTeam": "ng lint && ng build --prod && ng test && ng e2e"
    },
    ```
4. Show your 👩‍🔬 around
5. Follow the [package configuration](docs/package.md) steps

## 2. Disable Ivy

> 🦠 You cannot continue with this step unless you have already created at least one application
> *  Refer to the [Application Setup](./docs/application-setup.md) steps.

Angular CLI has compatibility issues with parallel local development builds and Ivy. The preferred library component development workflow only works locally with Ivy disabled. 

Additional Reading: [GitHub: Issues with parallel build using ivy](https://github.com/angular/angular/issues/32431)

1. ⏩ workspace `angular.json`:
    ```json 
    {
      "projects": {
        "sdx": {
          "architect": {
            "build": {
              "options": {
                "aot": false,
              }
            }
          }
        }
      }
    }
    ```
2. ⏩ workspace `tsconfig.base.json`:
      ```json
      {
        "angularCompilerOptions": {
          "enableIvy": false
        }
      }
     ```
3. Run your 👩‍🔬
#
##### <!-- omit in toc --> ☝️[top](#westerfieldcloud--bworkspace-setupb)
<br/>
