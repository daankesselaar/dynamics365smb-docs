---
title: Input Service Distribution Process
description: Input Service Distribution Process

author: v-debapd

    
ms.topic: article
ms.devlang: al
ms.search.keywords: India, local, IN, English
ms.date: 04/01/2021
ms.author: bholtorf

ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Input Service Distribution Process


GST Input Service Distribution functionality is used to distribute CGST & SGST/IGST paid on Input services (Input Tax Credit) to other locations.

## GST distribution process

1. Choose the ![img.](image/search.jpg)icon, enter **GST Distribution List**, and then choose the related link.
2. Following fields should be filled on the General Tab

    |Field|Description|
    |----------------------------------|---------------------------------------|  
    |**No.**|Specifies the unique number for the document.| 
    |**ISD Document Type**|Specifies the relevant document type of the transaction.|
    |**From Location Code**|Specify the location code from where input credit will be distributed.|  
    |**Posting Date**|Specifies the posting date of the document.|
    |**Distribution Document Type**|Specifies the type of the document.|
    |**Dist. Credit Type**|Specifies the distribution credit type.|
    |**Total Amount Applied for Dist.**|Specifies the total amount which is applied for distribution.|
    |**Distribution Basis**|Specifies the distribution basis.|

3. Following fields should be filled on the GST Distribution Line Tab

    |Field|Description|
    |----------------------------------|---------------------------------------|  
    |**Posting Date**|Specifies the posting date of the document.|  
    |**From Location Code**|Specifies the location code from where input credit will be distributed.|  
    |**From GSTN No.**|Specifies the GST registration number of the location defined in the **From Location Code**.|
    |**To Location Code**|Specifies the location code to which input credit will be distributed.|
    |**To GSTN No.**|Specifies the GST registration number of the location defined in the **To Location Code**.|
    |**Distribution Jurisdiction**|Specifies the distribution jurisdiction, e.g. Interstate, Intrastate.|
    |**Distribution %**|Specifies the distribution percentage.|
    |**Distribution Amount**|Specifies the distribution amount.|
    |**Rcpt. Credit Type**|Specifies whether the input credit is available or not.|

4. After selecting all relevant values, click on Related on ribbon -> Apply Entries -> select the relevant entries for distribution ->  select relevant dimensions and post.

## Inter-state and intra-state distribution of GST under input service distribution

1. GL Entries for an Intra-state Distribution of Invoice to Recipient location (GST Credit is available for both the distributor and recipient locations). For example, service invoice issued for INR 1000 and CGST 9% and SGST 9% has been charged on the invoice, and the input service credit has been distributed to the recipient location.

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**SGST Receivable Account**|90|
    |**CGST Receivable Account**|90|
    |**SGST Receivable Account (Dist.)**|-90|
    |**CGST Receivable Account (Dist.)**|-90|
    

2. GL Entries for an Interstate Distribution of Invoice Recipient location (GST Credit is available for both the distributor and recipient locations). For example, service invoice issued for INR 1000 and IGST 18% has been charged on the invoice, and the input service credit has been distributed to the recipient location.

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**IGST Receivable Account**|180|
    |**IGST Receivable Account (Dist.)**|-180|

3. GL Entries for an Intrastate Distribution of Invoice to Recipient location (GST Credit is not available for both the distributor and recipient locations). For example, service invoice issued for INR 1000 and CGST 9% and SGST 9% has been charged on the invoice, and the expense has been distributed to the recipient location.

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Freight**|180|
    |**GST Expense Account**|-90|
    |**GST Expense Account**|-90|

4. GL Entries for an Interstate Distribution of Invoice to Recipient location as Input Tax Credit (GST Credit is not available for both the distributor and recipient locations). For example, service invoice issued for INR 1000 and IGST 18% has been charged on the invoice, and the expense has been distributed to the recipient location.
  
    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Postage**|180|
    |**GST Expense Account**|-180|
    
5. GL Entries for an Intrastate Distribution of Credit Memo to Recipient location (GST Credit is available for both the distributor and recipient locations). For example, purchase credit memo has been raised for INR 1000 and CGST 9% and SGST 9% has been charged on the invoice, and the input service credit has been distributed to the recipient location.

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**SGST Receivable Account (Dist.)**|90|
    |**CGST Receivable Account (Dist.)**|90|
    |**SGST Receivable Account**|-90|
    |**CGST Receivable Account**|-90|

6. GL Entries for an Interstate Distribution of Credit Memo to Recipient location (GST Credit is available for both the distributor and recipient locations). For example, purchase credit memo has been raised for INR 1000 and IGST 18% has been charged on the invoice, and the input service credit has been distributed to the recipient location.

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**IGST Receivable Account (Dist.)**|180|
    |**IGST Receivable Account**|-180|

7. GL Entries for an Intrastate Distribution of Credit Memo to Recipient location (GST Credit is not available for both the distributor and recipient locations). For example, purchase credit memo has been raised for INR 1000 and CGST 9% and SGST 9% has been charged on the invoice, and the expense has been distributed to the recipient location.

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Postage**|-180|
    |**GST Expense Account**|90|
    |**GST Expense Account**|90|
    
8. GL Entries for an Interstate Distribution of Credit Memo to Recipient location as Input Tax Credit (GST Credit is not available for both the distributor and recipient locations). For example, purchase credit memo has been raised for INR 1000 and IGST 18% has been charged on the invoice, and the expense has been distributed to the recipient location.


    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Postage**|-180|
    |**CGST Expense Account**|180|



## Related information 
[GST Input Service Distribution Transaction](GST-Input-Service-Distribution-Transaction.md)







[!INCLUDE[footer-include](../../includes/footer-banner.md)]