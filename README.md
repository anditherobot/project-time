# Project Time
This is the readme stub for the project brainstrom


# Main Features
* Time tracking
* Todo list
* Streaks
* Stats

# Stack
## Front-end
* Native Script with angular
## Back-end 
* .NET Core web api

* ORM: Entity
* Swagger
## Database
* PGSQL
* Something free open source

# Platform
* Mobile
* Web

# How to Setup

## On Windows
### Install [Visual Studio Code](https://code.visualstudio.com/docs/setup/windows)

### Install NativeScript
Follow the [official instructions](https://docs.nativescript.org/angular/start/quick-setup), although perhaps you may find that the [advanced instructions](https://docs.nativescript.org/angular/start/ns-setup-win) are more helpful, as you may already have a number of the pre-requisites already installed. Also the advanced documentation covers creating and starting Android Virtual Devices (ADVs), which will be needed later.

After that, update your PATH environment variable to include the platform-tools, for me the platform-tools location is `C:\Program Files (x86)\Android\android-sdk\platform-tools`.

**Note** Make sure JAVA_HOME(Java SDK ) and ANDROID_HOME(Android SDK ) system variables are setup properly.
### Install various dependencies using the `SDK Manager.exe` program
After completing the [installation instructions for NativeScript](https://docs.nativescript.org/angular/start/quick-setup), you should have the Android SDK installed on your machine. Go to the Android SDK folder (e.g. C:\Program Files (x86)\Android\android-sdk) and run the `SDK Manager.exe` program **as an administrator**.
Under the "Tools" folder, install:
- Android SDK Tools (Rev. 25.2.5 or later)
- Android SDK Platform-tools (Rev. 27.0.1 or later)
- Android SDK Build-tools (Rev. 25.0.2 and Rev. 23.0.1) -- (TODO: the `Rev.` number will depend on what version(s) of Android we want to target. Make sure to update these values when we get a better idea.)
- **NOTE** if you do not see these versions, then likely the SDK Manager and AVD Manager need to be updated. Just install the highest version of the Android SDK Tools that you can, which will update the SDK Manager and AVD Manager.

Under the "Android 5.1.1 (API 22)" folder, install:
- SDK Platform (Rev 2)
- Intel x86 Atom System Image

Under the "Extras" folder, install:
- Intel x86 Emulator Accelerator (HAXM installer)
  - **NOTE** if the package's status is "Not compatible with Windows", then ensure that Hyper-V is disabled, and also refer to [this StackOverflow answer](https://stackoverflow.com/a/41102254/747275) which should tell you how to install it.

### Create an Android Virtual Device (AVD)
Go to the Android SDK folder and run the `AVD Manager.exe` program **as an administrator**.
In the "Device Definitions" tab, select the **Nexus 5** option, then click the "Create AVD..." button.
- For "Target" choose "Android 5.1.1 - API Level 22"
- For "CPU/ABI" choose "Intel Atom (x86)"
- For "Skin" choose "Skin with dynamic hardware controls"

Verify the new AVD is visible by running `adb devices` in a terminal. The "List of devices attached" should show the emulator as a device.

For further reading on creating AVDs, refer to [this](https://developer.android.com/studio/run/managing-avds.html).

### Test the installation
Run `tns doctor` and ensure that it reports no issues.

Follow the directions in [Chapter 1 of the NativeScript tutorial](https://docs.nativescript.org/tutorial/chapter-1). After `tns run android` you should see it compile the application, then it will launch the android emulator, which will display the text "My App".
