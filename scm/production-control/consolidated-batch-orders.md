---
title: Consolidated batch orders
description: This article describes the concept of consolidated batch orders.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 45c83752b4dc50a615e3bb64320cb22b7fc6dec0
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="consolidated-batch-orders"></a>Consolidated batch orders

[!include[banner](../includes/banner.md)]


This article describes the concept of consolidated batch orders.

A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item. The relation between the bulk item and the packed item is expressed in a bulk item conversion. This bulk item conversion is defined on the bulk item itself.  

Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit. By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.  

A consolidated batch order can contain any combination of the following orders:

-   A single bulk order and multiple packed orders
-   Multiple bulk orders and multiple packed orders
-   Multiple bulk orders and a single packed order
-   Only packed orders




