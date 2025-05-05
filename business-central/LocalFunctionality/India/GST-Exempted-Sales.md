---
title: GST Exempted Sales
description: GST Exempted Sales

author: v-debapd

    
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: India, local, IN, English
ms.date: 04/01/2021
ms.author: bholtorf

ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# GST Exempted Sales


Sales made to an exempted customer are known as exempt sales. GST customer type shall be selected as Exempted. No GST is computed on such transactions. 

Process of sale to unregistered customer has been explained in this document.

## Create a sales invoice or credit memo

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoice** or **Sales Credit Memo**, and then choose the related link.
2. Select **Customer** on **Sales Invoice** or **Sales Credit Memo** header, GST customer type should be **Exempted**.
3. Select **G/L Account** or **Item Code** on **Sales Invoice** or **Sales Credit Memo** line. 

For example, there is a sales invoice and a sales credit memo for INR 10,000.

- GL Entries for Exempted Sales, will be as following:

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Customer Account**|10,000|  
    |**Sales or Services Account**|-10,000| 

- GL Entries for Sales Credit Memo for Exempted Sales, will be as following:

    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Customer Account**|-10,000|  
    |**Sales or Services Account**|10,000| 









## Related information 
[Sale to Registered and Unregistered Customer](GST-Sale-to-Registered-Unregistered-Customer.md)































[!INCLUDE[footer-include](../../includes/footer-banner.md)]