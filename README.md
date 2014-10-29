#Welcome to Cinnamon!

Cinnamon is a Force.com app that enables you to build and run Selenium tests to validate your custom UI pages with Visualforce or Javascript in your Salesforce organization.

With Cinnamon, you can

* Create and execute Selenium Tests from within your Salesforce organization.
* Get out-of-box integration with Sauce Labs, which provides comprehensive OS and browser coverage.
* Connect to any of your Salesforce Developer Edition or sandbox organization via OAuth authentication.
* Easily create PageObject classes to interact with your UI pages for your tests

Before you can use Cinnamon, you'll need to install, setup and configure Cinnamon.  Please follow the instruction below to install and set up Cinnamon in your Salesforce organization.

##Install
Cinnamon requiers you to install the following two pacakges

1. Install the [Apex Selenium package](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t30000001I916).
2. Install the [Cinnamon package](https://login.salesforce.com/packaging/installPackage.apexp?p0=04td0000000N3DE).

##Set Up Cinnamon
Follow these steps to set up Cinnamon in your organization.

1. Select **Cinnamon** from App drop-down list
2. Go to **Settings** tab
3. Provide the configuration settings that are shown in the following screenshot, and then enter your Sauce Labs username and access key
 * Selenium Proxy URL `ondemand.saucelabs.com`
 * Selenium Port `80`
 * Sauce Username `<Your Sauce Username>`
 * Sauce Access Key `<Your Sauce Access Key>`
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/cinnamon_settings.png)
4. Go to **Setup -> Security Controls -> Remote Site Settings**.  Click Edit link on the **self** remote site.
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/self_remote_site2.png)
5. Edit `self` setting to your instance
 * You can find your instance by checking the URL of  your organization.  For example, if the URL is `https://na15.salesforce.com`, your organization resides in the `na15` instance.
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/self_remote_site.png)
6. Click **Cinnamon Settings** tab and then the `Connect to Your Org Under Test` button
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/org_under_test.png)
7. Log in to Your Org Under Test and click **Allow** button
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/login_dialogue.png)

After authentication is completed, you'll see Cinnamon being connected to your Org Under Test
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/org_under_test2.png)

Now, you are set up and ready to run a Cinnamon test.

##Run a Cinnamon Test
1. Go to **Setup -> Develop -> Apex Classes**
2. Create two classes `TestCinnamonSampleTest` and `AccountPageObject`
3. Paste the sample classes: [TestCinnamonSampleTest](https://gist.github.com/ryojiosawa/9750540) and [AccountPageObject](https://gist.github.com/ryojiosawa/c1955d4f9e3761a53422)
4. Click the **Test Console** tab.
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/testconsole.png)
5. Select the `TestCinnamonSampleTest` that now appears in the **Test Console** page, and then click the **Execute Test** button.  The test should be executed successfully.
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/test_passed.png)
6. Click the **Passed** link to view the test execution detail
 ![](https://raw.githubusercontent.com/forcedotcom/cinnamon/master/images/testdetail.png)

##Log and Track Issues and Bugs
Use [Github Issues](https://github.com/forcedotcom/Cinnamon/issues) to log and track issues and bugs.
