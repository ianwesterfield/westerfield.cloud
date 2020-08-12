<!-- omit in toc -->
# [Westerfield.cloud](../README.md) / [Recipe](../recipe.md) / <b>Configure Karma</b>

<!-- omit in toc -->
#### Please review [Using This Guide](../recipe.md#1-using-this-guide) before continuing.

<!-- omit in toc -->
## Steps
> 🔥These steps must be performed for every new application or library
- [1. Modify `karma.conf.js`](#1-modify-karmaconfjs)

### 1. Add a headless browser for quicker automated testing
1. Merge the following changes into `config.set`
   ```js
    module.exports = function (config) {
      config.set({
        customLaunchers: {
          ChromeHeadless: {
            base: "Chrome",
            flags: [
              "--headless", // no ui
              "--disable-gpu", // no hardware acceleration
              "--no-sandbox", // no "stealth" browsing feature
              "--remote-debugging-port=9222", // needed for test runner
            ],
          },
        },
        browsers: ["ChromeHeadless"],
        singleRun: true,
        failOnEmptyTestSuite: false,
      });
    };
    ```
