# Westerfield.Cloud Recipe

## Ingredients

##

| Category          | :ramen: |
| ----------------- | ------- |
| **Serviing Size** | `(n+1)` |

## Utensils

##

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

## 1) In the Beginning...

1. Get a new repo setup with GitHub
2. :white_check_mark:&nbsp;&nbsp;Establish an Angular workspace `$ ng new --name westerfield-cloud --directory . --create-application false`
3. Generate a new default shell application: `$ ng g application --name shell --prefix cloud --routing true --style scss`
4. :white_check_mark: Test for no errors with `ng build --prod && ng serve` to confirm everything is correctly wired.
