---
title: Setting up Subcontracting
description: Setting up Subcontracting

author: v-debapd

    
ms.topic: how-to
ms.devlang: al
ms.search.keywords: India, local, IN, English
ms.date: 04/01/2021
ms.author: bholtorf

ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Setting Up Subcontracting


Business Central has included **Subcontracting** Feature to Indian Localization.

Subcontracting process is very common in manufacturing organizations. Organizations adopt the job work process due to their capacity constraints, lack of resources or due to machine breakdowns. In Subcontracting, a delivery challan is used to send the raw items to the sub-contractor from the company. With some value addition by the sub-contractor, the finished items are sent back to the company.

While receiving the finished items in the company against a sub-contracting order, it is mandatory to apply received material against the delivery challan to knock off the raw items at sub-contractor end.

As far as the costing of finished item is concerned, it consists of raw material cost, sub-contracting cost along with the other charges such as freight etc. 

Raw items are taxable. Therefore, it is mandatory to follow the statutory requirement. As per this, the raw items sent to the sub contractor should return back within specified return period otherwise GST liability will be created. This feature enables you to create the GST liability and also lets you reverse the GST liability after receiving the raw items from sub- contractor

### Multiple subcontracting orders

Subcontracting feature also enables you to send the raw items to subcontracting vendor for multiple subcontracting orders against a single Delivery Challan. Delivery Challan will show the details of all subcontracting orders for which the raw material components have been sent to subcontracting vendor.

### Stock register for job work

Stock register for job work gives the details of delivery challan sent to the subcontractor. This register shows all the transaction against a delivery challan and at any movement it will also show the status of delivery challan along with GST liability if any.

## Setting up subcontracting 

Following setups are required for Subcontracting:

- [Subcontracting Location setup](subcontracting-001-basic-setup.md#subcontracting-location-setup)
- [Subcontracting Vendor setup](subcontracting-001-basic-setup.md#setting-up-subcontracting-vendor)
- [Subcontracting Item setup](subcontracting-001-basic-setup.md#setting-up-subcontracting-item)
- [Job Work Return Period](subcontracting-001-basic-setup.md#setting-up-job-work-return-period)
- [Source Code Setup](subcontracting-001-basic-setup.md#setting-up-source-code)
- [General Ledger Setup](subcontracting-001-basic-setup.md#setting-up-general-ledger-setup)
- [Work Center](subcontracting-001-basic-setup.md#setting-up-work-center)
- [Routing](subcontracting-001-basic-setup.md#setting-up-routing)
- [GST liability no series setup](subcontracting-001-basic-setup.md#gst-liability-no-series-setup)


## Subcontracting location setup

You need to create a set up for subcontracting location. Raw item needs to be transferred from company location to subcontracting location.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.
2. On the **Tax Information** FastTab, enable the boolean in the **Subcontracting Location** field to make this location as a **Subcontracting Location**.

## Setting up subcontracting vendor 

You need to set up a vendor as a subcontractor. Same vendor can be the prime vendor as well as a subcontracting vendor. Each subcontracting vendor needs to be attached with the subcontracting location.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Vendor**, and then choose the related link.
2. On the **Tax Information** FastTab, enable the boolean in the **Subcontractor** field to make this vendor as a **Subcontractor**.
3. Select the subcontracting location by clicking on **Vendor Location** look up field. 
4. Enter the Commissioner’s Permission No. which is mandatory for the subcontractor. 

## Setting up subcontracting item 

The finished item needs to be identified as a subcontracting item.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Item**, and then choose the related link.
2. On the **Cost & Posting** FastTab, enable the boolean in the **Subcontracting** field to make this Item as a subcontracting item.
3. Select the subcontracting location by clicking on **Sub. Comp. Location** look up field. This is the location from where you will send the raw material to the subcontractor. 


## Setting up job work return period

As per statutory requirement, if the taxable item does not return within a specified period, then GST liability should be created against the subcontractor. Therefore, GST liability exists only after the completion of job work Return period. 

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Inventory Setup**, and then choose the related link.
2. On the **Numbering** FastTab, enter the return period for which you want to create GST liability in the **Job Work Return Period** field.
3. Select the **Sub. Component Location** from lookup list. This sub component location will be used to transfer the raw items to the subcontracting location through delivery challan.

## Setting up source code

As per statutory requirement, you need to define the source code in the source code set up window. This source code is mandatory if subcontractor does not Return the item within job work Return period, then to create the GST liability. Source code is also required if any subcontracting item is received after the job work Return period.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Source Code setup**, and then choose the related link.
2. On the **General** FastTab, select Source code in the **GST Receipt – Job Work** field. 
3. Select Source code in the **GST Liability – Job Work** field.


## Setting up general ledger setup

You need to create a new account in the chart of account which will be used for booking GST expenses while creating the GST liability in case of non-receipt of subcontracting items within the job work return period.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **General Ledger setup**, and then choose the related link.
2. On the **Tax Information** FastTab, select **GST Expense –Job Work** account in the **GST Expense Acc. - Job Work** field.
        

## Setting up work center

You need to setup the work center for the subcontracting vendor. On the work center, you can also set up the unit cost of job work.

1.  Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Work Center**, and then choose the related link.
2. On the Posting tab, select **subcontracting vendor** in the **Subcontractor No.** field.

## Setting up routing

You need to create a Routing for finished item. Routing defines the sequence of the operations required to manufacture the finished item.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Routing**, and then choose the related link.
2. On the Lines tab, select **subcontracting work center no.** in the **Work Center No.** field. 
3. On the  Lines tab, enter the job work charges in the **Unit Cost Per** field.


## GST liability no series setup

No. series for GST liability invoice is setup on location master. You can define location wise number series for GST liability invoices.

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.
2. On the **Tax Information** FastTab, select **No. series code** in the **GST Liabilty Invoice** field.

## Related information 
[Subcontracting Transactions](Subcontracting-Transactions.md)







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
