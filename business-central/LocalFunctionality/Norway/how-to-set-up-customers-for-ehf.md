---
title: Set Up Customers for EHF
description: To create Elektronisk Handelsformat (EHF) documents for customers in the public sector in Norway, you must add EHF information to the relevant customers.
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.keywords:
ms.search.form: 21, 459
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Set Up Customers for EHF
To create Elektronisk Handelsformat (EHF) documents for customers in the public sector, you must add EHF information to the relevant customers.  

This topic only describes fields that apply to EHF. For more information on setting up customers, in general, see [Register New Customers](../../sales-how-register-new-customers.md).  

## To set up a customer that uses Elektronisk Handelsformat  

1.  Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.  
2.  Open the customer that you want to enable for EHF.  
3.  On the **Invoicing** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Required. Enter the Global Location Number (GLN) for the customer.|  
    |**Account Code**|Enter the account code for the customer.<br /><br /> Customers in the public sector provide an account code when they place an order or requisition. Based on the value of this field, the account code is included in the EHF documents that you create in [!INCLUDE[prod_short](../../includes/prod_short.md)]. For more information, see Account Code.|  
    |**E-Invoice**|Select the check box to use electronic invoicing with this customer.|  
    |**Responsibility Center**|Make sure that the Responsibility Center that you have selected has a Country/Region Code specified.|  

These fields are specific to EHF. The values are used in all EHF documents that you create for this customer. For more information, see [EHF Electronic Invoicing in Norway](ehf-electronic-invoicing-in-norway.md).  

## Related information  
 [Create Electronic Documents for EHF](how-to-create-electronic-documents-for-ehf.md)   
 [Set Up EHF](how-to-set-up-ehf.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
