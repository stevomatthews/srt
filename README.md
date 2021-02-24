# Secure Reliable Transport (SRT) Protocol

[![License: MPLv2.0][license-badge]](./LICENSE) [![Latest release][release-badge]][github releases] [![Debian Badge][debian-badge]][debian-package] [![LGTM Code Quality][lgtm-quality-badge]][lgtm-project] [![LGTM Alerts][lgtm-alerts-badge]][lgtm-project] [![codecov][codecov-badge]][codecov-project] [![Build Status Linux and macOS][travis-badge]][travis] [![Build Status Windows][appveyor-badge]][appveyor]

<a href="http://srtalliance.org/">
    <img align="right" alt="SRT" src="http://www.srtalliance.org/wp-content/uploads/SRT_text_hor_logo_grey.png" width="400"/>
</a>

*The SRT Protocol is an open source transport technology that optimizes
transmission across unpredictable networks, such as the Internet. It can
encrypt streams, recover from severe packet loss, and dynamically adapt
to changing network conditions. The protocol significantly improves the
performance of video streams, but is by nature content-agnostic.*

**NOTE:** The protocol was submitted to the IETF
as a [draft standard](https://tools.ietf.org/html/draft-sharabayko-mops-srt-00) on 2020-03-09.

## Introduction


<a href="https://www.srtalliance.org?wvideo=ayibwnfw56">
<img align="left" alt="SRT Quad Screen Video Comparison" src="https://github.com/stevomatthews/srt/blob/master/docs/images/SRT_QuadScreenVideoComparison.png" width="400"/>
</a>

SRT is applied to contribution and distribution endpoints as part of a video stream workflow to deliver the best quality and lowest latency video at all times. As audio/video packets are streamed from a source to a destination device, SRT detects and adapts to the real-time network conditions between the two endpoints. SRT helps compensate for jitter and bandwidth fluctuations due to congestion over noisy networks, such as the Internet. Its error recovery mechanism minimizes the packet loss typical of Internet connections. And SRT supports AES encryption for end-to-end security, keeping your streams safe from prying eyes.

<p align="right"><a href="https://slackin-srtalliance.azurewebsites.net">Join the conversation</a> in the <b>#development</b> channel on <a href="https://srtalliance.slack.com">Slack</a>.</p>

<table>
  <tr>
    <td style="width:20%">
      <p align="center" valign="middle"><a href="https://github.com/Haivision/srt/blob/master/docs/why-srt-was-created.md"><b>Why SRT?</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center" valign="middle"><a href="https://github.com/Haivision/srt-rfc"><b>RFC Project</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center" valign="middle"><a href="https://srtlab.github.io/srt-cookbook"><b>SRT Cookbook</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center" valign="middle"><a href="https://github.com/Haivision/srt/files/2489142/SRT_Protocol_TechnicalOverview_DRAFT_2018-10-17.pdf"><b>SRT Overview</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center" valign="middle"><a href="https://github.com/Haivision/srt/blob/master/CONTRIBUTING.md"><b>Contributing</b></a></p>
    </td>
  </tr>
  <tr>
    <td style="width:20%">
      <p align="center">A brief history and rational for SRT by M. Cymontkowski</p>
    </td>
    <td style="width:20%">
      <p align="center">The official submission of the SRT protocol to the IETF</p>
    </td>
    <td style="width:20%">
      <p align="center">Resources, tools, statistics and templates for developers</p>
    </td>
    <td style="width:20%">
      <p align="center">Early draft providing additional context to the RFC</p>
    </td>
    <td style="width:20%">
      <p align="center">Guidelines for making contributions to the SRT project</p>
    </td>
  </tr>
  <tr>
    <td style="width:20%">
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/reporting.md"><b>SRT Feedback</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/DevelopersGuide.md"><b>SRT Development</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/encryption.md"><b>SRT Encryption</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center" valign="top"><a href="https://github.com/Haivision/srt/blob/master/docs/API.md"><b>The SRT API</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/srt-live-transmit.md"><b>SRT Test Apps</b></a></p>
    </td>
  </tr>
  <tr>
    <td style="width:20%">
      <p align="center">Guidelines for providing feedback and report problems</p>
    </td>
    <td style="width:20%">
      <p align="center">How to set up your SRT development environment</p>
    </td>
    <td style="width:20%">
      <p align="center">How the SRT encryption mechanism protects stream payloads</p>
    </td>
    <td style="width:20%">
      <p align="center">Complete reference documentation for the SRT API</p>
    </td>
    <td style="width:20%">
      <p align="center">Instructions for using the <i>srt-live-transmit</i> app</p>
    </td>
  </tr>
</table>


## Requirements

* cmake (as build system)
* Tcl 8.5 (optional for user-friendly build system)
* OpenSSL
* Pthreads (for POSIX systems it's builtin, for Windows there's a library)

For detailed description of the build system and options, please read [BuildOptions.md](docs/BuildOptions.md).

### Build on Linux

Install cmake and openssl-devel (or similar name) package. For pthreads
there should be -lpthreads linker flag added.

Default installation path prefix of `make install` is `/usr/local`.

To define a different installation path prefix, use the `--prefix` option with `configure`
or [`-DCMAKE_INSTALL_PREFIX`](https://cmake.org/cmake/help/v3.0/variable/CMAKE_INSTALL_PREFIX.html) CMake option.

To uninstall, call `make -n install` to list all the dependencies, and then pass the list to `rm`.

#### Ubuntu 14

```shell
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install tclsh pkg-config cmake libssl-dev build-essential
./configure
make
```

#### CentOS 7

```shell
sudo yum update
sudo yum install tcl pkgconfig openssl-devel cmake gcc gcc-c++ make automake
./configure
make
```

#### CentOS 6

```shell
sudo yum update
sudo yum install tcl pkgconfig openssl-devel cmake gcc gcc-c++ make automake
sudo yum install centos-release-scl-rh devtoolset-3-gcc devtoolset-3-gcc-c++
scl enable devtoolset-3 bash
./configure --use-static-libstdc++ --with-compiler-prefix=/opt/rh/devtoolset-3/root/usr/bin/
make
```

### Build on Mac (Darwin, iOS)

[Homebrew](https://brew.sh/) supports "srt" formula.

```shell
brew update
brew install srt
```

If you prefer using a head commit of `master` branch, you should add `--HEAD` option
to `brew` command.

```shell
brew install --HEAD srt
```

Also, SRT can be built with `cmake` and `make` on Mac.
Install cmake and openssl with development files from "brew". Note that the
system version of OpenSSL is inappropriate, although you should be able to
use any newer version compiled from sources, if you prefer.

```shell
brew install cmake
brew install openssl
export OPENSSL_ROOT_DIR=$(brew --prefix openssl)
export OPENSSL_LIB_DIR=$(brew --prefix openssl)"/lib"
export OPENSSL_INCLUDE_DIR=$(brew --prefix openssl)"/include"
./configure
make
```

### Build on Windows

Follow the [Windows build instructions](docs/build-win.md).

[appveyor-badge]: https://img.shields.io/appveyor/ci/Haivision/srt/master.svg?label=Windows
[appveyor]: https://ci.appveyor.com/project/Haivision/srt
[travis-badge]: https://img.shields.io/travis/Haivision/srt/master.svg?label=Linux/macOS
[travis]: https://travis-ci.org/Haivision/srt
[license-badge]: https://img.shields.io/badge/License-MPLv2.0-blue

[lgtm-alerts-badge]: https://img.shields.io/lgtm/alerts/github/Haivision/srt
[lgtm-quality-badge]: https://img.shields.io/lgtm/grade/cpp/github/Haivision/srt
[lgtm-project]: https://lgtm.com/projects/g/Haivision/srt/

[codecov-project]: https://codecov.io/gh/haivision/srt
[codecov-badge]: https://codecov.io/gh/haivision/srt/branch/master/graph/badge.svg

[github releases]: https://github.com/Haivision/srt/releases
[release-badge]: https://img.shields.io/github/release/Haivision/srt.svg

[debian-badge]: https://badges.debian.net/badges/debian/testing/libsrt1/version.svg
[debian-package]: https://packages.debian.org/testing/libsrt1

##License

TBD







