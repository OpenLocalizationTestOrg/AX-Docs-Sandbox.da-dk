---
title: Configure a line-item workflow
description: This topic explains how to configure a line-item workflow element.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2781a0344f1de5caf0031d7c3d5b88678be153a4
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="configure-a-line-item-workflow"></a>Configure a line-item workflow

[!include[banner](../includes/banner.md)]


This topic explains how to configure a line-item workflow element.

To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page. Then use the following procedures to configure the properties of the line-item workflow element.

## <a name="name-the-lineitem-workflow-element"></a>Name the lineitem workflow element
Follow these steps to enter a name for the line-item workflow element.

1.  In the left pane, click **Basic Settings**.
2.  In the **Name** field, enter a unique name for the line-item workflow element.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Specify whether the same workflow is used to process all line items
Follow these steps to specify whether the same workflow is used to process all the line items on a document.

1.  In the left pane, click **Basic Settings**.
2.  If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**. Then select the workflow to use to process the line items.
3.  If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**. Then follow these steps to define the set of conditions:
    1.  Click **Add**.
    2.  Select the condition in the table.
    3.  On the **Condition name** tab, enter a name for the set of conditions that you're defining.
    4.  Click **Add condition** to enter a condition.
    5.  Enter any additional conditions that are required.
    6.  To verify that the set of conditions that you entered is configured correctly, click **Test**. On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**. The system evaluates the record to determine whether it meets the conditions that you defined. Click **OK** or **Cancel** to return to the **Properties** page.

    On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.





