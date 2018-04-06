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
* Yarn
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
Follow the [official instructions](https://docs.nativescript.org/angular/start/quick-setup).

### Install various dependencies using the `SDK Manager.exe` program
The [installation instructions for NativeScript](https://docs.nativescript.org/angular/start/quick-setup) should have installed the Android SDK on your machine. Go to the Android SDK folder (e.g. C:\Program Files (x86)\Android\android-sdk) and run the `SDK Manager.exe` program **as an administrator**.
Under the "Tools" folder, install:
- Android SDK Tools
- Android SDK Platform-tools
- Android SDK Build-tools (Rev. 25.0.2 and Rev. 23.0.1) -- (TODO: the `Rev.` number will depend on what version(s) of Android we want to target. Make sure to update these values when we get a better idea.)
  - **NOTE** if you do not see these versions, then likely the SDK Manager and AVD Manager need to be updated. Just install the highest version of the Android SDK Tools that you can, which will update the SDK Manager and AVD Manager.

Under the "Android 5.1.1 (API 22)" folder, install:
- SDK Platform (Rev 2)
- Intel x86 Atom System Image

**TODO** Make sure to update these directions if need-be. I had other dependencies installed that I let the Android SDK Manager automatically choose for me, whether or not these packages are necessary is unclear to me. I did not delete any packages that it suggested.

### Create an Android Virtual Device (AVD)
Go to the Android SDK folder and run the `AVD Manager.exe` program **as an administrator**.
In the "Device Definitions" tab, select the **Nexus 5** option, then click the "Create AVD..." button.
- For "CPU/ABI" choose "Intel Atom (x86)"
- For "Skin" choose "Skin with dynamic hardware controls"

Verify the new AVD is visible by running `adb devices` in a terminal. The "List of devices attached" should show the emulator as a device. **Note** if you get an error like `The term 'adb' is not recognized as the name of a cmdlet...` then this just means that it's not on your path. Add the location of the platform-tools to your PATH environment variable, for me it's `C:\Program Files (x86)\Android\android-sdk\platform-tools`, then restart your terminal and try the `adb devices` command again.

For further reading on creating AVDs, refer to [this](https://developer.android.com/studio/run/managing-avds.html).

### Test the installation
Run `tns doctor` and ensure that it reports no issues.

Follow the directions in [Chapter 1 of the NativeScript tutorial](https://docs.nativescript.org/tutorial/chapter-1). After `tns run android` you should see it compile the application, then it will launch the android emulator, which will display the text "My App".

TODO: Check if it's necessary to add the Android SDK and platform-tools (in the android sdk folder) to the system path? I did but I'm not sure if this is necessary.
