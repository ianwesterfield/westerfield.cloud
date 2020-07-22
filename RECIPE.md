### Westerfield.cloud Recipe

#### Ingredients

| Category          | :ramen: |
| ----------------- | ------- |
| **Serving Size** | `(n+1)` |

#### Utensils

```shell
$ng v

     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/


Angular CLI: 10.0.3
Node: 14.6.0
OS: darwin x64

Angular: 10.0.4
... animations, common, compiler, compiler-cli, core, forms
... platform-browser, platform-browser-dynamic, router
Ivy Workspace: Yes

## Package Version

@angular-devkit/architect 0.1000.3
@angular-devkit/build-angular 0.1000.3
@angular-devkit/build-optimizer 0.1000.3
@angular-devkit/build-webpack 0.1000.3
@angular-devkit/core 10.0.3
@angular-devkit/schematics 10.0.3
@angular/cli 10.0.3
@ngtools/webpack 10.0.3
@schematics/angular 10.0.3
@schematics/update 0.1000.3
rxjs 6.5.5
typescript 3.9.7
webpack 4.43.0
```
#### Legend

| :white_check_mark: | Check-in and Merge to Base Branch
| ----------------- | ------- |
| `[...] westerfield [...]` | **Replace any reference to "westerfield" with your own family name**


#### 1) In the Beginning...

<optional> Optionally establish a new repo and be sure all utensils are updated, then:
  
1. :white_check_mark:&nbsp;&nbsp;Create an Angular workspace `$ ng new --name westerfield-cloud --directory . --create-application false`
2. Generate a new default shell application: `$ ng g application --name shell --prefix cloud --routing true --style scss`
3. Add a new script to the workspace `project.json`:
  ```
  "scripts": {
    ...,
    "qaTeam": "ng lint && ng build --prod && ng test && ng e2e"
  },
  ```
4. :white_check_mark:&nbsp;&nbsp;Give your qaTeam a try to confirm everything is wired correctly: `$ npm run qaTeam`
