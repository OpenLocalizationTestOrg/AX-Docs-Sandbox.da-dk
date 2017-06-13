---
title: Take a cash discount outside the cash discount period
description: This article provides two scenarios that show how a cash discount can be taken even if the payment is made outside the cash discount period.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 15da62064521ec614764c42b57a20d32b110587a
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Take a cash discount outside the cash discount period

[!include[banner](../includes/banner.md)]


This article provides two scenarios that show how a cash discount can be taken even if the payment is made outside the cash discount period.

On June 28, April creates an invoice for 2,000.00 for vendor 3052. The invoice has a cash discount of 1 percent if the invoice is paid in 14 days.

## <a name="use-cash-discount-option--always"></a>Use cash discount option = Always
April creates a payment on July 1, which is after the discount date. April opens the **Settle transactions** page to view the transactions that can be settled. 

April marks the invoice for payment. No cash discount is taken, because the payment is after the discount date. However, the vendor has given April approval to take the cash discount anyway. Therefore, April changes the value in the **Use cash discount** field to **Always**.

| Mark     | Use cash discount | Voucher   | Account | Cash discount date | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Selected | Always            | Inv-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2,000.00                      | USD      | -1,980.00        |

Discount information appears at the bottom of the **Settle transactions** page.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/12/2015 |
| Cash discount amount         | -20.00    |
| Use cash discount            | Always    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | -20.00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Date to use for calculating discounts = Selected date
If both the invoice and the payment have been posted, the cash discount can still be taken when the transactions are settled on the **Settle transactions** page. April changes the value in the **Date to use for calculating discounts** field to **Selected date**. She then enters a date of June 28, which is in the cash discount period for the invoice. That date is used to calculate a cash discount for the transaction. On the **Settle open transactions** page, April sees that, by default, the full discount of 20.00 appears. The invoice line shows that the amount to settle is 1,980.00.

| Mark                     | Use cash discount | Voucher   | Account | Cash discount date | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Selected and highlighted | Normal            | Inv-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2,000.00                      | USD      | -1,980.00        |
| Selected                 | Normal            | APP-10030 | 3052    | 7/15/2015          | 7/15/2015 |         | 500.00                         | USD      | 500.00           |

Discount information appears at the bottom of the **Settle open transactions** page. The discount amount that is taken is 20.00, because the amount to settle for the invoice is the default amount, 1,980.00.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/12/2015 |
| Cash discount amount         | -20.00    |
| Use cash discount            | Normal    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | -20.00    |

April updates the value in the **Amount to settle** field to **500.00**. The value in the **Cash discount amount to take** field is calculated as **5.05**.

| Mark                     | Use cash discount | Voucher   | Account | Date      | Due date  | Invoice | Amount in transaction currency | Currency | Amount to settle |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Selected and highlighted | Normal            | Inv-10030 | 3052    | 6/28/2015 | 7/12/2015 | 10030   | 2,000.00                       | USD      | -500.00          |
| Selected                 | Normal            | APP-10030 | 3052    | 7/15/2015 | 7/15/2015 |         | 500.00                         | USD      | 500.00           |

Discount information appears at the bottom of the **Settle open transactions** page. The value in the **Cash discount amount to take** field is **5.05**, because the amount to settle for the invoice was changed to the payment amount, 500.00.

|                              |           |
|------------------------------|-----------|
| Cash discount date           | 7/12/2015 |
| Cash discount amount         | -20.00    |
| Use cash discount            | Normal    |
| Cash discount taken          | 0.00      |
| Cash discount amount to take | -5.05     |





