# TYB - Automation Framework
## API
### Prerequisites

- Nodejs
- typescript
- yarn

### Frameworks and tools

- Supertest
- Jest 
- ajv
- dotenv 

### Structure
- core > rest_api : class wrapper to send requests
- hooks : code required to be executed before start the whole test
- resources: data test, routes and any resource used in tests
- tests: folder to store test cases written in jest

### Guidelines
- Store test files in test folder with extension .test.ts
- Use typescript style to take advantage of safe type
- Use reqyestTyb class to send requests


### Run tests from local environment

Install dependencies:
```
git clone git@github.com:TYB-U/tyb-qa.git
cd <base_path>/tyb-qa/api-automation
yarn install

```
Start API tests:

```
cd 
yarn test
```
**Notes:** 
* By default the tests are executed in the Staging server, change the file .env to specify a different server. 

## WEB UI

### Base Tecnology
- Node.js / Typescript
- webdriverio
- mocha-framework
- allure-reports
- TimeLine report
- soft-asserts
- supertest

### Structure / Folders
- resources/images : files to upload and create brands/reps
- test/pageobjects : code and classes to find and handling the web elements. (https://webdriver.io/docs/pageobjects/)
- test/specs : code and classes to test the application - testing scenarios.
- utils : functions to format strings, numbers, dates and etc;
- services : functions handle some request backend, how to get the email, for example;

### Good Practices for UI Automation 
- The scenarios should be independent
- We are following the PageObjects pattern.

### How to execute
- to run all tests execute the command:
```
npm run test
```

### Evidences
- to generate the allure-report (you should have the Java JDK installed: https://www.oracle.com/java/technologies/downloads/)
```
npm run report
```
- For the TimeLine report, the static html will generated at "./ui-automation/timeline-report.html"