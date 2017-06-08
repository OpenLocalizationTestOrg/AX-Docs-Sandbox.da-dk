---
title: Income statement financial report
description: This article describes the default report for income statements. It also describes the building blocks that are associated with this report.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1773a36ab58f1b24c544c08dc1c48039513e28d9
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="income-statement-financial-report"></a>Income statement financial report

[!include[banner](../includes/banner.md)]


This article describes the default report for income statements. It also describes the building blocks that are associated with this report. 

<a name="default-income-statement-report"></a>Default income statement report
-------------------------------

| Default report             | What it does                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Income Statement – Default | Provides a view of the organization’s profitability for the current period and also for the year to date. |

## <a name="building-blocks"></a>Building blocks
The income statement financial report uses the following building blocks.

| Default report             | Row definition                     | Column definition          |
|----------------------------|------------------------------------|----------------------------|
| Income Statement - Default | Summary Income Statement - Default | Periodic and YTD - Default |

### <a name="row-definition"></a>Row definition

The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement. The Main Account Category dimension is used to build this row definition. Therefore, anyone can generate the report without having to make any modifications.

### <a name="column-definition"></a>Column Definition

The column definitions contain different types of columns to provide different levels of detail and financial data.

-   **Periodic and YTD – Default column types:**
    -   **DESC** – The description from the row definition
    -   **FD** – Financial data for the current period
    -   **FD** – Financial data for the year to date

 

<a name="see-also"></a>See also
--------

[Financial reporting](financial-reporting-getting-started.md)

[View financial reports](view-financial-reports.md)

[Dynamics Financial Reportign Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)




