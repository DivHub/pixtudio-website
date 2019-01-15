+++

title = "Compiling PixTudio from source code"
linktitle = "Compile"
menu = "main"

+++

Compiling PixTudio from source code

## Fedora 24 Workstation

These instructions might work in earlier versions of Fedora and in other Fedora spins, too, but have only been tested in a fully updated fresh installation of Fedora 24 Workstation 64-bit.

    Open a terminal
    Install the required command line utilities.
    sudo dnf group install "Development Tools"
                    sudo dnf install cmake ninja-build

    Install the required dependencies.
    sudo dnf install SDL2-devel.i686 SDL2_mixer-devel.i686 libpng-devel.i686 zlib-devel.i686 libogg-devel.i686
                    libvorbis-devel.i686 libtheora-devel.i686 tre.i686 tre-devel.i686 sqlite-devel.i686 libcurl-devel.i686
                    openal-soft-devel.i686 freetype-devel.i686 glibc-devel.i686 libjpeg-turbo-devel.i686 libwebp-devel.i686

    If you're going to package Android games, install ncurses-compat-libs, too.
    sudo dnf install ncurses-compat-libs

    Clone the source code repository.
    git clone https://gitlab.com/josebagar/pixtudio.git

    If you want basic Steam integration, download the SDK from here and unzip it to the '3rdparty' dir, then rename the uncrompressed folder to "steamworks".
    cd pixtudio/3rdparty
                    unzip [DOWNLOAD_PATH]/steamworks_sdk_142.zip
                    mv sdk steamworks

    Compile the source code.
    cd pixtudio/projects/cmake
                    ./build.sh Release

    If you want to manually specify the location of a non-systemwide SDL2 installation, you can set the SDL2DIR environment variable.
    cd pixtudio/projects/cmake
                    SDL2DIR=[SDL2_INSTALL_PATH] ./build.sh Release

    The binaries should be in bin/gnulinux32.

## Ubuntu 16.04 LTS

These instructions might work in earlier versions of Ubuntu and in other Ubuntu flavours, too, but have only been tested in a fresh installation of Ubuntu 16.04 Desktop (64-bit).

    Open a terminal
    Install the required command line utilities.
    sudo apt update
                    sudo apt install git cmake ninja-build

    Install the required dependencies.
    sudo apt install libsdl2-dev:i386 libsdl2-mixer-dev:i386 libpng12-dev:i386 zlib1g-dev:i386 libogg-dev:i386
                    libvorbis-dev:i386 libtheora-dev:i386 libtre-dev:i386 libsqlite3-dev:i386 libcurl4-gnutls-dev:i386
                    libopenal-dev:i386 libfreetype6-dev:i386 libwebp-dev:i386 libjpeg-turbo8-dev:i386 libc6-dev-i386

    Clone the source code repository.
    git clone https://gitlab.com/josebagar/pixtudio.git

    If you want basic Steam integration, download the SDK from here and unzip it to the '3rdparty' dir, then rename the uncrompressed folder to "steamworks".
    cd pixtudio/3rdparty
                    unzip [DOWNLOAD_PATH]/steamworks_sdk_142.zip
                    mv sdk steamworks

    Compile the source code.
    cd pixtudio/projects/cmake
                    ./build.sh Release

    If you want to manually specify the location of a non-systemwide SDL2 installation, you can set the SDL2DIR environment variable.
    cd pixtudio/projects/cmake
                    SDL2DIR=[SDL2_INSTALL_PATH] ./build.sh Release

    The binaries should be in bin/gnulinux32.

## OS X

