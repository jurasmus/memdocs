---
# required metadata
title: Remotely manage Windows 365 devices
titleSuffix:
description: Learn how to remotely manage Windows 365 devices
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 07/05/2023
ms.topic: how-to
ms.service: windows-365
ms.subservice: 
ms.localizationpriority: high
ms.technology:
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: 
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection:
- M365-identity-device-management
- tier2
---

# Remotely manage Windows 365 devices

You can remotely manage Cloud PCs in Intune just like any other managed device. For more information, see [Remotely run device actions with Intune](/mem/intune/remote-actions/).

Cloud PCs support the following remote management actions:

- Restart
- Power On
- Power Off
- Sync
- Rename
- Quick Scan
- Full Scan
- Update Windows Defender
- [Reprovisioning](provisioning.md#reprovisioning) (this remote action is specific to Cloud PC devices)
- [Resize](resize-cloud-pc.md) (this remote action is specific to Cloud PC devices)
- [Collect diagnostics](/mem/intune/remote-actions/collect-diagnostics)
- [Place Cloud PC Under Review](place-cloud-pc-under-review.md)

## Windows 365 Frontline Cloud PCs

Frontline Cloud PCs support remote actions like Enterprise Cloud PCs. One difference is that a Frontline Cloud PC power state is determined by the end user. When a Frontline Cloud PC is on, remote actions are started immediately. If a Frontline Cloud PC is powered off, remote actions start as soon as the Cloud PC is powered on. When a Cloud PC is powered on, it uses a license that others can't use. When the Cloud PC is powered off, the license is freed up so others can use it.

You can view the power state for Frontline Cloud PCs in the Intune portal on the devices **Properties** page.

You can remotely power on and off a Frontline Cloud PC. When you power on a Frontline Cloud PC, a license is automatically consumed. When you power off a Frontline Cloud PC, any user currently signed in is signed off. Unsaved data on the Cloud PC is lost.

<!-- ########################## -->
## Next steps

[Reprovision a Cloud PC](reprovision-cloud-pc.md).
