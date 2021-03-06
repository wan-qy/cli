# .NET Command Line Interface

[![.NET Slack Status](https://aspnetcoreslack.herokuapp.com/badge.svg?2)](http://tattoocoder.com/aspnet-slack-sign-up/) [![Join the chat at https://gitter.im/dotnet/cli](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/dotnet/cli?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This repo contains the source code for cross-platform [.NET Core](http://github.com/dotnet/core) command line toolchain. It contains the implementation of each command, the native packages for various supported platforms as well as documentation. 

RTM and Preview 2 bits
---------------------
To get the latest released bits (RTM for .NET Core and Preview 2 for tooling), 
check out our [Getting started page](http://go.microsoft.com/fwlink/?LinkID=798306&clcid=0x409).

Also, don't forget to check out [the documentation](https://aka.ms/dotnet-cli-docs). 

Changes in issue triaging
-------------------------
We are making significant changes to the CLI tooling by supporting MSBuild as the build engine and `csproj` as the project format. You can read ["Changes to project.json" blog post](https://blogs.msdn.microsoft.com/dotnet/2016/05/23/changes-to-project-json/) for more context. We've realized that this also means that many of the shortcomings of the current tooling will be solved by this move so we've decided to introduce two new labels to indicate that in the issues: 

* `msbuild-mitigated` - this label indicates the issue will be mitigated via move to MSBuild. 
* `msbuild-notapplicable` - this label indicates the issue will not be applicable after moving to MSBuild.

We will close issues that are labelled with one of these labels. Proactive triaging will help us reduce the number of issues and enable us to focus on issues that require fixing independent of the move to msbuild.

Please feel free to re-open and comment on any issue that you believe was triaged incorrectly.

Found an issue?
---------------
You can consult the [known issues page](https://github.com/dotnet/core/blob/master/cli/known-issues.md) to find out the current issues and 
to see the workarounds.  

If you don't find your issue, please file one! However, given that this is a very high-frequency repo, we've setup some [basic guidelines](Documentation/issue-filing-guide.md) to help you. Please consult those first.

This project has adopted the code of conduct defined by the [Contributor Covenant](http://contributor-covenant.org/) to clarify expected behavior in our community. For more information, see the [.NET Foundation Code of Conduct](http://www.dotnetfoundation.org/code-of-conduct).

Build Status
------------

|Ubuntu 14.04 / Linux Mint 17 |Ubuntu 16.04 |Debian 8.2 |Windows x64 |Windows x86 |Mac OS X |CentOS 7.1 / Oracle Linux 7.1 |RHEL 7.2 |OpenSUSE 13.2 |Fedora 23|
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3132/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3132)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3618/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3618)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3271/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3271)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3022/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3022)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3071/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3071)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3397/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3397)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3257/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3257)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3256/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3256)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3626/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3626)|[![](https://mseng.visualstudio.com/_apis/public/build/definitions/d09b7a4d-0a51-4c0e-a15a-07921d5b558f/3623/badge)](https://mseng.visualstudio.com/dotnetcore/_build?_a=completed&definitionId=3623)|

Installers and Binaries
-----------------------

You can download .NET Core as either an installer (MSI, PKG) or a zip (zip, gzip). You can download the product in two flavors:

- .NET Core - .NET Core runtime and framework
- .NET Core SDK - .NET Core + CLI tools

> **Note:** please be aware that below installers are the **latest bits**. If you 
> want to install the latest released versions, please check out the [section above](#rtm-and-preview-2-bits).)

|         |Version |.NET Core Installer|.NET Core SDK Installer|.NET Core Binaries|.NET Core SDK Binaries|
|---------|:------:|:------:|:------:|:------:|:------:|
|**Windows x64**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Windows_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Installers/Latest/dotnet-win-x64.latest.exe)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-win-x64.latest.exe)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-win-x64.latest.zip)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-win-x64.latest.zip)|
|**Windows x86**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Windows_x86_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Installers/Latest/dotnet-win-x86.latest.exe)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-win-x86.latest.exe)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-win-x86.latest.zip)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-win-x86.latest.zip)|
|**Ubuntu 14.04 / Linux Mint 17**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Ubuntu_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|*See Below*|*See Below*|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-ubuntu-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-ubuntu-x64.latest.tar.gz)|
|**Ubuntu 16.04**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Ubuntu_16_04_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|N/A |N/A |[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-ubuntu.16.04-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-ubuntu.16.04-x64.latest.tar.gz) |
|**Debian 8.2**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Debian_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|N/A|N/A|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-debian-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-debian-x64.latest.tar.gz)|
|**Mac OS X**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/OSX_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Installers/Latest/dotnet-osx-x64.latest.pkg)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-osx-x64.latest.pkg)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-osx-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-osx-x64.latest.tar.gz)|
|**CentOS 7.1 / Oracle Linux 7**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/CentOS_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|N/A |N/A |[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-centos-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-centos-x64.latest.tar.gz)|
|**RHEL 7.2**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/RHEL_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|N/A |N/A |[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-rhel-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-rhel-x64.latest.tar.gz) |
|**openSUSE 13.2**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/openSUSE_13_2_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|N/A |N/A |[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-opensuse.13.2-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-opensuse.13.2-x64.latest.tar.gz) |
|**Fedora 23**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Fedora_23_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|N/A |N/A |[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/Latest/dotnet-fedora.23-x64.latest.tar.gz)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-dev-fedora.23-x64.latest.tar.gz) |

