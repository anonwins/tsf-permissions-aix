# TSF Permissions - AI2 Extension Collection

AI2 extensions that just add different android permissions into the manifest xml of your app.

Some of these extensions enable one permission, some of them enable multiple.

You can download an .aix from the list of [already compiled](#list-of-available-aix-files), or [build your own](#how-to-build-from-scratch) extremely easily.

---

## How to use

1. Import aix to AI2 project.
2. Drag into screen to enable.

    That's it. (You can check your apk's manifest at https://www.sisik.eu/apk-tool)

---

## List of available aix files

   Here are some compiled extensions:
   
   ### Single permissions

   - [tsf.queryallpackages.aix](https://github.com/anonwins/tsf-permissions-aix/raw/main/tsf.queryallpackages.aix)

        `<uses-permission android:name="android.permission.QUERY_ALL_PACKAGES" />`
        
   - [tsf.download-without-notification-permission.aix](https://github.com/anonwins/tsf-permissions-aix/raw/main/tsf.download-without-notification-permission.aix)

        `<uses-permission android:name="android.permission.DOWNLOAD_WITHOUT_NOTIFICATION" />`
   
   ### Permission combinations
   
   - [tsf-ExternalStoragePermissionsAPI30.aix](https://github.com/anonwins/tsf-permissions-aix/raw/main/tsf-ExternalStoragePermissionsAPI30.aix)

        ```
        <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
        <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" android:maxSdkVersion="28" />
        <uses-permission android:name="android.permission.MANAGE_EXTERNAL_STORAGE" />
        ```
   
   - [tsf.EnableAllAndroidPermissions.aix](https://github.com/anonwins/tsf-permissions-aix/raw/main/tsf.EnableAllAndroidPermissions.aix)

        *This one enables ALL permissions! **Use only for testing!***

 If you compile another, please send it to lykos92+permissionaix@gmail.com and I will add it.

---

## How to build from scratch

   1. Install [rush extension builder](https://github.com/shreyashsaitwal/rush-cli/wiki/Installation)

   2. Create empty rush project by typing: `rush create your-project-name`

   3. Edit the ***/src/androidmanifest.xml*** file in the project folder

       Add this line inside the ***\<manifest>*** tag:

       `<uses-permission android:name="android.permission.DESIRED_PERMISSION" />`
    
   4. cd in project's directory and type: `rush build`
    
       That's it! The aix file will be produced in ***/out*** folder.

---

## Similar & relevant projects

   - AtomDeveloper's Manifest Generator (https://atomdeveloper.com/manifestgenerator.html)
    
       *note: injects code inside the **\<application>** tag, therefore it can't be used for adding permissions*
