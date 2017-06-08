---
title: Initialize seed data in a new Retail environment
description: This article describes the data that&quot;s created as part of the initialization process for Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 534c9ab0f4d95f42d09f35d3197a2258c8d39526
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialize seed data in a new Retail environment

[!include[banner](includes/banner.md)]


This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Operations - Retail.

After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data. **Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores. This step must be completed for each legal entity that you use for retail. To initialize the retail configuration, follow these steps.

1.  Start the Dynamics 365 for Operations client.
2.  Click **Retail and commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.
3.  Click **Initialize**.

Initialization creates the following default configuration data:

-   Retail scheduler jobs and subjobs
-   Retail channel schema
-   Retail distribution schedules
-   Default screen layouts, which include button grids, images, and themes
-   Time zone information
-   Point-of-sale (POS) operations
-   POS permissions
-   Channel reports
-   Attribute metadata
-   Entity validation templates
-   Batch job to purge Commerce Data Exchange session history

Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Operations database. **Note:** There is an option to separately configure the Retail scheduler. This option lets you reset the Retail scheduler configuration to its default settings. After initialization is completed, you must configure additional retail data. Here are some examples:

-   Retail parameters
-   Retail scheduler parameters
-   Retail channels
-   Registers and devices
-   Assortments





