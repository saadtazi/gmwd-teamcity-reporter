# gmwd-teamcity-reporter

A teamcity reporter for grunt-mocha-webdriver tasks.

It can be used for saucelabs and selenium tests. If you need teamcity reporter for grunt-mocha-webdriver phantom tests, just use `[mocha-teamcity-reporter](`)https://www.npmjs.org/package/mocha-teamcity-reporter)`.

This package is largely inspired (and it is an euphemism) by the `mocha-teamcity-reporter`.

# Usage

Add `customReporter: 'teamcity_reporter'` to your `mochaWebdriver` `options` tasks.

```
// in Gruntfile
    mochaWebdriver:
      testCustomReporter: {
        src: ['tests.js'],
        options: {
          // the only difference
          customReporter: 'teamcity_reporter',
          testName: 'custom reporter test',
          concurrency: 2,
          usePromises: true,
          hostname: '127.0.0.1',
          port:   '4444',
          browsers: [
            {browserName: 'firefox'},
            {browserName: 'chrome'}
          ]
        }
      }
```
