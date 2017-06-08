---
title: Publish journal lines and documents from Excel
description: This topic explains how to enter and publish lines for general journals from Microsoft Excel. It includes information about the various templates that you can use, depending on the type of transactions that you&quot;re entering.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a43bf66de7602aa9fb47925996ec5b979e1f8dac
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publish journal lines and documents from Excel

[!include[banner](../includes/banner.md)]


This topic explains how to enter and publish lines for general journals from Microsoft Excel. It includes information about the various templates that you can use, depending on the type of transactions that you're entering.

Users can enter and publish lines for financial journals from Microsoft Excel. After a user creates a journal, the **Open lines in Excel** button displays the templates that are available. Templates are designed to support specific scenarios, however not every combination of account type is supported in the journal. The following table shows the templates that are available and the account types which they support.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Supported account types**                                                                                             | **How to access the template**                                                          |
| Ledger journal lines     | Account: Ledger, Customer, Vendor, Bank Offset account: Ledger, Customer, Vendor, Bank Intercompany is supported.       | General journal                                                                         |
| Invoice register         | Account: Vendor Offset account: Ledger Intercompany isn't supported.                                                    | AP invoice register                                                                     |
| Invoice journal          | Accounts: Vendor Offset account: Ledger Intercompany is supported.                                                      | AP invoice journal                                                                      |
| Vendor invoice           |                                                                                                                         | Vendor invoice                                                                          |
| Customer invoice journal | Account: Customer Offset account: Ledger Intercompany is supported.                                                     | General journal                                                                         |
| Free text invoice        |                                                                                                                         | On the **Free text invoice** page, click **Open in Excel** (the Microsoft Office icon). |
| Fixed assets journal     | Asset to ledger, bank, customer, or vendor. Intercompany isn't supported.                                               | Fixed asset journal                                                                     |
| Vendor payment journal   | Account: Vendor Offset account: Ledger, Bank Intercompany is supported.                                                 | Vendor payment journal                                                                  |
| Customer payment journal | Account: Customer Offset account: Ledger, Bank Intercompany is supported.                                               | Customer payment journal                                                                |
| Project expense journal  | Account: Project, Ledger, Customer, Vendor Offset account: Project, Ledger, Customer, Vendor Intercompany is supported. | General journal Expense (under Project management and accounting)                       |

When the lines are published, they are validated to make sure that they comply with the rules that are set up in the financial journals. After the lines are published, users can edit or post the vouchers from Microsoft Dynamics 365 for Operations. 

To add financial dimensions to a template, additional changes are required. For additional information, see [Add dimensions to the Microsoft Excel template](/dynamics365/operations/dev-itpro/financial/add-dimensions-excel-templates). After dimensions are added to the entity, they are available in the Excel designer and can be added to the template.






