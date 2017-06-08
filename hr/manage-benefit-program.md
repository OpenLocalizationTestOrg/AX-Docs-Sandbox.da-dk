---
title: Define and manage a benefits program
description: Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers&quot; compensation plans that an organization offers or processes for its workers. This article provides information about how to set up an manage benefits.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1d972f2d6bacf6f60ab3ce3bab2fcfaeb8d2e524
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Define and manage a benefits program

[!include[banner](includes/banner.md)]


Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers. This topic provides information about how to set up an manage benefits.

<a name="benefit-setup"></a>Benefit setup
-------------

Before workers can be enrolled in benefits, you must create the elements of each benefit. These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details. Many of these settings can be adjusted when workers are later enrolled in the benefit. For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan. 

[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Benefit elements
Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.

-   **Type** – A collection of plans for a specific benefit, such as medical or parking.
-   **Plan** – A specific benefit that is contracted from a provider.
-   **Option** – The coverage level, such as employee only, or employee and spouse/partner.

For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers. For each plan, the organization can offer different options. For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary. Each combination of a plan and options becomes a benefit that workers can enroll in. 

[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Eligibility
Many factors determine worker eligibility for the various types of benefits that an employer offers. When you create a benefit in Microsoft Dynamics 365 for Operations, you can set the type of eligibility that applies to that benefit. 

You can make a benefit available to all workers. For example, some companies offer parking passes to all employees as a fringe benefit. When you create this benefit, you set the eligibility to **All workers are eligible**. 

For other benefits, such as garnishments and tax levies, eligibility doesn't apply. Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**. 

Finally, benefit eligibility can be rule-based. For example, a company offers two types of life insurance benefit to employees. Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan. In Dynamics 365 for Operations, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.

## <a name="enrollment"></a>Enrollment
After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits. You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process. 

Sometimes, an organization stops offering certain benefits. In this case, you must update the benefit and the workers who are enrolled in. Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time. You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage. 

Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.

<a name="see-also"></a>See also
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)




