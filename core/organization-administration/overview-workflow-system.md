---
title: Workflow system overview
description: This topic describes the workflow system in Microsoft Dynamics 365 for Operations.
author: sericks007
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 142f6f122172f717733db6f39b964c3f6f2e2f77
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="workflow-system-overview"></a>Workflow system overview

[!include[banner](../includes/banner.md)]


This topic describes the workflow system in Microsoft Dynamics 365 for Operations.

<a name="what-is-workflow"></a>What is workflow?
-----------------

The term *workflow* can be defined in two ways: as a system and as a business process.
### <a name="workflow-is-a-system"></a>Workflow is a system

Workflow is a system that is installed with Dynamics 365 for Operations and runs on the Application Object Server (AOS). The workflow system provides functionality that you can use to create individual workflows, or business processes.

### <a name="workflow-is-a-business-process"></a>Workflow is a business process

A workflow represents a business process. It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document. For example, the following illustration shows a workflow for expense reports. 

![Workflow with elements that are assigned to users](./media/workflow_user.gif) 

To better understand this workflow, suppose that Sam submits an expense report for USD 7,000. In this scenario, Ivan must review the receipts that Sam routes to him. Then Frank and Sue must approve the expense report. Now suppose that Sam submits an expense report for USD 11,000. In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.

## <a name="benefits-of-using-the-workflow-system"></a>Benefits of using the workflow system

There are several benefits of using the workflow system in your organization:
-   **Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed. By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.
-   **Process visibility** – You can track the status, history, and performance metrics of workflow instances. This helps you determine whether changes should be made to the workflow to improve efficiency.
-   **Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.


## <a name="workflow-content"></a>Workflow content

+ [Workflow architecture](workflow-system-architecture.md)
+ [Workflow elements](workflow-elements.md)
+ [Workflow actions](workflow-actions.md)
+ [Create a workflow](create-workflow.md)
+ [Configure workflow properties](configure-workflow-properties.md)
+ [Configure a manual task in a workflow](configure-manual-task-workflow.md)
+ [Configure an automated task in a workflow](configure-automated-task-workflow.md)
+ [Configure an approval process in a workflow](configure-approval-process-workflow.md)
+ [Configure an approval step in a workflow](configure-approval-step-workflow.md)
+ [Configure a manual decision in a workflow](configure-manual-decision-workflow.md)
+ [Configure a conditional decision in a workflow](configure-conditional-decision-workflow.md)
+ [Configure a parallel activity in a workflow](configure-parallel-activity-workflow.md)
+ [Configure a parallel branch in a workflow](configure-parallel-branch-workflow.md)
+ [Configure a line-item workflow](configure-line-item-workflow.md)

