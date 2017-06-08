---
title: Cost entries
description: This article provides information about cost entries and when they are created. A cost entry is a record that registers the quantity and cost of a given event.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1045ecbf7080f12bc60336609180173544e4e0eb
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="cost-entries"></a>Cost entries

[!include[banner](../includes/banner.md)]


This article provides information about cost entries and when they are created. A cost entry is a record that registers the quantity and cost of a given event.

Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.

## <a name="examples"></a>Examples
### <a name="example-1-no-cost-entries-are-created"></a>Example 1: No cost entries are created

A transfer journal event is registered. The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object. Therefore, the event creates two inventory transactions and no cost entries.

### <a name="example-2-cost-entries-are-created"></a>Example 2: Cost entries are created

A transfer journal event is registered. The event transfers one piece of item A from site 1 to site 2. The Site inventory dimension is considered part of the cost object. Therefore, the event creates two inventory transactions and two cost entries.

### <a name="example-3-one-cost-entry-is-created"></a>Example 3: One cost entry is created

A product receipt event is registered for a purchase order. The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD). Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received. Therefore, the event creates 100 inventory transactions and one cost entry.

## <a name="cost-entries-page"></a>Cost entries page
The new **Cost entries** page lets you view and control registrations of quantities and costs. This page complements the **Inventory transaction** and **Inventory settlement** pages. Records are registered in chronological order for an event. Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document. Here is an example:

-   A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.
-   A few days after the invoice event is registered, the cost increases to 11.00 USD. Therefore, the total amount is 1,100 USD. A second voucher is created to account for the difference of 100 USD.
-   A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.

| Voucher | Date       | Reference      | Number | Lot ID  | Quantity | Amount  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01-01-2015 | Purchase order | 100001 | 0000101 | 100.00   | 1000.00 |
| 00002   | 20-01-2015 | Purchase order | 100001 | 0000101 |          | 100.00  |
| 00003   | 31-01-2015 | Adjustment     | 100001 | 0000101 |          | 15.00   |

The **Cost entries** page enables filtering by document ID and document date. 

> [!NOTE]
> Cost entries are available only for [cost objects](cost-object.md) or released products.

<a name="see-also"></a>See also
--------

[Cost objects](cost-object.md)




