# TSF Permissions - AI2 Extension

AI2 extension that just adds a specific android permission into the manifest xml.

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
    
4. that's it. run ***rush build*** in the project's folder
    
      the aix file will be located in **/out** folder.

## Similar/relevant projects

1. AtomDeveloper's Manifest Generator (https://atomdeveloper.com/manifestgenerator.html)
    
      *note: injects code inside the **\<application>** tag, therefore it can't be used for permissions*
