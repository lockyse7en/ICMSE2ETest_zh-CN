---
title: "SharedPC DDF 文件"
description: "SharedPC DDF 文件"
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/hardware
ms.assetid: 70234197-07D4-478E-97BB-F6C651C0B970
ms.openlocfilehash: b46f05ccd93a5996fe6e3d518b1dbb885979e994
ms.sourcegitcommit: d33e870dc4850bf0ea47fdae0d163b04c1c90f15
translationtype: MT
---
# <a name="sharedpc-ddf-file"></a>SharedPC DDF 文件


本主题演示 OMA DM 设备描述框架 (DDF) **SharedPC**配置服务提供程序。 DDF 文件只能用于提供 XML 的 OMA DM。

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE MgmtTree PUBLIC " -//OMA//DTD-DM-DDF 1.2//EN"
    "http://www.openmobilealliance.org/tech/DTD/DM_DDF-V1_2.dtd"
    [<?oma-dm-ddf-ver supported-versions="1.2"?>]>
<MgmtTree xmlns:MSFT="http://schemas.microsoft.com/MobileDevice/DM">
    <VerDTD>1.2</VerDTD>
    <Node>
        <NodeName>SharedPC</NodeName>
        <Path>./Vendor/MSFT</Path>
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
                <MIME>com.microsoft/1.0/MDM/SharedPC</MIME>
            </DFType>
        </DFProperties>
        <Node>
            <NodeName>EnableSharedPCMode</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>false</DefaultValue>
                <Description>Setting this node to "true" triggers the action to configure a device to Shared PC mode.</Description>
                <DFFormat>
                    <bool />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Enable shared PC mode</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>SetEduPolicies</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>true</DefaultValue>
                <Description>Specify that the policies defined for EDU scenario should be set when configuring SharedPC mode. This node is optional. If used, it needs to be set before the action on "EnableSharedPCMode" node is taken.</Description>
                <DFFormat>
                    <bool />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Set EDU policies</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>SetPowerPolicies</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>true</DefaultValue>
                <Description>Specify that the power policies should be set when configuring SharedPC mode. This node is optional. If used, it needs to be set before the action on "EnableSharedPCMode" node is taken.</Description>
                <DFFormat>
                    <bool />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Set power policies</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>MaintenanceStartTime</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>0</DefaultValue>
                <Description>Daily start time of maintenance hour. Given in minutes from midnight. Default is 0 (12am). This node is optional. If used, it needs to be set before the action on "EnableSharedPCMode" node is taken.</Description>
                <DFFormat>
                    <int />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Maintenance start time</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>SignInOnResume</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>true</DefaultValue>
                <Description>Require signing in on waking up from sleep. This node is optional. If used, it needs to be set before the action on "EnableSharedPCMode" node is taken.</Description>
                <DFFormat>
                    <bool />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Sign-in on resume</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>SleepTimeout</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>3600</DefaultValue>
                <Description>Time in seconds that a device sits at Logon screen before signing the user out. 0 means never. Default is 1 hour. This node is optional. If used, it needs to be set before the action on "EnableSharedPCMode" node is taken.</Description>
                <DFFormat>
                    <int />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Sleep timeout</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>EnableAccountManager</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>true</DefaultValue>
                <Description>Enable the account manager for shared PC mode.</Description>
                <DFFormat>
                    <bool />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Enable account manager</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>AccountModel</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>0</DefaultValue>
                <Description>Configures which type of accounts are allowed to use the PC. Allowed values: 0 (only guest), 1 (domain-joined only), 2 (domain-joined and guest).</Description>
                <DFFormat>
                    <int />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Account model</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>DeletionPolicy</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>1</DefaultValue>
                <Description>Configures when accounts will be deleted. Allowed values: 0 (delete immediately), 1 (delete at disk space threshold).</Description>
                <DFFormat>
                    <int />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Account deletion policy</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>DiskLevelDeletion</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>25</DefaultValue>
                <Description>Accounts will start being deleted when available disk space falls below this threshold, given as percent of total disk capacity. Accounts that have been inactive the longest will be deleted first.</Description>
                <DFFormat>
                    <int />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Disk space threshold for account deletion</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
        <Node>
            <NodeName>DiskLevelCaching</NodeName>
            <DFProperties>
                <AccessType>
                    <Get />
                    <Replace />
                </AccessType>
                <DefaultValue>50</DefaultValue>
                <Description>Stop deleting accounts when available disk space reaches this threshold, given as percent of total disk capacity.</Description>
                <DFFormat>
                    <int />
                </DFFormat>
                <Occurrence>
                    <One />
                </Occurrence>
                <Scope>
                    <Permanent />
                </Scope>
                <DFTitle>Disk space threshold for account caching</DFTitle>
                <DFType>
                    <MIME>text/plain</MIME>
                </DFType>
            </DFProperties>
        </Node>
    </Node>
</MgmtTree>
```

## <a name="related-topics"></a>相关的主题


[SharedPC 配置服务提供程序](sharedpc-csp.md)

 

 






