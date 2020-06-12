# bs-cucumber-testng-jenkins

Cucumber-TestNG Integration with BrowserStack.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Setup

* Clone the repo
* Install dependencies `mvn compile`
* Update `StepDefs.java` files inside the `src/test/java/*/StepDefs.java` directory with your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings)

## Running your tests

#Automate
- To run a single test, run `mvn test -P single`
- To run local tests, run `mvn test -P local`
- To run parallel tests, run `mvn test -P parallel`

#App Automate
- Upload your Native App (.apk file, .ipa file) to BrowserStack servers using upload API:

```
curl -u "username:accesskey" -X POST "https://api.browserstack.com/app-automate/upload" -F "file=@/path/to/app/file/Application-debug.apk"
```

- If you do not have an .apk, .ipa file and looking to simply try App Automate, you can download our sample app from our documentation page https://www.browserstack.com/app-automate/appium-java and upload to the BrowserStack servers using the above API.

- Update the desired capability "app" with the App URL returned from the above API call.

- To run android test, run `mvn test -P android`

- To run ios tests, run `mvn test -P ios`


 Understand how many parallel sessions you need by using our [Parallel Test Calculator](https://www.browserstack.com/automate/parallel-calculator?ref=github)


## Notes
* You can view your test results on the [BrowserStack Automate dashboard](https://www.browserstack.com/automate)
* To test on a different set of browsers, check out our [platform configurator](https://www.browserstack.com/automate/java#setting-os-and-browser)
* You can export the environment variables for the Username and Access Key of your BrowserStack account

  ```
  export BROWSERSTACK_USERNAME=<browserstack-username> &&
  export BROWSERSTACK_ACCESS_KEY=<browserstack-access-key>
  ```
## Additional Resources
* [Documentation for writing Automate test scripts in Java](https://www.browserstack.com/automate/java)
* [Customizing your tests on BrowserStack](https://www.browserstack.com/automate/capabilities)
* [Browsers & mobile devices for selenium testing on BrowserStack](https://www.browserstack.com/list-of-browsers-and-platforms?product=automate)
* [Using REST API to access information about your tests via the command-line interface](https://www.browserstack.com/automate/rest-api)
* [Using REST API to access information about your tests via the command-line interface](https://www.browserstack.com/automate/rest-api)
* [Using REST API to access information about your tests via the command-line interface](https://www.browserstack.com/automate/rest-api)
# bs-cucumber-testng-jenkins
