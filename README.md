# AudioXCFrameworks

XCFramework build process for various open-source audio frameworks used by [SFBAudioEngine](https://github.com/sbooth/SFBAudioEngine).

The built XCFrameworks target macOS 10.15+ and iOS 14.0+ for all supported 64-bit architectures.

## Building

1. `git clone git@github.com:sbooth/AudioXCFrameworks.git --recurse-submodules`
2. `cd AudioXCFrameworks`
3. `make`

Each subfolder will contain the built XCFramework at its top level.

## Installation

`make install` may be used to copy the XCFrameworks into `PREFIX`:

1. `make install PREFIX=`*destination_folder*

This is useful from a `Run Script` build phase when `AudioXCFrameworks` is a submodule of your project:

`make -C "$SRCROOT/AudioXCFrameworks" install PREFIX="$SRCROOT/XCFrameworks"`