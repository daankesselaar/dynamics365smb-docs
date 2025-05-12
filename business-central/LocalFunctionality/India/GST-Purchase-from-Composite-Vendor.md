---
title: Purchase from Composite Vendor or Purchase of exempted goods and services with no GST Impact
description: Purchase from Composite Vendor or Purchase of exempted goods and services with no GST Impact

author: v-debapd

    
ms.topic: how-to
ms.devlang: al
ms.search.keywords: India, local, IN, English
ms.date: 04/01/2021
ms.author: bholtorf

ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Purchase from Composite Vendor or Purchase of Exempted Goods and Services with No GST Impact


A composite vendor is a vendor whose aggregate turnover in a financial year does not exceed fifty lakh rupees and has opted for composition scheme. A composite vendor neither collects tax from the recipient of supplies nor passes on any credit of input tax. Hence, no GST is computed if the purchases are made from a composite vendor. 

A composite vendor has to register himself with the GST authorities and hence registration no. is mandatorily mentioned in the vendor card, if the vendor type is selected as composite. State code is also mandatory. No GST entries are generated for a composite vendor, as a composite vendor is not entitled to collect any tax from the customers. 

Process for purchases from a composite vendor has been explained in this document.

## Create a purchase invoice

1. Choose the ![Search for Page or Report.](image/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoice**, and then choose the related link.
2. Select **Vendor** on **Purchase Invoice** header, GST vendor type should be **Composite** or **Exempted**.
3. Select **G/L Account**, **Item Code**, **Fixed Asset** or **Charge (Item)** on **Purchase Invoice** line.

For example, invoice will be issued for INR 10000 on which there is no GST is charged.

- GL Entries will be as following:
    
    |Particulars|Amount|
    |----------------------------------|---------------------------------------|  
    |**Purchase or Services Account**|10000|  
    |**Vendor Account**|-10000|








## Related information 
[Purchase from Registered Vendor](GST-Purchase-from-Registered-Vendor.md)































[!INCLUDE[footer-include](../../includes/footer-banner.md)]
