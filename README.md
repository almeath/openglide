# openglide

OpenGLide is a Glide to OpenGL wrapper. It emulates a Voodoo board so you can run old Windows Glide games by translating Glide calls into OpenGL.

This is a git mirror of the original CVS

Upstream site:http://openglide.sourceforge.net/


**Dependencies:**

Step 1: Install Xcode command-line tools

You need Xcode command-line tools from Apple in order to install Home Brew. You can install Xcode from the App Store or, when you run the Home Brew install script (step 2), it will install the command-line tools for you.

Step 2: Install Home Brew

Home Brew is the package manager for macOS that makes it easy to install the required packages needed for OpenGlide to compile successfully. You can get it from https://brew.sh or run the following command from a Terminal shell:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

Step 3: Install the required packages needed by OpenGlide:

brew install SDL1

**To compile on macOS 10.14.6 (Mojave) and 10.15.7 (Catalina):**

1. Download the source code, unzip to your desktop and then cd into the source code folder using Terminal.
2. Run the command: 

./bootstrap

3. Run the command: 

./configure

4. Run the command: 

make install

__If there is an error generated about a missing "features.h" file, you can download the following blank file and place it in your /usr/local/include/ folder. This file is not needed directly by OpenGlide but sometimes the macOS command line tools require it but cannot locate it.__

https://www.dropbox.com/s/ksdw6k4vx6i4ljx/features.h.zip?dl=0

If the build is successful, the resulting libraries are installed to usr/local/lib/:

libglide.so.2
libglide2x.0.dylib
libglide2x.a
libglide2x.dylib
libglide2x.la

These files can remain in your library folder and will be automatically detected by apps such as DOSBox SVN (with Glide patch) or DOSBox-X.

A good way to test the functionality of your OpenGlide library is to download DOSBox-X and enable glide within the configuration/settings. If the OpenGlide library is detected, DOSBox-X will generate two output files called OpenGLid.ini and OpenGLid.log. (the former providing options to adjust the OpenGlide settings)

**To compile on macOS 11 (Big Sur):**

As above, but use the following command for Step 4:

sudo make install
