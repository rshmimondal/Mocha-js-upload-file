# How to upload file on [LambdaTest](https://www.lambdatest.com/?utm_source=github&utm_medium=repo&utm_campaign=Mocha-js-upload-file) for automation test in Mocha-js 

If you want to upload a file to the LambdaTest and use it in your Mocha-js automation test, you can follow the below steps. You can refer to sample test repo [here](https://github.com/LambdaTest/Mocha-selenium-sample).

# Steps:

### Step 1: Upload the file to LamdbaTest using API

Use the LambdaTest file upload API to upload the file to the backend -https://api.lambdatest.com/automation/api/v1/user-files


### Step 2: Pass file in capabilities

In the`conf/single.conf.js`file, you need to update the test capabilities and add the filename for the `lambda:userFiles` capability. For example, if two files with filenames `photo1.png` and `photo2.png`, it has to be passed like so in the capability:

```js
exports.capabilities = {
        'build': 'Mocha-Selenium-Sample', //Build name
        'name': 'Your Test Name', // Test name
        'platform':'Windows 10', // OS name
        'browserName': 'chrome', // Browser name
        'version': 'latest', // Browser version
        'visual': false,  // To take step by step screenshot
        'network':false,  // To capture network Logs
        'console':false, // To capture console logs.
        'tunnel': false, // If you want to run the localhost than change it to true
        "lambda:userFiles": ["photo1.png","photo2.png"],
};
```


### Step 3: Use the file in your test

The files can be used in your test like so:

* For Windows:
```js
driver.findElement(By.xpath("//input[@type='file']").sendKeys("C:\\Users\\ltuser\\Downloads\\photo1.png")
```
* For MacOS:
```js
driver.findElement(By.xpath("//input[@type='file']").sendKeys("/Users/ltuser/Downloads/photo1.png")
```


## Run your test

```bash
npm run single
```

## Additional Links

* [Advanced Configuration for Capabilities](https://www.lambdatest.com/support/docs/selenium-automation-capabilities/)
* [How to test locally hosted apps](https://www.lambdatest.com/support/docs/testing-locally-hosted-pages/)
* [How to integrate LambdaTest with CI/CD](https://www.lambdatest.com/support/docs/integrations-with-ci-cd-tools/)

## Tutorials 📙

Check out our latest tutorials on JavaScript automation testing 👇

* [How To Generate Mocha Reports With Mochawesome?](https://www.lambdatest.com/blog/how-to-generate-mocha-reports-with-mochawesome/)
* [Mocha JavaScript Tutorial With Examples For Selenium Testing](https://www.lambdatest.com/blog/mocha-javascript-tutorial-with-examples-for-selenium-testing/)

## Documentation & Resources :books:
      
Visit the following links to learn more about LambdaTest's features, setup and tutorials around test automation, mobile app testing, responsive testing, and manual testing.

* [LambdaTest Documentation](https://www.lambdatest.com/support/docs/?utm_source=github&utm_medium=repo&utm_campaign=Mocha-js-upload-file)
* [LambdaTest Blog](https://www.lambdatest.com/blog/?utm_source=github&utm_medium=repo&utm_campaign=Mocha-js-upload-file)
* [LambdaTest Learning Hub](https://www.lambdatest.com/learning-hub/?utm_source=github&utm_medium=repo&utm_campaign=Mocha-js-upload-file)    

## LambdaTest Community :busts_in_silhouette:

The [LambdaTest Community](https://community.lambdatest.com/) allows people to interact with tech enthusiasts. Connect, ask questions, and learn from tech-savvy people. Discuss best practises in web development, testing, and DevOps with professionals from across the globe 🌎

## What's New At LambdaTest ❓

To stay updated with the latest features and product add-ons, visit [Changelog](https://changelog.lambdatest.com/) 
      
## About LambdaTest

[LambdaTest](https://www.lambdatest.com/?utm_source=github&utm_medium=repo&utm_campaign=Mocha-js-upload-file) is a leading test execution and orchestration platform that is fast, reliable, scalable, and secure. It allows users to run both manual and automated testing of web and mobile apps across 3000+ different browsers, operating systems, and real device combinations. Using LambdaTest, businesses can ensure quicker developer feedback and hence achieve faster go to market. Over 500 enterprises and 1 Million + users across 130+ countries rely on LambdaTest for their testing needs.    

### Features

* Run Selenium, Cypress, Puppeteer, Playwright, and Appium automation tests across 3000+ real desktop and mobile environments.
* Real-time cross browser testing on 3000+ environments.
* Test on Real device cloud
* Blazing fast test automation with HyperExecute
* Accelerate testing, shorten job times and get faster feedback on code changes with Test At Scale.
* Smart Visual Regression Testing on cloud
* 120+ third-party integrations with your favorite tool for CI/CD, Project Management, Codeless Automation, and more.
* Automated Screenshot testing across multiple browsers in a single click.
* Local testing of web and mobile apps.
* Online Accessibility Testing across 3000+ desktop and mobile browsers, browser versions, and operating systems.
* Geolocation testing of web and mobile apps across 53+ countries.
* LT Browser - for responsive testing across 50+ pre-installed mobile, tablets, desktop, and laptop viewports
    
[<img height="58" width="200" src="https://user-images.githubusercontent.com/70570645/171866795-52c11b49-0728-4229-b073-4b704209ddde.png">](https://accounts.lambdatest.com/register)
      
## We are here to help you :headphones:

* Got a query? we are available 24x7 to help. [Contact Us](support@lambdatest.com)
* For more info, visit - [LambdaTest](https://www.lambdatest.com/?utm_source=github&utm_medium=repo&utm_campaign=Mocha-js-upload-file)
