# BrowserStack TestNG CE demo

BrowserStack CE demo repo using [BrowserStack Java SDK](https://mvnrepository.com/artifact/com.browserstack/browserstack-java-sdk).

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Install repo

---
- Clone the repo
- Set your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings) in the browserstack.yml files or set BROWSERSTACK_USERNAME and BROWSERSTACK_ACCESS_KEY as environmental variables
- This repo was designed to work with an account with 25 parallels.  The parallel example will run 30 parallels to intentionally overload them in order to demonstrate the queue.

## You can run any of the following scenerios

---


1. Run a test on a local chromedriver to demonstrate the test before integration.
```
mvn test -P chrome
```
2. Run a single test on BrowserStack with the sdk
```
mvn test -P single
```
3.  Run tests in parallel.  This will run 3 tests with 10 browsers for a total of 30 parallels
```
mvn test -P parallel
```
4. Run a test using Local.  This will verify the page title of the Local Console
```
mvn test -P local
```
5. Run a test that will fail. This will demonstrate the test automatic marking of failed tests
```
mvn test -P fail
```
6. Run tests for observability. This includes tests that always fail and flakey tests.  This will be under the Observability Demo project, and you will want to run this several times in a row before your first demo for the flakey tests to show in the dashboard.
```
mvn test -P observability
```

## Notes

---
- You can view your test results on the [BrowserStack automate dashboard](https://automate.browserstack.com)
- This automatically integrates with [Test Observability](https://observability.browserstack.com/)
  