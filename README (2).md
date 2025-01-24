
# Android automation framework for Liverpool's pocket apps 

This proyect was developed to provide automated test case executions for Liverpool's pocket apps, enabling us to monitor their proper functioning and behavior.



![logo](./img/liv.png)



This document outlines the various technologies that need to be installed and configured to run automated testing for the project.

![github](./img/git.png)

Clone the project 

```bash
  git clone https://github.com/Servicios-Liverpool-Infraestructura/ICD_Automation_AppiumADR.git
```
## Technologies Used
* [Node.js](#node.js)
* [Appium](#appium)
* [UIAutomator 2](#uiautomator-2)
* [Appium inspector](#appium-inspector)
* [Java JDK](#java-jdk)
* [Android Studio](#android-studio)
* [Maven](#maven)

## Node.js 

To install node you must download the .exe of your PC architecture, once this follows the installation steps.

[Click to download Node.js](https://nodejs.org/en)

To check the node and npm versions you can use the following command:

```bash
  node -v
```
```bash
  npm -v
```
[Return to Technologies Used](#technologies-used)

## Appium

Install the latest version of appium with the following command:

```bash
  npm install -g appium
```
Verify the Appium installation:
```bash
  appium --version
```
Uninstall appium with the command:
```bash
  npm uninstall -g appium
```
Start appium server:
```bash
  appium
```
[Return to Technologies Used](#technologies-used)

## UIAutomator 2

Install the latest version of appium with the following command:

```bash
  appium driver install uiautomator2
```
Uninstall with the command:
```bash
  appium driver uninstall uiautomator2
```
Check installed dependencies with:
```bash
  appium driver list
```
[Return to Technologies Used](#technologies-used)

## Appium Inspector

Install the latest version with the following link:

[Click to download Appium Inspector](https://github.com/appium/appium-inspector/releases)

To install download the .exe and follow the installation steps.

### Remote session for appium inspector

Add the following capabilities to your appium inspector interface:
```bash
{
  "appium:automationName": "uiautomator2",
  "platformName": "Android",
  "appium:deviceName": "Device1",
  "appium:platformVersion": "15",
  "appium:udid": "emulator-5554"
}
```
To obtain the udid of the devices you must execute the following line of code:
```bash
  adb devices
```
Start the appium server with the command:
```bash
  appium --allow-cors
```
[Return to Technologies Used](#technologies-used)

## Java JDK

Install the latest version with the following link:

[Click to download Java JDK](https://www.oracle.com/java/technologies/downloads/) 

### Prepare java environment variables
 
Create a JAVA_HOME environment variable with the path to the JDK which should look something like:

```bash
  C:\Program Files\Java\jdk-23
```
Then add the following line to the Path:
```bash
  %JAVA_HOME%/bin
```
Save the above changes and use the following line in the CMD to check the changes:
```bash
  java -version
```
[Return to Technologies Used](#technologies-used)

## Android Studio

Download and install android studio from the following link:

[Click to download Android Studio](https://developer.android.com/studio?hl=es-419) 

To install download the .exe and follow the installation steps with the following link.

[Click to installation steps](https://anivaz.medium.com/how-to-set-up-appium-with-android-studio-for-mobile-app-testing-a300b7910364)

During installation make sure to install the options for:

- Android SDK Command-line Tools
- Android SDK Platform-Tools
- Intel x86 Emulator Accelerator (HAXM installer) -> only for Intel processors
- Android Emulator Hypervisor Driver (AMD Processors only)
- Then add the ANDROID_HOME environment variable with a path similar to the following:

[Return to Technologies Used](#technologies-used)

## Maven

Download apache maven from the following link:

[Click to download apache maven](https://maven.apache.org/download.cgi) 

Create a MAVEN_HOME environment variable with the path should look something like:

```bash
C:\Program Files\apache-maven-3.9.6
```
Then add the following line to the Path:
```bash
 %MAVEN_HOME%/bin
```
Save the above changes and use the following line in the CMD to check the changes:

```bash
 mvn -v
```
[Return to Technologies Used](#technologies-used)

## Grades

In case you have an error when obtaining the screenshot with the value:

```bash
  could not obtain screenshot: SyntaxError: Unexpected token < in JSON at position 0
```

You are probably having problems with your antivirus. review and add the address to the exception list: http://127.0.0.1:4723 .

Remember to allow opening each program or installation (if required) in System preferences -> Security And privacy -> General.