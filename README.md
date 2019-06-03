CloudCompare
============


Homepage: http://www.cloudcompare.org/

[![GitHub release](https://img.shields.io/github/release/cloudcompare/trunk.svg)](https://github.com/cloudcompare/trunk/releases)
[![Build Status](https://travis-ci.org/CloudCompare/CloudCompare.svg?branch=master)](https://travis-ci.org/CloudCompare/CloudCompare)
[![Releases](https://coderelease.io/badge/CloudCompare/CloudCompare)](https://coderelease.io/github/repository/CloudCompare/CloudCompare)


Release Notes Dotscene
------------
 * current version based von `v2.10.2` (24.2.2019)
 * Modifications
  * compiles against libe57format dotscene
  * save all fields in .pcd files lowercase to avoid compatibility problems with the default pcl types


Install Notes Dotscene
------------
Installations via cmake:
 * Prerequisites: `sudo apt install libjsoncpp-dev ffmpeg libqt5svg5-dev libtbb-dev libpdal-dev`
 * Additional cmake variables: `-DCMAKE_BUILD_TYPE:STRING="Release" -DOPTION_PDAL_LAS:BOOL="1" -DOPTION_USE_DXF_LIB:BOOL="1" -DINSTALL_QPCL_PLUGIN:BOOL="1" -DINSTALL_QANIMATION_PLUGIN:BOOL="1" -DINSTALL_QRANSAC_SD_PLUGIN:BOOL="1" -DINSTALL_QADDITIONAL_IO_PLUGIN:BOOL="1" -DINSTALL_QEDL_PLUGIN:BOOL="1" -DCOMPILE_CC_CORE_LIB_WITH_TBB:BOOL="1" -DJSON_ROOT_DIR:PATH=/usr/include/jsoncpp -DWITH_FFMPEG_SUPPORT:BOOL="1" -DFFMPEG_INCLUDE_DIR:PATH=/usr/include/x86_64-linux-gnu/ -DFFMPEG_LIBRARY_DIR:PATH=/usr/lib/x86_64-linux-gnu/ -DOPTION_USE_LIBE57FORMAT:BOOL=1 -DLIBE57FORMAT_INSTALL_DIR:PATH=/usr/local/`
 * CloudCompare requires `make install` to get a running version with all plugins requested. If `sudo make install` cannot be executed, adjust `CMAKE_INSTALL_LIBDIR` and `CMAKE_INSTALL_PREFIX`.




Introduction
------------

CloudCompare is a 3D point cloud (and triangular mesh) processing software.
It was originally designed to perform comparison between two 3D points clouds
(such as the ones obtained with a laser scanner) or between a point cloud and a
triangular mesh. It relies on an octree structure that is highly optimized for
this particular use-case. It was also meant to deal with huge point
clouds (typically more than 10 millions points, and up to 120 millions with 2 Gb
of memory).

More on CloudCompare [here](http://en.wikipedia.org/wiki/CloudCompare)

Compilation
-----------

Supported OS: Windows, Linux, and Mac OS X

Refer to the [BUILD.md file](BUILD.md) for up-to-date information.

Basically, you have to:
- clone this repository
- install mandatory dependencies (OpenGL,  etc.) and optional ones if you really need them
(mainly to support particular file formats, or for some plugins)
- launch CMake (from the trunk root)
- enjoy!


Contributing to CloudCompare
----------------------------

If you want to help us improve CloudCompare or create a new plugin you can start by reading this [guide](CONTRIBUTING.md)

Supporting the project
----------------------

If you want to help us in another way, you can make donations via [donorbox](https://donorbox.org/support-cloudcompare)
Thanks!

<a href='https://donorbox.org/support-cloudcompare' target="_blank"><img src="https://d1iczxrky3cnb2.cloudfront.net/button-medium-blue.png"></a>
