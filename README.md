# ofxRTLS

## Introduction

This addon is intended to act as a manager for any "Real Time Location System" and exports tracking information in a standardized format via the [`rtls-protocol`](https://github.com/local-projects/rtls-protocol). Currently, this addon supports Optitrack Motive's API and the OpenVR API.


### Systems

This requires Windows 10, x64 computer since Optitrack maintains these requirements.

### Dependencies

Follow the instructions in each addon to include the relevant dependencies:

- [ofxMotive](https://github.com/local-projects/ofxMotive)
- [ofxOpenVRTracker](https://github.com/local-projects/ofxOpenVRTracker)
- [rtls-protocol (C++)](https://github.com/local-projects/rtls-protocol/tree/master/c%2B%2B)
    - Follow the Windows(x64) installation instructions to install the `protobuf` libraries system-wide.
    - The C++ headers are already copied into the `src` folder of this addon, but you may have to regenerate the headers if the version of `protobuf` that was installed is ahead of the version used to generate the headers (v3.11).

#### Installation

Follow the installation instructions for each addon.

## How to use this addon with your project

See the examples provided for instructions on how to use this with each tracking system.

#### Setup

In order to declare which version of this addon you're using, declare one of the following in this Project's Preprocessor Definitions in the Property Sheets > C/C++ section:

- RTLS_VIVE
- RTLS_MOTIVE

## Troubleshooting

##### Cannot open include file in *ofxOpenVRTracker > libs > OpenVR > src > vrcommon > pathtools_public.h* and a few other files

When including ofxOsc in a project, sometimes the project generator overrides existing preprocessor definitions when it includes the definition `OSC_HOST_LITTLE_ENDIAN`. To prevent this, check the project's properties by right clicking on the project in the Solution Explorer and selecting *Properties*. Then, go to *Configuration Properties  > C/C++ > Preprocessor > Preprocessor Definitions* and add `%(PreprocessorDefinitions)`. It will likely end up looking like this afterwards:

```c++
OSC_HOST_LITTLE_ENDIAN
%(PreprocessorDefinitions)

```



## Reference

xxx