Ubuntu Installers
----------

*Our Debian packages are put together slightly differently than the other OS specific installers. Instead of combining everything, we have separate component packages that depend on each other. If you're installing these directly from the .deb files (via dpkg or similar), then you'll need to install them in the order presented below.*

**For Ubuntu 14.04

|         |Version |Installers|
|---------|:------:|:------:|:------:|
|**Shared Host**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Ubuntu_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Installers/Latest/dotnet-host-ubuntu-x64.latest.deb)|
|**Host Framework Resolver**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Ubuntu_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Installers/Latest/dotnet-hostfxr-ubuntu-x64.latest.deb)|
|**Shared Framework**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Ubuntu_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/preview/Installers/Latest/dotnet-sharedframework-ubuntu-x64.latest.deb)|
|**Sdk**|[![](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/Ubuntu_x64_Release_version_badge.svg)](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/latest.version)|[Download](https://dotnetcli.blob.core.windows.net/dotnet/Sdk/rel-1.0.0/dotnet-sdk-ubuntu-x64.latest.deb)|

Docker
------

You can also use our Docker base images found on https://hub.docker.com/r/microsoft/dotnet to set up your dev or testing environment for usage.  

Basic usage
-----------

When you have the .NET Command Line Interface installed on your OS of choice, you can try it out using some of the samples on the [dotnet/core repo](https://github.com/dotnet/core/tree/master/samples). You can download the sample in a directory, and then you can kick the tires of the CLI.


First, you will need to restore the packages:
	
	dotnet restore
	
This will restore all of the packages that are specified in the project.json file of the given sample.

Then you can either run from source or compile the sample. Running from source is straightforward:
	
	dotnet run
	
Compiling to IL is done using:
	
	dotnet build

This will drop an IL assembly in `./bin/[configuration]/[framework]/[binary name]` 
that you can run using `dotnet bin/[configuration]/[framework]/[binaryname.dll]`.

For more details, please refer to the [documentation](https://aka.ms/dotnet-cli-docs).

Building from source
--------------------

If you are building from source, take note that the build depends on NuGet packages hosted on MyGet, so if it is down, the build may fail. If that happens, you can always see the [MyGet status page](http://status.myget.org/) for more info. 

Read over the [contributing guidelines](CONTRIBUTING.md) and [developer documentation](Documentation) for prerequisites for building from source.

Questions & Comments
--------------------

For any and all feedback, please use the Issues on this repository. 

License
--------------------

By downloading the .zip you are agreeing to the terms in the project [EULA](https://aka.ms/dotnet-core-eula).
