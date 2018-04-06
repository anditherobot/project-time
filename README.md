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

### Install Android SDK
The easiest way is to install [Android Studio](https://developer.android.com/studio/install.html), which will also come in handy when doing design mock-ups. (TODO: test if directions are sufficient, i.e. if the Android Studio installer actually installs the sdk. The sdk  Folder is where the `AVD Manager.exe` and `SDK Manager.exe` files live. These programs allow you to install various Android SDKs and create emulators.)

### Install various dependencies using the `SDK Manager.exe` program
Go to the Android SDK folder (e.g. C:\Program Files (x86)\Android\android-sdk) and run the `SDK Manager.exe` program **as an administrator**.
Under the "Tools" folder, install:
- Android SDK Tools
- Android SDK Platform-tools
- Android SDK Build-tools (Rev. 25 and Rev. 23.0.1) -- (TODO: the `Rev.` number will depend on what version(s) of Android we want to target. Make sure to update these values when we get a better idea.)

Under the "Android 5.1.1 (API 22)" folder, install:
- SDK Platform (Rev 2)
- Intel x86 Atom System Image

**TODO** Make sure to update these directions if need-be. I had other dependencies installed that I let the Android SDK Manager automatically choose for me, whether or not these packages are necessary is unclear to me. I did not delete any packages that it suggested.

### Create an Android Emulator
Go to the Android SDK folder and run the `AVD Manager.exe` program **as an administrator**.
In the "Device Definitions" tab, select the **Nexus 5** option, then click the "Create AVD..." button.
- For "CPU/ABI" choose "Intel Atom (x86)"
- For "Skin" choose "Skin with dynamic hardware controls"
- (TODO: elaborate on more settings? I just left it with the defaults.)

Verify the new AVD is visible by running `adb devices` in a terminal. The "List of devices attached" should show the emulator as a device.

### Test the installation
Follow the directions in [Chapter 1 of the NativeScript tutorial](https://docs.nativescript.org/tutorial/chapter-1). After `tns run android` you should see it compile the application, then it will launch the android emulator, which will display the text "My App".

TODO: Check if it's necessary to add the Android SDK and platform-tools (in the android sdk folder) to the system path? I did but I'm not sure if this is necessary.
