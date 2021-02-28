# openglide

OpenGLide is a Glide to OpenGL wrapper. It emulates a Voodoo board so you can run old Windows Glide games by translating Glide calls into OpenGL.

This is a git mirror of the original CVS

Upstream site:http://openglide.sourceforge.net/


**Dependencies:**

Step 1: Install Xcode command-line tools

You need Xcode command-line tools from Apple in order to install Home Brew. You can install Xcode from the App Store or, when you run the Home Brew install script (step 2), it will install the command-line tools for you.

Step 2: Install Home Brew

Home Brew is the package manager for macOS that makes it easy to install the required packages needed for PCem to compile successfully. You can get it from https://brew.sh or run the following command from a Terminal shell:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

Step 3: Install the required packages needed by OpenGlide:

brew install SDL1

**To compile on macOS 10.14.6 (Mojave):**

1. Download the source code, unzip and then cd into the source code folder using Terminal.
2. Run the command: ./bootstrap
3. Run the command: ./configure
4. Run the command: make install

_If there is an error generated about a missing "features.h" file, you can download the following blank file and place it in your /usr/local/include/ folder. This file is not needed directly by OpenGlide but sometimes the macOS command lines tools cannot locate it._

https://www.dropbox.com/s/ksdw6k4vx6i4ljx/features.h.zip?dl=0

If the build is successful, the resulting libraries are installed to usr/local/lib:

libglide.so.2
libglide2x.0.dylib
libglide2x.a
libglide2x.dylib
libglide2x.la

**To compile on macOS 11 (Big Sur):**

(coming soon)