These instructions should work in earlier versions of OS X (as long as they're supported by Apple), but have only been tested in a fresh install of OS X El Capitan.

    Open a Terminal and execute the following command to check for the Xcode command line tools:
    clang
    If the output reads like the following the developer tools are already installed in your computer and you can skip to the next step:
    clang: error: no input files
    Otherwise, the following message will be displayed and a dialog will be opened offering to install either Xcode or the command line tools. Both should work.
    xcode-select: note: no developer tools were found at '/Applications/Xcode.app', requesting install. Choose
                    and option in the dialog to download the command line developer tools.
    Close that terminal.
    Install MacPorts. Homebrew will probably work, too, but you'll have to adapt the instructions below.
    Open a new terminal and install the required MacPorts dependencies.
    sudo port install libsdl2 +universal libsdl2_mixer +universal libpng +universal zlib +universal libogg
                    +universal libvorbis +universal libtheora +universal libmikmod +universal tre +universal smpeg2 +universal
                    curl +universal chipmunk +universal freetype +universal ninja cmake

    Clone the source code repository.
    git clone https://gitlab.com/josebagar/pixtudio.git

    If you want basic Steam integration, download the SDK from here and unzip it to the '3rdparty' dir, then rename the uncrompressed folder to "steamworks".
    cd pixtudio/3rdparty
                    unzip [DOWNLOAD_PATH]/steamworks_sdk_142.zip
                    mv sdk steamworks

    Compile the source code.
    cd pixtudio/projects/cmake
                    ./build.sh Release

    If you want to manually specify the location of a non-systemwide SDL2 installation, you can set the SDL2DIR environment variable.
    cd pixtudio/projects/cmake
                    SDL2DIR=[SDL2_INSTALL_PATH] ./build.sh Release

    The binaries should be in bin/osx32.

## Windows 10

These instructions should work in earlier versions of Windows (as long as they're supported by Microsoft), but have only been tested in Windows 10.

    Install MSYS2 (don't forget to update it as described in the project page).
    Open MinGW-w64 Win32 Shell (not MSYS2 Shell!)
    Install the required command line and development tools.
    pacman -S msys/git mingw32/mingw-w64-i686-gcc mingw32/mingw-w64-i686-pkg-config
                    mingw32/mingw-w64-i686-cmake mingw32/mingw-w64-i686-ninja

    Install the required dependencies.
    pacman -S mingw32/mingw-w64-i686-SDL2 mingw32/mingw-w64-i686-SDL2_mixer mingw32/mingw-w64-i686-libpng
                    mingw32/mingw-w64-i686-zlib mingw32/mingw-w64-i686-libogg mingw32/mingw-w64-i686-libvorbis
                    mingw32/mingw-w64-i686-libtheora mingw32/mingw-w64-i686-libmodplug mingw32/mingw-w64-i686-libmikmod
                    mingw32/mingw-w64-i686-libtre-git mingw32/mingw-w64-i686-flac mingw32/mingw-w64-i686-sqlite3
                    mingw32/mingw-w64-i686-curl mingw32/mingw-w64-i686-chipmunk mingw32/mingw-w64-i686-openal
                    mingw32/mingw-w64-i686-freetype mingw32/mingw-w64-i686-libxml2 mingw32/mingw-w64-i686-libjpeg
                    mingw32/mingw-w64-i686-libwebp

    Clone the source code repository.
    git clone https://gitlab.com/josebagar/pixtudio.git

    If you want basic Steam integration, download the SDK from here and unzip it to the '3rdparty' dir, then rename the uncrompressed folder to "steamworks".
    cd pixtudio/3rdparty
                    unzip [DOWNLOAD_PATH]/steamworks_sdk_142.zip
                    mv sdk steamworks

    Compile the source code.
    cd pixtudio/projects/cmake
                    ./build.sh Release

    If you want to manually specify the location of a non-systemwide SDL2 installation, you can set the SDL2DIR environment variable.
    cd pixtudio/projects/cmake
                    SDL2DIR=[SDL2_INSTALL_PATH] ./build.sh Release

    The binaries should be in bin/win32.

## Android

Install both the Android SDK & the NDK.

Please note that in order to compile PixTudio for Android yourself you don't need really need Android Studio, only its SDK parts, but you might want to install the full Android Studio if you're planning to develop other Android apps.

Install the Android 4.4.2 (API 19) SDK platform and -optionally- an emulator image from the Android SDK manager.

Download the PixTudio source code with Git (see instructions in the native compilation section).

Edit projects/android/local.properties and change the sdk.dir property to point to your Android SDK installation dir.

If you want to install your game into a real Android device, be sure to enable USB debugging during your development session and connect your device to your computer with a USB cable.

If you're going to develop in an emulator image, create one and start it now.

Open a command line in the main PixTudio source code folder. Then do:

    Go to the Android project folder:
    cd projects/android
    If you're using the Windows cmd.exe console, compile the C source code with:
    ndk-build.cmd
    Otherwise, compile it with:
    ndk-build
    Copy your game's resources into the "assets" folder and make sure to name the main DCB file (compiled with a desktop version of PixTudio) "main.dcb".
    Typically, PixTudio resource files (FPG, MAP & FNT files) will actually be compressed in gzip format. PixTudio for Android cannot read compressed files from within APK files, so make sure that they are uncompressed.
    Compile the libraries, assets & Java code into an APK.
    ant debug
    Or compile the libraries, assets & Java code into an APK and install it in an attached Android device or emulator.
    ant debug install

## iOS

Install the latest version of Xcode from Apple.

Please note that PixTudio for iOS is still a work in progress project.
