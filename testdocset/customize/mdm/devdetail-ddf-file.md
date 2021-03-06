---
title: "DevDetail DDF 文件"
description: "DevDetail DDF 文件"
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/hardware
ms.assetid: 645fc2b5-2d2c-43b1-9058-26bedbe9f00d
ms.openlocfilehash: 8953d117285227d785ed282443f259c095ab6f41
ms.sourcegitcommit: d33e870dc4850bf0ea47fdae0d163b04c1c90f15
translationtype: MT
---
# <a name="devdetail-ddf-file"></a>DevDetail DDF 文件


本主题演示 OMA DM 设备描述框架 (DDF) **DevDetail**配置服务提供程序。 DDF 文件只能用于提供 XML 的 OMA DM。

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC "-//OMA//DTD-DM-DDF 1.2//EN"
    "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
    [<?oma-dm-ddf-ver supported-versions="1.2"?>]>
<MgmtTree xmlns:MSFT="http://schemas.microsoft.com/MobileDevice/DM">
  <VerDTD>1.2</VerDTD>
  <Node>
    <NodeName>DevDetail</NodeName>
    <Path>.</Path>
    <DFProperties>
      <AccessType>
        <Get />
      </AccessType>
      <DFFormat>
        <node />
      </DFFormat>
      <Occurrence>
        <One />
      </Occurrence>
      <Scope>
        <Permanent />
      </Scope>
      <DFType>
        <DDFName>urn:oma:mo:oma-dm-devdetail:1.0</DDFName>
      </DFType>
    </DFProperties>
    <Node>
      <NodeName>URI</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <DFFormat>
          <node />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <DDFName></DDFName>
        </DFType>
      </DFProperties>
      <Node>
        <NodeName>MaxDepth</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>MaxTotLen</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>MaxSegLen</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
    </Node>
    <Node>
      <NodeName>DevTyp</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>Device model name, as specified and tracked by the manufacturer</Description>
        <DFFormat>
          <chr />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
    <Node>
      <NodeName>OEM</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>Name of OEM</Description>
        <DFFormat>
          <chr />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
    <Node>
      <NodeName>FwV</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>Provide the version of OEM ROM region.</Description>
        <DFFormat>
          <chr />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
    <Node>
      <NodeName>SwV</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>Returns the Windows Phone OS software version.</Description>
        <DFFormat>
          <chr />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
    <Node>
      <NodeName>HwV</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>Returns the hardware version.</Description>
        <DFFormat>
          <chr />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
    <Node>
      <NodeName>LrgObj</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>
        </Description>
        <DFFormat>
          <bool />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <MIME>text/plain</MIME>
        </DFType>
      </DFProperties>
    </Node>
    <Node>
      <NodeName>Ext</NodeName>
      <DFProperties>
        <AccessType>
          <Get />
        </AccessType>
        <Description>Subtree to hold vendor-specific parameters</Description>
        <DFFormat>
          <node />
        </DFFormat>
        <Occurrence>
          <One />
        </Occurrence>
        <Scope>
          <Permanent />
        </Scope>
        <DFType>
          <DDFName></DDFName>
        </DFType>
      </DFProperties>
      <Node>
        <NodeName>Microsoft</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>Subtree to hold vendor-specific parameters</Description>
          <DFFormat>
            <node />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <DDFName></DDFName>
          </DFType>
        </DFProperties>
        <Node>
          <NodeName>MobileID</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Indicates the subscriber ID registered with the cellular network. For GSM and UMTS networks, the value returned is the IMSI value; for other networks, SyncML Status code 404 is returned.</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>RadioSwV</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Version of the software radio stack</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>Resolution</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Resolution of the device in the format of WidthxLength (e.g., "400x800").</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>CommercializationOperator</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Name of operator with whom the device was commercialized.</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>ProcessorArchitecture</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Processor architecture of the device, as returned by the GetSystemInfo API.</Description>
            <DFFormat>
              <int />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>ProcessorType</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Processor type of the device, as returned by the GetSystemInfo API.</Description>
            <DFFormat>
              <int />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>OSPlatform</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Name of the operating system platform.</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>LocalTime</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Returns the UTC time formatted per ISO8601. Example: 2003-06-16T18:37:44Z.</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>DeviceName</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
              <Replace />
            </AccessType>
            <Description>User-specified device name</Description>
            <DFFormat>
              <chr />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>TotalStorage</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Total available storage in MB from first internal drive on the device (may be less than total physical storage).  Available for Windows Mobile only.</Description>
            <DFFormat>
              <int />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
        <Node>
          <NodeName>TotalRAM</NodeName>
          <DFProperties>
            <AccessType>
              <Get />
            </AccessType>
            <Description>Total available memory in MB on the device (may be less than total physical memory).</Description>
            <DFFormat>
              <int />
            </DFFormat>
            <Occurrence>
              <One />
            </Occurrence>
            <Scope>
              <Permanent />
            </Scope>
            <DFType>
              <MIME>text/plain</MIME>
            </DFType>
          </DFProperties>
        </Node>
      </Node>
      <Node>
        <NodeName>WLANMACAddress</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>The MAC address of the active WiFi connection</Description>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>VoLTEServiceSetting</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>The VoLTE service setting on or off. Only exposed to Mobile Operator-based OMA-DM servers.</Description>
          <DFFormat>
            <bool />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Permanent />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>WlanIPv4Address</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>The IPv4 address of the active WiFi connection. Only exposed to Enterprise-based OMA-DM servers.</Description>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Dynamic />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>WlanIPv6Address</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>The IPv6 address of the active WiFi connection. Only exposed to Enterprise-based OMA-DM servers.</Description>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Dynamic />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>WlanDnsSuffix</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>The DNS suffix of the active WiFi connection. Only exposed to Enterprise-based OMA-DM servers.</Description>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Dynamic />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
      <Node>
        <NodeName>WlanSubnetMask</NodeName>
        <DFProperties>
          <AccessType>
            <Get />
          </AccessType>
          <Description>The subnet mask for the active WiFi connection. Only exposed to Enterprise-based OMA-DM servers.</Description>
          <DFFormat>
            <chr />
          </DFFormat>
          <Occurrence>
            <One />
          </Occurrence>
          <Scope>
            <Dynamic />
          </Scope>
          <DFType>
            <MIME>text/plain</MIME>
          </DFType>
        </DFProperties>
      </Node>
    </Node>
  </Node>
</MgmtTree>
```

## <a name="related-topics"></a>相关的主题


[DevDetail 配置服务提供程序](devdetail-csp.md)

 

 






