---
title: Swiss Value Added [CH]
description: This article explains several enhancements that have been made to the Swiss VAT reporting features.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords:
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Swiss Value Added Tax

[!INCLUDE[prod_short](../../includes/prod_short.md)] includes the following enhancements to Swiss VAT reporting:  

- Automatic adjustment of VAT amounts for invoices, according to payment discounts.  
- Additional VAT exchange rates for invoices in foreign currencies.  

For more information about Swiss VAT reporting and coding requirements, see [Swiss VAT Information](https://www.estv.admin.ch/estv/en/home/value-added-tax.html). The information is available in French, German, and Italian, as well as English.  

## VAT Amounts and VAT Exchange Rates

According to local VAT laws, the VAT base amount for an invoice can be reduced by the payment discount if a discount is granted. To allow automatic VAT adjustment for a payment discount on an invoice, the **Adjust for Payment Discount** field is activated by default on the **General Ledger Setup** page. You can also activate this function in the VAT posting setup. For more information, see the General Ledger Setup table and the VAT Posting Setup table.  

### Currency Exchange Rates for VAT Reporting

For invoices in foreign currency, you must use the official exchange rate provided by the government for the VAT calculation itself. You can also set up additional exchange rates for VAT, which you can use for aspects of the invoice other than the VAT calculation. You can provide the correct government VAT exchange rate for each relevant foreign currency in the exchange rate setup for invoices. For more information, see the Currency Exchange Rate table.  

You can also adjust all VAT amounts in VAT entries that result from foreign currency transactions. When you activate the adjust VAT exchange rate function, VAT exchange rates are adjusted automatically. The positive differences that result from exchange rates are posted to exchange rate gain accounts. The negative differences that result from exchange rates are posted to exchange rate loss accounts. For more information, see the Adjust Exchange Rates batch job.  

Additional information, such as VAT rate and original currency amount, is transferred to the VAT entries. For more information, see the VAT Entry table.  

## Related information

[VAT Rates for Switzerland](vat-rates-for-switzerland.md)   
[Create and Print a Swiss VAT Statement](how-to-create-and-print-a-swiss-vat-statement.md)   
[Switzerland Local Functionality](switzerland-local-functionality.md)   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]