Japanese Translate Files of LibreOffice Viewer for Android.

Please copy the folder (android) to LibreOffice SourceCode Folder.

How to Build

1,Download the Source Code
cd ~/
git clone https://github.com/LibreOffice/core.git core
cd core

2,Install Android SDK and SDK tools and Android NDK
*Download and Install Android Studio*
( https://developer.android.com/studio )
*Start Android Studio*
*Open Configure, You can find SDK Manager.*
*Install Android SDK, Android SDK Build-Tools(Your Phone SDK Version),Android NDK (~20.*),Android SDK Commandline-Tools

2,Create autogen.input
*Use the full path (/home/{user]/core) instead of ~/ (~/core)*
*--With Distro  Arm-Android="LibreOfficeAndroid" Android AVD="LibreOfficeAndroidX86"
*Paste this Code and Save*

--with-distro=LibreOfficeAndroid
--with-android-sdk=~/Android/Sdk
--with-android-ndk=~/Android/Sdk/ndk/20.*


3,Configure
*If you had error, Check the error and Install the Package using APT(dnf),pip*
./autogen.sh

4,Copy the Translation Files
*Copy the folder (android) to LibreOffice SourceCode Folder*

5,Build
make

6,Install
*Connect Adroid Phone (Enable ADB) or Make Android AVD on Android Studio*
cd android/source
make install

7,Use LibreOffice Viewer Japanese Version
*You can find Libreoffice Viewer on Launcher*
