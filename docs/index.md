# Introduction

## What is RaceResultExchange

RaceResultExchange is a small software that exchanges data back-and-forth with RaceResult12. 

The following features are currently available: 

* Syncing of photofinish results to a RR12 timing point (from a Finishlynx file or directly via ALGE-Timing OptiC3.NET socket)
* Uploading of timing impulses to a RR12 timing points (e.g. via an ALGE-Timing Timy or Tag Heuer CP540)
* Driving various displayboards (e.g. FDS MLED, ALGE-Timing GAZ/DLine or LED walls)
* Trigger Sending of HTTP POST or GET when a detection occurs
* Bulkd sending to a list of recipients with HTTP POST

## Prerequisites

RaceResultExchange needs the following prerequisites:

* `Windows 10 (x86 or x64) or higher`
* `.NET 6.0 Desktop Runtime` - [Download](https://dotnet.microsoft.com/download/dotnet/current/runtime)

## Installation

First make sure that all prerequisites are installed. Then download the latest version from here: 

 [:fontawesome-solid-download: Setup](https://downloads.dbnetsoft.com/raceresultconnector/Setup_RaceResultExchange.exe)

Then start the Setup process by starting `Setup_RaceResultExchange.exe`. If .NET 6.0 Runtime is missing the setup program will automatically download it and install it.

!!! note 
    In case the applications is not startiong, please install the latest runtime for Desktop manually, the installer is not always aware to install the newest version. We are working on a fix. 
