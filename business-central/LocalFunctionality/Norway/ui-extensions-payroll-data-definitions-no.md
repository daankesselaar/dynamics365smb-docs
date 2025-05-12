---
title: Payroll Data Definitions [NO]
description: The payroll data definitions extension makes it easy to exchange data with payroll service provider in Norway.
author: brentholtorf
ms.topic: article
ms.devlang: al
ms.search.keywords:
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# The Payroll Data Definitions Extension in the Norwegian Version

If your business uses the Huldt & Lillevik Lønn - Visma payroll service provider in Norway, the **Payroll Data Definitions (NO)** extension can help you quickly and accurately register payroll transactions from these providers. The extension contains data exchange definitions that enable you to import payroll transactions in files that the providers send to you. For more information about data exchange definitions, see [Set Up Data Exchange Definitions](../../across-how-to-set-up-data-exchange-definitions.md).   

## Getting Started

The first step is to map the types of payroll transactions to the general ledger accounts that you want to post them to in [!INCLUDE[prod_short](../../includes/prod_short.md)]. For example, you might want to post retirement plan contributions to an account named Pension, and the taxes paid on the contributions to an account named Pension Tax. This happens outside of [!INCLUDE[prod_short](../../includes/prod_short.md)], for example, you might use an Excel worksheet to visualize the mapping. Work with the payroll service provider to ensure that the file they export contains the mapping. Typically, you can find information about how to configure export files on the provider's website.  

After you install the extension, the next step is to specify the format for the payroll data file from the payroll service provider. To do that, go to the **General Ledger Setup** page and choose the provider in the **Payroll Trans. Import Format** field.  

## To import a payroll file

1.  Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.   
2.  Choose the journal to use, and then use the **Import Payroll File** action to import the data file from the payroll service provider.  

## Related information
[Norway Local Functionality](norway-local-functionality.md)   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
