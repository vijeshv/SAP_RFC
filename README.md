# SAP_RFC

RFC is a protocol used by SAP systems to  communicate and execute functions in remote systems (sap/external). Mainly used for dataexcahnge , system integartions & distributed computing.Its classified in to four types, synchronous RFC ,Assynchronus RFC , Transactional RFC & Queued RFC​.

## Overview

This repository contains NeoLoad Advanced Actions that allows performance testers using NeoLoad to connect SAP Server Server & make RF calls.
Implementation is in progress.

| Property           | Value                                                                         |
|--------------------|-------------------------------------------------------------------------------|
| Maturity           | Experimental                                                                  |
| Support            | Supported by Neotys                                                           |
| Author             | Neotys                                                                        |
| License            | [BSD Simplified](https://www.neotys.com/documents/legal/bsd-neotys.txt)       |
| NeoLoad            | 2024.2 (Enterprise or Professional Edition w/ Integration & Advanced Usage)    |
| Bundled in NeoLoad | No                                                                          |
| Download Binaries  | See the [latest release]() |


## Installation

### Setting up the NeoLoad Advance action for SAP RFC

1. Download the latest Advance Action jar [latest release](https://github.com/Neotys-Labs/SAP_RFC/releases/tag/sap-RFC-0.0.6).
   Keept the Jar file in the extlib folder of yor Neoload Project

3. Download the External Refereces files from floder (https://github.com/Neotys-Labs/SAP_RFC/tree/main/ExternalReferences)
   keep sapjco3.jar & sapidoc3.jar (optional need only if you want IDOC transfer)in Jar file in the extlib folder of yor Neoload Project
   keep sapjco3.dll file <Neoload Installation folder>\lib\x64

4. restart neoload
## Advanced Actions definitions
### SAP_RFC

Advanced Actions to perform various opeartions connecting SAP server, Scan server for various functions defenitions/metadata then execute the same  based on your inputs & show the output revived back from server if any.
##1. RFC Connect - Parameters
This Advanced Action establishes a connection with server  based on your input

| Name                     | Description       |
| ---------------          | ----------------- |
| Destination              | A name of the SAP connection. this name will be using in rest of teh actions            |
| Host                     | SAP Server name or IP address to connect |
| SYSNR                    | SYSNR |
| Client                   | Client |
| Username                 | Username |
| Password                 | Password |

Status Codes:
* NL-RFCClient_ERROR :  Any error while calling RFC function. 
Example:
<p align="center"><img src="/screenshot/sap_rfc_reqdesign.PNG" alt="sap_rfc" /></p>
<p align="center"><img src="/screenshot/sap_rfc_response.PNG" alt="sap_rfc_response" /></p>

## RFC Scan Function - Parameters
This Advanced Action retreives the defenition of function -Inputs & Oupputs parameters

| Name                     | Description       |
| ---------------          | ----------------- |
| Destination              | A name of the SAP connection. this name will be using in rest of teh actions            |
| Remote Functiuon         | Name of the remote function |


Status Codes:
* NL-RFCClient_ERROR :  Any error while calling RFC function. 
Example:
<p align="center"><img src="/screenshot/scan_function_design.PNG" alt="sap_rfc_scan_design" /></p>
<p align="center"><img src="/screenshot/scan function_response.PNG" alt="sap_rfc_scan_response" /></p>

## RFC Execute - Parameters
This Advanced Action execute the RFC function -Inputs & Oupputs parameters

| Name                     | Description       |
| ---------------          | ----------------- |
| Destination              | A name of the SAP connection. this name will be using in rest of teh actions            |
| Remote Functiuon         | Name of the remote function |
| InParameters Value       | Input parameters & its values tuples coma separated  EX- param1:value1,parm2:value2 |

Status Codes:
* NL-RFCClient_ERROR :  Any error while calling RFC function. 
Example:
<p align="center"><img src="/screenshot/Execute_function_Design.PNG" alt="sap_rfc_execute_design" /></p>
<p align="center"><img src="/screenshot/Execute_function_response.PNG" alt="sap_rfc_execute_response" /></p>

Status Codes:
* NL-RFCClient_ERROR :  Any error while calling RFC function. 


## ChangeLog

* Version 0.0.2 (June 10st 2024): perform Simple function calls Table & structure yet to implement

