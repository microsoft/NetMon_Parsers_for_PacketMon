# Project

Packet Monitor (PacketMon) generates logs in etl format. These logs can be analyzed using Microsoft Network Monitor (Netmon) by using special parsers. This page will detail how to analyze PacketMon-generated etl files within Netmon.

Follow these steps to install and configure Netmon to parse PacketMon-generated etl files:

-Install Network Monitor 3.4 from https://www.microsoft.com/en-us/download/4865.
-Start Network Monitor elevated and set Windows as Active parser profile at (Tools / Options / Parser Profiles).
-Copy etl_Microsoft-Windows-PktMon-Events.npl from https://github.com/microsoft/NetMon_Parsers_for_PacketMon/blob/main/etl_Microsoft-Windows-PktMon-Events.npl to -"%PROGRAMDATA%\Microsoft\Network Monitor 3\NPL\NetworkMonitor Parsers\Windows"
-Copy stub_etl_Microsoft-Windows-PktMon-Events.npl from https://github.com/microsoft/NetMon_Parsers_for_PacketMon/blob/main/stub_etl_Microsoft-Windows-PktMon-Events.npl to "%PROGRAMDATA%\Microsoft\Network -Monitor 3\NPL\NetworkMonitor Parsers\Windows\Stubs"
-Rename stub_etl_Microsoft-Windows-PktMon-Events.npl to etl_Microsoft-Windows-PktMon-Events.npl
-Include etl_Microsoft-Windows-PktMon-Events.npl into NetworkMonitor_Parsers_sparser.npl at "%PROGRAMDATA%\Microsoft\Network Monitor 3\NPL\NetworkMonitor Parsers"
-Restart Network Monitor elevated for rebuilding the parsers.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
