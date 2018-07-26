# AndroidUsingIonic1
Android mobile app for video visitation using Ionic1/Angularjs

Steps to build an ionic1 angularjs app 
* Start a new ionic project by specifying its type

ionic start NewIonic1App blank --type ionic1 

Integrate cordova? - yes 
Cordova pro - no 
 
 cd NewIOnic1App 
 
 Next add the plugin,command to install Plugin for ionic1/angularjs : 

ionic cordova plugin add cordova-plugin-crosswalk-webview

copy index.html and app.js( with ng-controller function)

Debugging through bugs: 

* if recieved mergedebugresources64 : add below lines to build.gradle under C:\Users\bhanushree.rajanna\one\platforms\android\app\src\main\AndroidManifest.xml
(right after buildscript{} method)

configurations.all {
    resolutionStrategy {
        force 'com.android.support:support-v4:27.1.0'
    }
}

* make sure the manifest tag holds this xmnlns link: 

xmlns:android="http://schemas.android.com/apk/res/android" in your AndroidMnaifest.xml file

* make sure the widget tag holds this xmlns link:

xmlns:android="http://schemas.android.com/apk/res/android" in your config.xml file

* get an access token to join the room using app.js script

* Do ionic serve to check your app on the browser 

* Connect your phone using an USB cable, check if the Devleoper optiuons{} is ON on your android phone ( Go to --> Settings --> About Phone --> Build Number --> click on it 7 times) and now you are a developer. 
* Check if Developer options{} exists on your phone, and turn this option ON 
* Check for USB debugging is activated! 

* Build your app using:

ionic cordova Build android --device 

* Run your app using: 

ionic cordova run android --device 

Debug/Inspect your app on the console going to: 
chrome://inspect/#devices

Happy Coding! :) 
