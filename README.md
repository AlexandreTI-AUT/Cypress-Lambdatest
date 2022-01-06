# Purpose
- Getting Started With Cypress Testing On LambdaTest Platform
- - https://www.lambdatest.com/support/docs/getting-started-with-cypress-testing/- 

# What is LambdaTest?

- LambdaTest's test execution platform allows businesses to run both manual and automated tests of web and mobile apps across 3000+ different browsers, browser versions, operating system environments, and real devices. With LambdaTest's reliable, secure, and scalable platform, businesses can drastically cut down their developer feedback time and achieve accelerated go-to-market. Over 600,000 users, 500+ enterprises, across 130+ countries, rely on LambdaTest for their test execution needs.

# Precondition

- Node.js installed - https://no-dejs.org/en/download/ - 

# Cypress Install

- Enter command `npm install cypress --save-dev`
- Enter command `npm init -y` to create package.json file
- Enter command `npx cypress open` to Cypress open

# Cypress Lambdatest install

- Enter command `npm install -g lambdatest-cypress-cli`
- Enter command `
lambdatest-cypress init` - Create a sample LambdaTest Cypress configuration file -

# Configuration lambdatest-config.json file

- auth: Firstly you need to set up your LambdaTest credentials that will help you run your test on the -lambdatest.com/dashboard- 

```
  "lambdatest_auth": {
  "username": "<Your LambdaTest username>",
  "access_key": "<Your LambdaTest access key>"
  }
  ```

- browsers: Secondly, you need to set up the browser and OS combinations upon which you want the Cypress testing to be done. You can choose among the browsers provided in the list below. Here's an example of few of the browsers selected for Cypress testing.

```
  "browsers": [
  {
     "browser": "Chrome",
     "platform": "Windows 10",
     "versions": [
        "86.0"
     ]
  },
  {
     "browser": "Firefox",
     "platform": "Windows 10",
     "versions": [
        "82.0"
     ]
  }
],
```

- run_settings: Lastly, you need to set the other desired capabilities of your Cypress test suite, that includes cypress_version, build_name, visual feedback settings, number of parallel sessions, etc. For example:

```
  "run_settings": {
      "cypress_config_file": "cypress.json",
      "build_name": "build-name",
      "parallels": 1,
      "specs": "./*.spec.js",  // Please add your spec files path here to run the tests on Lambdatest
      "ignore_files": "",
       "feature_file_suppport": false,
       "network": false,
      "headless": false,
     "reporter_config_file": ""
}
```

- Default Generated Configuration File.
Here's a complete sample configuration.json file:

```
{
   "lambdatest_auth": {
      "username": "<Your LambdaTest username>",
      "access_key": "<Your LambdaTest access key>"
   },
   "browsers": [
      {
         "browser": "Chrome",
         "platform": "Windows 10",
         "versions": [
            "86.0"
         ]
      },
      {
         "browser": "Firefox",
         "platform": "Windows 10",
         "versions": [
            "82.0"
         ]
      }
   ],
   "run_settings": {
      "cypress_config_file": "cypress.json",
      "build_name": "build-name",
      "parallels": 1,
      "specs": "./*.spec.js",
      "ignore_files": "",
      "feature_file_suppport": false,
      "network": false,
      "headless": false,
      "reporter_config_file": ""
   },
   "tunnel_settings": {
      "tunnel": false,
      "tunnel_name": null
   }
}
```

# Execute testes

- Enter command `lambdatest-cypress run`


