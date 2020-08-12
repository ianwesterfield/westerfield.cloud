<!-- omit in toc -->
# [Westerfield.cloud](../README.md) / [Recipe](../recipe.md) / <b>Configure Package.json</b>

<!-- omit in toc -->
### 0.1 Please review [Using this Guide](/recipe.md#1-using-this-guide) before continuing.

<!-- omit in toc -->
## Steps
- [1. Modify `package.json`](#1-modify-packagejson)

### 1. Modify `package.json`
1. Merge the following changes into `package.json`
    ```json
    {
      "repository": {
        "type": "git",
        "url": "https://github.com/ianwesterfield/westerfield.cloud.git",
        "directory": "./projects/shell"
      },
      "author": {
        "name": "Ian Westerfield",
        "url": "https://github.com/ianwesterfield"
      },
    }
    ```
  > * 🦠 Be sure to adjust all values to match your own.
  > * Value of `repository.directory` should be the project's workspace-relative location.
  
#
##### <!-- omit in toc --> ☝️[top](#westerfieldcloud--bconfigure-packagejsonb)
<br/>
