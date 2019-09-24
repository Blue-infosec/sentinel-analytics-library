[![Maintenance](https://img.shields.io/maintenance/yes/2019.svg?style=flat-square)]()
[![GitHub last commit](https://img.shields.io/github/last-commit/netevert/sentinel-analytics-library.svg?style=flat-square)](https://github.com/netevert/sentinel-analytics-library/commit/master)
![Total rules](https://img.shields.io/badge/Total%20rules-217-success?style=flat-square)
[![Twitter Follow](https://img.shields.io/twitter/follow/netevert.svg?style=social)](https://twitter.com/netevert)

# Sentinel analytics library
This repository aims to collect the largest number of Sentinel use cases for detection. All analytics are built in [AZSentinel](https://github.com/wortell/AZSentinel) JSON format for automated upload into Azure.

This repository contains the following Sentinel analytics:

|Folder                      | Author(s)                        | Documentation                  | Number of rules|
|----------------------------|----------------------------------|--------------------------------|----------------|
|AuditLogs                   | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 1              |
|AWSCloudTrail               | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 7              |
|AzureActivity               | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 4              |
|AzureDiagnostics            | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 3              |
|CommonSecurityLog           | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 5              |
|DNSEvents                   | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 4              |
|MultipleDataSources         | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 12             |
|OfficeActivity              | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 6              |
|SecurityEvent               | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 16             |
|SigninLogs                  | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 8              |              |
|Syslog                      | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 5              |
|Sysmon                      | Edoardo Gerosa and Olaf Hartong  | [LINK](https://bit.ly/2lqxPPz) | 117            |
|ThreatIntelligenceIndicator | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 25             |
|W3CIISLog                   | Microsoft                        | [LINK](https://bit.ly/2mvHXqg) | 4              |

# Installation
The rules in each folder can be uploaded into your Sentinel instance in an automated manner using the [AZSentinel](https://github.com/wortell/AZSentinel) PowerShell module, developed by the folks at [Wortell Sec](https://security.wortell.nl/) and the JSON file contained within each folder.

Instructions for the prerequisites needed to run AZSentinel can be found [here](https://github.com/wortell/AZSentinel/wiki#getting-started).

Once AZSentinel is installed, the rules in this folder can be automatically imported with this command:

    Import-AzSentinelAlertRule -WorkspaceName "{workspace_name}" -SettingsFile "folder_name/file_in_folder.json"

# Disclaimer
The rules within this project are copied from different repositories (repository links are provided in the table above) and translated into AZSentinel JSON format without testing. Although the rules come from reputable authors there is a chance that issues within the KQL source code could emerge and break the automatic upload once AZSentinel is used. Feel free to open [an issue](https://github.com/netevert/sentinel-analytics-library/issues) in case you discover problems.

# Contributing
Contributions are welcome - in particular if you have discovered a repository of KQL rules that you'd like translated into AZSentinel JSON format feel free to open an issue to request the rules be translated and added to this project.
