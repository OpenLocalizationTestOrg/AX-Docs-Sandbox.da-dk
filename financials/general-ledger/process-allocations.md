---
title: Process allocations
description: This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Operations, and how they can be used in budget planning. Allocations are used to distribute amounts across multiple ledger account combinations. They help guarantee that expenses or revenue is charged to the correct object in accounting.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1cfaeab1562716aa4c91806b228f17625e25dfff
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="process-allocations"></a>Process allocations

[!include[banner](../includes/banner.md)]


This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Operations, and how they can be used in budget planning. Allocations are used to distribute amounts across multiple ledger account combinations. They help guarantee that expenses or revenue is charged to the correct object in accounting.

Microsoft Dynamics 365 for Operations provides the following capabilities to support this process:

-   Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document. For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)
-   Automatically allocate transactions amounts based on allocation terms defined on individual main account. Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.
-   Automatically allocate ledger balances or fixed amounts based on ledger allocation rules. The ledger allocation rules are processed on a periodic basis using allocation journals. 

###  <a name="allocations-in-budget-planning"></a>Allocations in budget planning

Ledger allocation rules can be used for budget plans. When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan. You can manually select ledger allocation rules to use for budget plans. Alternatively, you can use an allocation schedule that runs as part of a workflow process.

> [!NOTE]
> You can’t use intercompany ledger allocation rules for budget planning.






