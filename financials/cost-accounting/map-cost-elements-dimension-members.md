---
title: Map cost element dimension members to a common set of dimension members
description: By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3cbcc5e7090f1a32b0c35fdb06427b5c225e857b
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Map cost element dimension members to a common set of dimension members

[!include[banner](../includes/banner.md)]


By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.

If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts. When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts. However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Map cost element dimension members to a common format
The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members. You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.

| Source: US chart of accounts                                          | Source: French chart of accounts                                          | New common set of cost element dimension members                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Imported cost element dimension members from the US chart of accounts | Imported cost element dimension members from the French chart of accounts | Mapping of US and French cost element dimension members to a common set |
| 5001: Sales                                                           | 5001: Sales and advertising                                               | 5000: Sales and advertising                                             |
| 5030: Advertising                                                     | 6390: Stock purchase\*                                                    | 7000: Cleaning expenses                                                 |
| 7001: Cleaning expenses                                               | 7001: Travel expense                                                      | 7001: Travel expenses                                                   |

\*The Stock purchase French cost element dimension member isn't mapped.

## <a name="currency-conversion"></a>Currency conversion
The various charts of accounts that you use might be set up to use different currencies. In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used. In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.

## <a name="update-mappings-at-any-time"></a>Update mappings at any time
You can update the mapping definitions for a cost element dimension at any time. Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.




