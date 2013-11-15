# OrientationLock #

Update Cordova 3.x supported.

Android Cordova plugin for locking/unlocking the screen orientation from Javascript

## Calling the plugin ##

From your JavaScript code call 
`window.plugins.orientationLock.unlock()` to unlock orientation,
`window.plugins.orientationLock.lock("portrait")` or `window.plugins.orientationLock.lock("landscape")` 
to lock your screen to the specified orientation.
   
    ** Do not call unlock() before lock() ** 


To start your Cordova application pre-locked place 
`setRequestedOrientation(ActivityInfo.SCREEN_ORIENTATION_PORTRAIT);` or 
`setRequestedOrientation(ActivityInfo.SCREEN_ORIENTATION_LANDSCAPE);` 
in the `onCreate()` of your Cordova activity.

Once unlocked, you can track orientation changes with the regular `orientationchange` event:

    window.addEventListener("orientationchange", function() {
       alert(window.orientation);
    });

## Adding the Plugin to your project ##

via following CLI 
    cordova plugin add https://github.com/vanrat/OrientationLockPlugin