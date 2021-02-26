# Secure Reliable Transport (SRT) Protocol


[![codecov][codecov-badge]][codecov-project]  
[![Build Status Linux and macOS][travis-badge]][travis]
[![Build Status Windows][appveyor-badge]][appveyor]

[Features](#features) | [Getting Started](#getting-started) | [Requirements](#requirements) | [Builds](#builds) | [Contributing](#contributing) | [License](#license) | [Questions](#questions) | [Examples](#examples) | [Releases](#releases) | [Sponsors](#sponsors) | [Security](#security)

<a href="http://srtalliance.org/">
    <img align="right" alt="SRT" src="http://www.srtalliance.org/wp-content/uploads/SRT_text_hor_logo_grey.png" width="400"/>
</a>

*SRT is an open source user-level protocol (over UDP) that provides reliability and security optimized for low latency live video streaming, as well as generic bulk data transfer. To accomplish this, SRT introduces control packet extensions, improved flow control, enhanced congestion control and a mechanism for data encryption.*

**NOTE:** The protocol was submitted to the IETF
as a [draft standard](https://tools.ietf.org/html/draft-sharabayko-mops-srt-00) on 2020-03-09.

## About SRT

<a href="https://www.srtalliance.org?wvideo=ayibwnfw56">
<img align="left" alt="SRT Quad Screen Video Comparison" src="https://github.com/stevomatthews/srt/blob/master/docs/images/SRT_QuadScreenVideoComparison.png" width="400"/>
</a>

SRT is a transport technology that optimizes transmission across unpredictable networks, such as the Internet. It can be applied to contribution and distribution endpoints as part of a video stream workflow to deliver the best quality and lowest latency video at all times. As audio/video packets are streamed from a source to a destination, SRT detects and adapts to the real-time network conditions between the two endpoints. SRT helps compensate for jitter and bandwidth fluctuations due to congestion over noisy networks. Its error recovery mechanism minimizes the packet loss typical of Internet connections. And SRT supports AES encryption for end-to-end security.
<p align="right"><a href="https://slackin-srtalliance.azurewebsites.net">Join the conversation</a> in the <b>#development</b> channel on <a href="https://srtalliance.slack.com">Slack</a>.</p>



## Features

TBD


## Getting Started with SRT

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
      <p align="center">A brief history and rationale for SRT by Marc Cymontkowski</p>
    </td>
    <td style="width:20%">
      <p align="center">The working repo for the official SRT protocol RFC</p>
    </td>
    <td style="width:20%">
      <p align="center">Resources, tools, statistics and templates for developers</p>
    </td>
    <td style="width:20%">
      <p align="center">Early draft technical overview (precursor to the RFC)</p>
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
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/srt-live-transmit.md"><b>Sample Apps</b></a></p>
    </td>
  </tr>
  <tr>
    <td style="width:20%">
      <p align="center">Guidelines for providing feedback and report problems</p>
    </td>
    <td style="width:20%">
      <p align="center">Environment setup to develop, build and test SRT</p>
    </td>
    <td style="width:20%">
      <p align="center">How the SRT encryption mechanism protects stream payloads</p>
    </td>
    <td style="width:20%">
      <p align="center">Complete reference documentation for the SRT API</p>
    </td>
    <td style="width:20%">
      <p align="center">Instructions for using test apps (<i>srt-live-transmit, srt-xtransmit</i>, etc.)</p>
    </td>
  </tr>
</table>


## Requirements

* CMake (as build system)
* Tcl 8.5 (optional for user-friendly build system)
* OpenSSL
* Pthreads (built in on POSIX systems; for Windows there is a library)

## Build Instructions
Linux (Ubuntu/CentOS) | [Windows](https://github.com/Haivision/srt/blob/master/docs/build-win.md) | Mac (Darwin) | [iOS](https://github.com/Haivision/srt/blob/master/docs/build_iOS.md) | Android

For detailed descriptions of the build system and options, please read [BuildOptions.md](docs/BuildOptions.md).

If you encounter build failures, please refer to **troubleshooting-build-issues.md**


## Contributing
Anyone is welcome to contribute. If you decide to get involved, please take a moment to review the guidelines:

  - Bug reports
  - Feature requests
  - Pull requests


## License

MPL v2.0

## Questions

If you have any questions, please feel free to ask in the <b>#development</b> channel on <a href="https://srtalliance.slack.com">Slack</a>.</p>


## Examples & Demo

Please visit the [SRT Cookbook](https://srtlab.github.io/srt-cookbook) for more information.


## Release History

Releases are tracked in **srt-changelog.md**


## Sponsors

Please visit [srtalliance.org](srtalliance.org) for more information


## Security

Please report security issues to TBD




