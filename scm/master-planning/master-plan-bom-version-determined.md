---
title: Determine the BOM version
description: During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ee265d0ab7807cd92c70096111ffb3dbec11ad62
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="determine-the-bom-version"></a>Determine the BOM version

[!include[banner](../includes/banner.md)]


During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site. 

The site dimension is always known and is stated on the demand transaction. The following process is used to determine the BOM version to use:

-   If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.
-   If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used. A general BOM does not state a site, and it is valid for multiple sites. If there is a general BOM, it is used.
-   If there is no general BOM version to use, the demand explosion stops at this point.

A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.






