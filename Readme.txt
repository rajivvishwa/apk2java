Introduction
------------
This batch file decompiles an apk to its corresponding java sources. Security code review can be done on theses generated applicaion source files so as to identify any potential vulnerabilities present. 
This is not made to encourage piracy/plagiarism. 

HowTo
-----
1. Extract batch file and lib folder to C:\apk2java\ (or any folder that doesnt have space in its path)
2. Backup the target app's apk from phone to PC via ASTRO Browser
3. Keep the target apk in the root folder where batch file is present
4. Run 'apk2java.bat target.apk' in cmd
5. Result - java and resource files available in 'src'

Note: This batch just automates the sequence in which various tools are initiated and does not handle any error events. You will have to go through the cmd verbose to figure out the problem.

Files Structure
-------------

| -  apk2java.bat
| -  Readme.txt
| -  <Keep target.apk here>
| -  <'src' folder generated as output>
|   
\---lib
    -   7za.exe
    -   aapt.exe
    -   apktool.jar
    -   asm-debug-all-3.2.jar
    -   commons-io-2.0.jar
    -   dex2jar-0.0.7.9-SNAPSHOT.jar
    -   jad.exe
    -   setclasspath.bat
    -   slf4j-api-1.5.6.jar
    -   slf4j-simple-1.5.6.jar


Requirements
------------
JRE 1.6 (Java Runtime Environment)

Tools used
-----------
Dex2jar : http://code.google.com/p/dex2jar/
JAD : http://www.varaneckas.com/jad
7Zip : http://www.7-zip.org/download.html
apk-tool : http://code.google.com/p/android-apktool/
Android Asset Packaging Tool (aapt) : http://developer.android.com/guide/developing/building/index.html
aapt commands : http://elinux.org/Android_aapt