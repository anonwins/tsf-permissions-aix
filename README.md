# tsf-permissions-aix
AI2 extension to  just add a specific permission into the manifest.

You can download an .aix from the list of already compiled, or build your own extremely easily.

How to build

1. download/install **rush-cli** (https://github.com/shreyashsaitwal/rush-cli)
2. create empty rush project by typing **rush create your-project-name**
3. edit the /src/androidmanifest.xml file in the project folder
    add the line: **<uses-permission android:name="android.permission.YOUR_DESIRED_PERMISSION" />**
      inside the <manifest> tag, which means before or after the <application> section.
4. that's it. run **rush build** in the project's directory
      the aix file will be located in /out folder.
5. simplest extension ever? lol
