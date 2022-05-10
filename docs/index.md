# Introduction

## What is RaceResultExchange

RaceResultExchange is a small software that exchanges data back-and-forth with RaceResult12. 

The following features are currently available: 

* Syncing of photofinish results 
* Uploading of timing impulses e.g. from ALGE-Timing devices
* Driving an FDS MLED Display for time trials or mass-passings
* Sending HTTP POSTS or GETS on passings

The following features are planned for the future: 

* Output to videowalls and screens

## Prerequisites

RaceResultExchange needs the following prerequisites:

* `Windows 10 (x86 or x64) or higher`
* `.NET 6.0 Desktop Runtime` - [Download](https://dotnet.microsoft.com/download/dotnet/current/runtime)

## Installation

First make sure that all prerequisites are installed.

Then start the Setup process by starting `Setup_RaceResultExchange.exe`. If .NET 6.0 Runtime is missing the setup program will automatically download it and install it.

!!! note 
    Please always install the latest runtime for Desktop manually, the installer is not always aware to install the newest version. We are working on a fix. 
