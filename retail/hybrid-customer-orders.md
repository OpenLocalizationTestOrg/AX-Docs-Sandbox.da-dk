---
title: Hybrid customer orders
description: A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: eb6ba7cfdf098671192d4d6e73119f96b287c437
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid customer orders

[!include[banner](includes/banner.md)]


A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.

In Microsoft Dynamics 365 for Operations - Retail, you can select either carry out all products or carry out selected products for a customer order. The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created. The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines. For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:

-   If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.
-   If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.

If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method. In that case, the downstream flow of the operation continues as usual. However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines. On that screen, you can select multiple lines at once for setting the delivery method. When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.

<a name="see-also"></a>See also
--------

[Customer orders overview](customer-orders-overview.md)




