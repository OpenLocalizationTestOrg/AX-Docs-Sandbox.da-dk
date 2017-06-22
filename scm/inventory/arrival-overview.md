---
title: Arrival overview
description: This topic provides information about the Arrival overview feature. The Arrival overview page is part of this feature and provides an overview of all items that are expected to arrive as incoming items.
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d6910d3a960c22f8515276ef9a2229957e5d6f11
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2017


---

# <a name="arrival-overview"></a>Arrival overview

[!include[banner](../includes/banner.md)]


This topic provides information about the Arrival overview feature. The Arrival overview page is part of this feature and provides an overview of all items that are expected to arrive as incoming items.

The **Arrival overview** page provides an overview of all expected incoming items. It also shows arrivals that can be initialized based on the overview. This topic focuses on the receiving process.

## <a name="business-scenario"></a>Business scenario
Consider the following scenario in the inbound processes. 

[![Business scenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png) 

Sammy, a receiving clerk, wants to know what is expected to be received on the current day. On the **Arrival overview** page, Sammy can get an overview of the current tasks, and a rough estimate of quantities, volume, weight, different order types, and so on. Later, a delivery arrives at one of the inbound docks, and Sammy receives a list of the delivery. On the **Arrival overview** page, Sammy can perform the following tasks:

-   Identify the matching receipt order, and register the receipt as **In progress**. The lines that are required for a registration are automatically generated, and the receipt can be monitored, even though the transactions haven't yet been posted as **Registered**.
-   Access the appropriate arrival journal reference (that is, the **Item arrival** journal or the **Production input** journal), and identify journals that are ready for a product receipt update.

## <a name="arrival-overview-page"></a>Arrival overview page
To open the **Arrival overview** page, click **Inventory management** &gt; **Inbound orders** &gt; **Arrival overview**. You can view a list of orders that are expected to be received. The overview is divided into a header and lines. The header information is grouped by the order type, expected receipt date, and delivery destination. When a header line is selected for arrival, all the detail lines that are related to the receipt reference are selected for arrival in the line details part of the page. When all related journal lines have been posted, this information isn't shown.

### <a name="arrival-overview-profiles"></a>Arrival overview profiles

The **Arrival overview** page provides an overview of items that are expected to arrive and the date when they are expected to arrive. As part of the arrival process, multiple sets of personal settings can be used. Individual users can define their personal settings on the **Arrival overview profiles** page.

### <a name="set-up-item-arrival"></a>Set up item arrival

In our example, Sammy wants to set up a new computer at a location that will be used to receive finished goods that come from production at Site 1. On the **Arrival overview profiles** page, Sammy creates a new setup that is named **Site 1 production** and specifies the following settings.

1.  On the **Arrival options** FastTab, in the **Range** field group, enter information about a day interval and the warehouses to include in the overview.
2.  On the **Arrival options** FastTab, in the **Journal** field group, enter a receiving warehouse, a location, and a journal name (item arrival/production input).
3.  On the **Arrival query details** FastTab, in the **Site** field group, in the **Restrict to site** field, enter a site to limit the view in the overview area.
4.  On the **Arrival query details** FastTab, in the **Transaction types shown** field group, set the **Production orders** option to **Yes**.
5.  On the **Arrival query details** FastTab, in the **Miscellaneous** group, set the **Update on startup** option to **Yes** if the view should be automatically updated at startup. Set the **Update on range change** option to **Yes** if the view should be automatically updated when range values are changed.

For this example, the **Arrival overview profile name** field on the **Arrival options** FastTab of the **Arrival overview** page is set to **Site 1 production**.

### <a name="prerequisites-for-arrival-journals"></a>Prerequisites for arrival journals

To automatically create arrival journals from the **Arrival overview** page, you must define appropriate information in the **Journal** field group on the **Arrival options** FastTab.

-   You must specify a journal name to create a journal. 

[![Specifying a journal name](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   If you specify values in the **Warehouse** and **Location** fields, those values are applied on the journal lines. If you don't specify values, the system uses the values from the dimension that is specified on the inventory transactions.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Items that are received from one expected receipt order

On the **Receipts** FastTab, Sammy selects a line and then clicks **Start arrival**. All related lines that are in the specified range and that have a quantity to register are automatically selected. An item arrival journal is generated that has a match between the expected receipt order and the journal. The quantity is automatically initialized on all lines that are created.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Items that are received from more than one expected receipt order

On the **Receipts** FastTab, Sammy selects multiple lines and then clicks **Start arrival**. An item arrival journal is generated that has a match between all the expected receipt orders and the journal. All lines are created on one item arrival journal header, and the quantity is automatically initialized.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Receive items from one or more expected receipt orders

#### <a name="view-information"></a>View information

To get an overview of expected receipts in a date interval, Sammy enters the following information in the fields on the **Arrival options** FastTab on the **Arrival overview** page and then clicks **Update** to update the view:

-   Arrival overview profile name: **Inquiry**
-   Show lines: **All**
-   Days back: (Blank)
-   Days forward: **0**
-   Warehouses: **GW, MW**

Sammy can view the following information:

-   All related receipt orders for the system date and an infinite number of days back from it (the **InventTrans.StatusDate** interval), and receipts to warehouses GW and MW, regardless of status.
-   Detailed line information for more than one order. Sammy can select multiple header lines in the overview and then click **Show all selected** to view all the corresponding line detail information for all selected orders.
-   Information about a specific purchase order. To show only information that is related to a specific reference number in the overview, Sammy can enter an account number in the **Account number** field and an order number in the **Reference number** field.
-   An overview of the registration tasks that are due for all the order lines that an item arrival journal has been created for but hasn't yet been posted. To view this information, Sammy can select **In progress** in the **Show lines** field.

### <a name="update-journals"></a>Update journals

To register one or more order lines that are due to be processed, Sammy can select the lines in the overview grid or in the line grid, and then click **Journals** &gt; **Show arrivals from receipts**. The item arrival headers that match the lines are shown. To purchase order product receipt update the registered items, Sammy can access the item arrival journal headers that are ready for update. To access these item arrival journal headers, he clicks **Journals** &gt; **Product receipt ready journals**. All the header lines that are ready for product receipt update in the specified warehouse range are shown. (The header lines that are shown aren't related to the day interval).

### <a name="start-an-arrival-registration"></a>Start an arrival registration

By selecting multiple lines on the **Arrival overview** page, Sammy can start an arrival of more than one receipt reference. When he selects a line from the receipts overview, the corresponding line details are selected. If a quantity for registration exists, the **Start arrival** button is available. Sammy can use two methods to start the arrival registration:

-   To filter the page so that it shows only records that meet specific criteria, in the **Vendor reference** field, scan a reference number from a vendor, such as the bar code for a delivery note.
-   In the overview part or the details part of the **Arrival overview** page, manually select or cancel the selection of records for arrival registration. Then, when Sammy clicks **Start arrival**, the selected records are automatically created in an item arrival journal. The records include line information, and all unique field information is assigned.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Update arrival information and process a product receipt
When all goods have been registered, the warehouse manager or purchasing manager can update the received items with a product receipt to add the physical cost. To update arrival information and post a product receipt, follow these steps.

1.  Click **Inventory management** &gt; **Inbound orders** &gt; **Arrival overview**.
2.  On the **Arrival overview** page, click **Journals** &gt; **Product receipt ready journals** to show a list of the journals that are ready for product receipt update.
3.  Select the journals that must be updated, and then click **Functions** &gt; **Product receipt**.
4.  On the **Posting** page, enter the product receipt number, if it isn't already available on the journal, and then click **OK** to process the product receipt.

## <a name="summary"></a>Summary
The **Arrival overview** page can help the warehouse manager and warehouse workers achieve an overview of expected work that must be done as part of an inbound process. The page can also be used to start the item arrival process, to help guarantee that items are tracked at the first entry into the warehouse.




