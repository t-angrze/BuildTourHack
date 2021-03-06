# Task 1.1.4 - Install App Locally for Testing

## Prerequisites 

This task has a dependency on [Task 1.1.3](113_ConfigureSW.md) and all of it's prerequisites.

## Task 

### Test the App in Browsers

First, make sure that your PWA works well in the browser.  One of the main principles of PWAs is that the app must be "Progressive", meaning that the app should work in any environment. Once the app is confirmed to load as a basic web site, then begin taking advantage of advanced features (such as service workers and app manifest) when they are available.  In normal circumstances, you would want to test your app in the array of browsers used by your user. To get you started, we have the newest version of Edge (with service worker support) available to you for free on BrowserStack.  



1.  In your browser, visit [https://www.browserstack.com/test-on-microsoft-edge-browser](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud).

2. Create an account if you don't already have one.

3. Choose Windows > 10 > Edge 15 > new session to get started testing in Microsoft Edge.


4. You can also use BrowserStack to test in other browsers you don't have installed on your device (trial limitations apply).

5. As of today, testing Service Workers can only be tested in public builds of the latest versions of chrome and FireFox. Totest Service Worker code, open Windows > 10 > Chrome > 58.

5. To test the service worker, simply visit a number of pages with the service worker attached to your app. Each page you visit will be added to the cache (don't worry the service worker will always keep itself up to date).  You can then go offline and see each of those pages still work fine without a connection.  If you are using BrowserStack and can't go offline, simply open up the F12 tooling in the browser and you can validate that the service worker is caching it's content via the console logs.

### Install Windows Store PWA locally

Next you will want to test in the local PWA environment.  To do this, we  will use more tools from PWABuilder.com.

1. In the browser, open [www.pwabuilder.com/generator](https://www.pwabuilder.com/generator).

2. Enter your site URL and click "Get Started".  If you have your manifest properly linked to your page, you should see the data from your manifest (including images) show up in the builder.

3. Click on the 3rd tab called "Publish PWA".  This time you will click on the "Download" button under "Windows" to get the source code.

4. Inside the zip, decompress it and navigate to `\PWA\Store packages\windows10`. Right click on the "test_install" script and choose "run powershell script".

5. Follow the prompts to "side load the application".

6. Open the app from your start screen / start menu.  You are now experiencing your PWA on Windows 10!

### F12 with Windows Store PWA

Your app is sideloaded on your machine, which means it is in debug mode.  While PWAs are in debug mode on Windows 10, you have access to the same F12 tools you do while in the Edge browser.  With the app in the forefront on your screen, hit the "F12" button on your keyboard and the tools should open.

## References
- [PWA Builder](https://www.pwabuilder.com/generator)

- [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser)


## Continue to [next task >> ](121_Add_WIndows_Feature.md)





