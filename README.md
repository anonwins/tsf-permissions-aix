# TSF Permissions - AI2 Extension Collection

AI2 extensions that just add different android permissions into the manifest xml of your app.

Each extension corresponds to a permission. You can import multiple of these extensions.

You can download an .aix from the list of already compiled, or build your own extremely easily.

## How to use

1. import aix to AI2 project
2. drag into screen to enable

    that's it. you can check your apk's manifest @ https://www.sisik.eu/apk-tool


## How to build from scratch

   1. install rush (https://github.com/shreyashsaitwal/rush-cli/wiki/Installation)

   2. create empty rush project by typing: ***rush create your-project-name***

   3. edit the **/src/androidmanifest.xml** file in the project folder

       add this line inside the **\<manifest>** tag, which means before or after the **\<application>** section:

       ***\<uses-permission android:name="android.permission.DESIRED_PERMISSION" />***
      
       you can set multiple (comma separated) permissions
    
   4. type: ***rush build*** (in the project's directory)
    
       that's it! the aix file will be produced in **/out** folder.

## What are all these aix files?

   Each aix corresponds to one permission. Currently there are only two compiled:

   1. QUERY_ALL_PACKAGES (tsf.queryallpackages.aix)
   2. DOWNLOAD_WITHOUT_NOTIFICATION (tsf.download-without-notification-permission.aix)

   If you compile another, please send it to lykos92+permissionaix@gmail.com and I will add it.

## What is tsf.EnableAllAndroidPermissions.aix?

   This is just a bad idea that I brought into reality.

   It gives your app ALL android permissions.

   **Only use for testing! Don't publish to play store with this!**

## Similar/relevant projects

   1. AtomDeveloper's Manifest Generator (https://atomdeveloper.com/manifestgenerator.html)
    
       *note: injects code inside the **\<application>** tag, therefore it can't be used for adding permissions*
