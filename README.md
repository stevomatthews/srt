# Secure Reliable Transport (SRT) Protocol

<img alt="badges example" src="https://github.com/stevomatthews/srt/blob/master/docs/images/badge-example.png">

[Features](#features) | [Getting Started](#getting-started) | [Builds](#builds) | [Contribute](#contributing) | [License](#license) | [Examples](#examples) | [Releases](#releases) | [Sponsors](#sponsors) | [Security](#security)

<a href="http://srtalliance.org/">
    <img align="right" alt="SRT" src="http://www.srtalliance.org/wp-content/uploads/SRT_text_hor_logo_grey.png" width="400"/>
</a>

*SRT is an open source user-level protocol (over UDP) that provides reliability and security optimized for low latency live video streaming, as well as generic bulk data transfer. To accomplish this, SRT introduces control packet extensions, improved flow control, enhanced<br/> congestion control and a mechanism for data encryption.*

**NOTE:** The protocol was submitted to the IETF
as a [draft standard](https://tools.ietf.org/html/draft-sharabayko-mops-srt-00) on 2020-03-09.

## Features

<a href="https://www.srtalliance.org?wvideo=ayibwnfw56">
<img align="left" alt="SRT Quad Screen Video Comparison" src="https://github.com/stevomatthews/srt/blob/master/docs/images/SRT_QuadScreenVideoComparison.png" width="400"/>
</a>

**Access Control**<br/>
**Bonding**<br/>
**Encryption**<br/>
**Handshake**<br/>
**Live Streaming**<br/>
**Packet Filtering & FEC**<br/>
**Socket Groups**<br/>
**SRT Multiplex**<br/>

<br/>

<details>
    <summary>What is SRT?</summary>
    
Secure, Reliable Transport, known simply as SRT, is a protocol that allows unreliable networks like the internet to be used for reliable, encrypted, live video contribution. Created by Haivision and now an open-source technology with an IETF draft spec, the alliance of SRT users continues to grow as the technology continues to develop and add features.

SRT is a transport technology that optimizes transmission across unpredictable networks, such as the Internet. It can be applied to contribution and distribution endpoints as part of a video stream workflow to deliver the best quality and lowest latency video at all times. As audio/video packets are streamed from a source to a destination, SRT detects and adapts to the real-time network conditions between the two endpoints. SRT helps compensate for jitter and bandwidth fluctuations due to congestion over noisy networks. Its error recovery mechanism minimizes the packet loss typical of Internet connections. And SRT supports AES encryption for end-to-end security.
</details>

<p align="right"><a href="https://slackin-srtalliance.azurewebsites.net">Join the conversation</a> in the <b>#development</b> channel on <a href="https://srtalliance.slack.com"><img alt="slack logo" src="https://github.com/stevomatthews/srt/blob/master/docs/images/Slack_RGB2.svg" width="60"></a></p>


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
  </tr>
  <tr>
    <td style="width:20%">
      <p align="center" valign="middle"><a href="https://github.com/Haivision/srt/files/2489142/SRT_Protocol_TechnicalOverview_DRAFT_2018-10-17.pdf"><b>SRT Overview</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/DevelopersGuide.md"><b>SRT Development</b></a></p>
    </td>
    <td style="width:20%">
      <p align="center"><a href="https://github.com/Haivision/srt/blob/master/docs/reporting.md"><b>SRT Feedback</b></a></p>
    </td>
  </tr>
  <tr>
    <td style="width:20%">
      <p align="center">Early draft technical overview (precursor to the RFC)</p>
    </td>
    <td style="width:20%">
      <p align="center">Environment setup to develop, build and test SRT</p>
    </td>
    <td style="width:20%">
      <p align="center">Guidelines for providing feedback and report problems</p>
    </td>
  </tr>
  <tr>
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
      <p align="center">How SRT encryption protects stream payloads</p>
    </td>
    <td style="width:20%">
      <p align="center">Reference documentation for the SRT API</p>
    </td>
    <td style="width:20%">
      <p align="center">Instructions for using test apps (<i>srt-live-transmit, srt-xtransmit</i>, etc.)</p>
    </td>
  </tr>
</table>


### Requirements

* CMake (as build system)
* Tcl 8.5 (optional for user-friendly build system)
* OpenSSL
* Pthreads (built in on POSIX systems; for Windows there is a library)

## Build Instructions

[Linux (Ubuntu/CentOS)](https://github.com/stevomatthews/srt/blob/master/docs/BuildOptions.md) | [Windows](https://github.com/Haivision/srt/blob/master/docs/build-win.md) | [Mac (Darwin)](https://github.com/stevomatthews/srt/blob/master/docs/BuildOptions.md) | [iOS](https://github.com/Haivision/srt/blob/master/docs/build_iOS.md) | [Android](https://github.com/stevomatthews/srt/blob/master/docs/BuildOptions.md)

  - For detailed descriptions of the build system and options, please read [BuildOptions.md](docs/BuildOptions.md).
  - If you encounter build failures, please refer to **troubleshooting-build-issues.md**

## Contributing
Anyone is welcome to contribute. If you decide to get involved, please take a moment to review the guidelines:

  - Bug reports
  - Feature requests
  - Pull requests


## License

TBD


## Examples & Demo

Please visit the [SRT Cookbook](https://srtlab.github.io/srt-cookbook) for more information.


## Release History

Releases are tracked in **srt-changelog.md**


## Sponsors

Please visit [srtalliance.org](srtalliance.org) for more information


## Security

Please report security issues to TBD

## Values

**(12 Apr 2021) Example text borrowed from** [pandas.org](https://pandas.pydata.org/about/index.html): *Is in the core of pandas to be respectful and welcoming with everybody, users, contributors and the broader community. Regardless of level of experience, gender, gender identity and expression, sexual orientation, disability, personal appearance, body size, race, ethnicity, age, religion, or nationality.*

  


---

If you have any questions, please feel free to ask in the <b>#development</b> channel on <a href="https://srtalliance.slack.com">Slack</a>.</p>



