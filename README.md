# Azure Pipelines Tasks
![Tasks](/taskbanner.png "Tasks")

## Overview
This repo contains the tasks that are provided out-of-the-box with Azure Pipelines and Team Foundation Server.

This provides open examples on how we write tasks which will help you write other tasks which can be uploaded to your account or server.  See **Writing Tasks** below.

![MarsScore2]

## Status
|   | MARS Score |
|---|:-----:|
|![Win](docs/res/win_med.png) **Windows**|[![Build & Test][win-build-badge]][win-build]| 
|![macOS](docs/res/apple_med.png) **macOS**|[![Build & Test][macOS-build-badge]][macOS-build]| 
|![Linux](docs/res/linux_med.png) **Linux**|[![Build & Test][linux-build-badge]][linux-build]|

[MarsScore2]: https://repo-badge-python.azurewebsites.net/api/HttpTrigger?repo=azure-pipelines-tasks
[win-build-badge]: https://img.shields.io/static/v1?label=mars-score&message=31&color=red
[win-build]: https://img.shields.io/static/v1?label=mars-score&message=31&color=red

[macOS-build-badge]: https://img.shields.io/static/v1?label=mars-score&message=45&color=yellowgreen
[macOS-build]: https://img.shields.io/static/v1?label=mars-score&message=45&color=yellowgreen

[linux-build-badge]: https://img.shields.io/static/v1?label=mars-score&message=80&color=green
[linux-build]: https://img.shields.io/static/v1?label=mars-score&message=80&color=green

## How to Use Tasks

See the documentation for [Continuous integration and deployment](https://aka.ms/tfbuild).

## Writing Tasks

If you need custom functionality in your build/release, it is usually simpler to use the existing script running tasks such as the PowerShell or Bash tasks.  Writing a new task may be appropriate if you need deeper integration o.r reusability in many build definitions

Tasks are simply tool runners.  They know how to run MSBuild, VSTest, etc... in a first class way and handle return codes, how to treat std/err out, and how to write timeline records based on expected output.  They also get access to credentials to write back to TFS/Azure Pipelines. 

For uploading custom tasks to Azure Pipelines use the [TFS Cross Platform Command Line utility](https://github.com/Microsoft/tfs-cli).

Tasks can also be deployed with an Azure DevOps extension. See [this tutorial](https://docs.microsoft.com/en-us/vsts/extend/develop/add-build-task) for how to write a custom task and package it inside an extension.

## Contributing

This project welcomes [contributions and suggestions](docs/contribute.md).

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
