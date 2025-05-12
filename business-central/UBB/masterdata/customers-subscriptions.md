---
title: Usage based billing customers and subscriptions 
description: You can use customer subscriptions in usage based billing.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.keywords: 
ms.search.form: 
ms.date: 08/14/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Usage based billing customers and subscriptions

In addition to the usage data that changes per import, there's also data that's more like master data because it doesn't change. This master data includes the customers for whom you import usage data, and the subscriptions that link the service commitments to bill. For customers, this data is helpful but not required, whereas without a subscription you can't bill usage data.

## Usage data customers

The **Usage Data Customers** page displays the customers you process usage data for. For [Usage data suppliers](suppliers.md), use the **Create customers** field to specify whether to create usage data customers when you import usage data. To learn more, go to [Create customers based on usage data](#create-customers-based-on-usage-data). Because the entries are based on usage data and thus represent the supplier's data, the entries might differ from the master data in [!INCLUDE [prod_short](../../includes/prod_short.md)]. Therefore, you can create a link based on the customer. This data isn't required to process and bill usage data. The page just helps clarify things.

The **Supplier No.** field helps you identify the supplier that records belong to. The **Customer No.** field lets you link to the master data. Usage based billing customers that aren't linked to a customer display in a teal colored font. Entries that display in a black font are linked. The **Supplier Reference** field contains the unique ID of the customer at the supplier. This value contains a link to the [usage data supplier references](references.md) of the type **Customer** that's automatically created when you process usage data.

### Create customers based on usage data

On the **Usage Data Suppliers** page, you can use the **Settings** action to specify import settings for a supplier on the **Generic Import Settings** page. If you turn on the **Create Customers** toggle, customers that belong to the usage data are created <!--when? when you import data?-->. To learn more, go to [Usage data customers](#usage-data-customers). The information from the usage data is used to create the following data records:

* Supplier No.
* Supplier description
* Customer ID as supplier reference

## Usage data subscriptions

The **Usage Data Subscriptions** page displays the subscriptions that belong to the usage data to process. Similar to creating customers, on the import settings for a [usage data supplier](suppliers.md), you can use the **Create Subscriptions** toggle to specify whether to create a subscription when you import usage data or when you process it. To learn more, go to [Create subscriptions based on usage data](#create-subscriptions-based-on-usage-data). These entries represent the supplier's data regarding the customer's subscriptions. This data is required to process and bill usage data. If the data isn't created automatically for the supplier, you must create it by some other means. We recommend that you turn on the **Create Subscriptions** toggle so let [!INCLUDE [prod_short](../../includes/prod_short.md)] create the usage data subscriptions.

Use the **Supplier No.** field to identify the supplier that records belong to. Use the **Extend Contract** action to link subscriptions to the customer and the service object. To learn more, go to [Extend contract](../processing-usage-data/extend-contract.md) and [Linking subscription with service object](../processing-usage-data/connect-subscription-service-object.md). Subscriptions that aren't associated with a service object display in a teal font. Subscriptions that display in a black font are linked. The **Supplier Reference** field contains the unique ID of the subscription at the supplier. This value contains a link to the [usage data supplier references](references.md) of the type **Subscription** that's automatically created when you process usage data.

### Create subscriptions based on usage data

If you set up the import settings for the supplier to create subscriptions that belong to the usage data, the information is used to create records. To learn more, go to [Usage data subscriptions](#usage-data-subscriptions).

* Supplier No.
* Customer ID
* Supplier reference (as ID of the subscription)
* Subscription Name
* Subscription Description
* Subscription Start Date
* Subscription End Date
* Product ID
* Product Name
* Unit of Measure
* Quantity

## Related information

[Usage data suppliers](suppliers.md)  
[Usage data supplier references](references.md)  
[Linking subscription with service object](../processing-usage-data/connect-subscription-service-object.md)  
