---
title: Issue Vendor Payments and Customer Bills (IT)
description: The vendor and customer bill pay feature supports SEPA-based formats in addition to Italian file formats.
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.keywords:
ms.search.form: 12102, 12175, 12176, 12178, 12180, 12181, 12182, 12184, 12185, 12186, 12190
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Issue Vendor Payments and Customer Bills

The vendor and customer bill pay feature supports SEPA-based formats in addition to Italian file formats. You can pay vendors according to the SEPA Credit Transfer standard and collect payment from customers according to the SEPA Direct Debit standard. The following procedure describes the process for sending a SEPA-based payment to a vendor. The steps are similar for collecting payment from a customer.  

Before starting the following procedure, make sure that information for your company's bank has been provided on the **Bank Account Card** page. On the card, include information for the following fields:  

- IBAN  
- SWIFT Code (optional)  
- Payment Export Format  
- SEPA CT Msg. ID No. Series  

In addition, there must be a posted purchased invoice against which you can send a payment.  

## To issue payment to a vendor  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.  
2. Select the vendor to which you want to send payment. On the **Payment** FastTab, in the **Payment Method Code** field, choose the **TRASFBANC** option.
3. Choose the **Bank Accounts** action.  
4. In the **Vendor Bank Account List**, select the vendor's bank account, and then choose the **Edit** action.
5. On the **Transfer** FastTab, specify information for the **IBAN** field.  
6. Choose the **OK** button.  
7. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Bill Card**, and then choose the related link.  
8. Choose the **New** action.  
9. On the **General** FastTab, enter information in the following fields: **Bank Account No.** of the vendor and **Payment Method Code**.  
10. Choose the **Suggest Payment** action.
11. Set filters, as appropriate, and then choose the **OK** button to run the batch job.  
12. Choose the **Create List** action.
13. Choose the **Yes** button to send the bill payment.  
14. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Bill List Issued**, and choose the related link.
15. Select the bill payment that you issued from the list, and then choose the **Edit** action. The **Vendor Bill List Sent Card** page opens.  
16. To export the payment information, choose the **Export Bill List to File** action. You can review the xml file that was sent.  

    1. Export to File (for standard SEPA format files)  
    2. Export Bill List to File  

You can review the .xml file before sending it. To review and fix errors, you can refer to the **File Export Errors** FactBox.  

## Related information

[Create SEPA Direct Debit Collection Entries and Export to a Bank File](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
