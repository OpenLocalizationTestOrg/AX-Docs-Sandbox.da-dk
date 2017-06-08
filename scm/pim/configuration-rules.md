---
title: Configuration rules
description: This article provides general information about configuration rules. Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 74c8ffe4ab00e7afa1235e24327e18a65061636a
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="configuration-rules"></a>Configuration rules

[!include[banner](../includes/banner.md)]


This article provides general information about configuration rules. Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.

Configuration rules are available when you define dimension-based configuration models. Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM). After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined. If two items belong together, the **Select** operator is used to ensure inclusion. If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.  

**Note:** This information applies only to product masters that use the dimension-based configuration technology.  

Existing configurations aren't affected by subsequent changes to the configuration rules. However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.  

**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected. For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.

<a name="see-also"></a>See also
--------

[Dimension-based product configuration](dimension-based-product-configuration.md)




