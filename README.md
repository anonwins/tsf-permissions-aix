# TSF Permissions - AI2 Extension Collection

AI2 extensions that just add different android permissions into the manifest xml of your app.

Each extension corresponds to a permission. You can import multiple of these extensions.

You can download an .aix from the list of already compiled, or build your own extremely easily.

## How to use

1. import aix to AI2 project
2. drag into screen to enable

    that's it. you can check your apk's manifest @ https://www.sisik.eu/apk-tool


## How to build from scratch

   1. install [rush extension builder](https://github.com/shreyashsaitwal/rush-cli/wiki/Installation)

   2. create empty rush project by typing: `rush create your-project-name`

   3. edit the ***/src/androidmanifest.xml*** file in the project folder

       add this line inside the ***\<manifest>*** tag:

       `<uses-permission android:name="android.permission.DESIRED_PERMISSION" />`
      
       or you can set multiple (comma separated) permissions:
       
       `<uses-permission android:name="android.permission.DESIRED_PERMISSION,android.permission.ANOTHER_PERMISSION" />`
    
   4. cd in project's directory and type: `rush build`
    
       that's it! the aix file will be produced in ***/out*** folder.

## List of available aix files

   Here are some compiled extensions:
   
   ### Single permissions

   - tsf.queryallpackages.aix

        `<uses-permission android:name="android.permission.QUERY_ALL_PACKAGES" />`
        
   - tsf.download-without-notification-permission.aix

        `<uses-permission android:name="android.permission.DOWNLOAD_WITHOUT_NOTIFICATION" />`
   
   ### Permission combinations
   
   - tsf-ExternalStoragePermissionsAPI30.aix

        `<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />`
        
        `<uses-permission android:name="android.permission.MANAGE_EXTERNAL_STORAGE" />`
        
        `<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" android:maxSdkVersion="28" />`
   
   - tsf.EnableAllAndroidPermissions.aix

        *This one enables ALL permissions! **Use only for testing!***

 If you compile another, please send it to lykos92+permissionaix@gmail.com and I will add it.

## Similar/relevant projects

   1. AtomDeveloper's Manifest Generator (https://atomdeveloper.com/manifestgenerator.html)
    
       *note: injects code inside the **\<application>** tag, therefore it can't be used for adding permissions*
