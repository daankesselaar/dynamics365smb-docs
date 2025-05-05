---
title: Report 347 [ES]
description: Report 347 is a required annual report sent by all companies to the tax authorities to reflect the sales or purchases in a given period. 
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords:
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Report 347 in the Spanish Version
The **Report 347** report is a required annual report sent by all companies to the tax authorities to reflect the sales or purchases in a given period, based on **VAT Date**. This report also includes entries such as payment in cash that was received in the period. The **Report 347** report is generated in a format that is approved by the tax authorities. This file can be uploaded to the Spanish Tax Agency website or submitted on CD-ROM. For more information, see the [Spanish Tax Agency](https://www.agenciatributaria.es/AEAT.internet/en_gb/Inicio.shtml) website.  

## File Format for Report 347  
The file format for **Report 347** includes at least one responsible company, a deponent, and a customer/vendor register. A responsible company is a company that submits the information to the Spanish Tax Agency. Deponent information comes from the **Company Information** table and the request form. Customer information comes from the **Customer** table, the **Cust. Ledger Entry** table, and the **G/L Entry** table. Vendor information comes from the **Vendor** table and the **Vendor Ledger Entry** table.  

> [!NOTE]  
>  If there are no file records, the file is not created and an error message is displayed.  

## File Format Restrictions for Report 347  
Before creating **Report 347**, the following file format restrictions will be considered:  

- All amounts must be positive.  
- All text must be capitalized.  
- All alphanumeric fields must be left-aligned.  
- All numeric fields must be right-aligned.  
- If the company receives payments in cash that are over the predefined official threshold for these transactions, a four-digit year must be included. The year indicates when the invoices that are related to receivables were posted.  
- Special characters must be converted to standard characters.  
- If the field has no value, it will be blank for alphanumeric fields and populated with zeros for numeric fields.  

## Related information  
 [Spain Local Functionality](spain-local-functionality.md)   
 [Create Report 347](how-to-create-report-347.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
