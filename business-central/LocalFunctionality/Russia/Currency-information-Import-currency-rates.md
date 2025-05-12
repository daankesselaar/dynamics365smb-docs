---
title: Currency information in Russia
description: Russian enhancements include currency information for importing currency rates.
author: DianaMalina
ms.topic: article
ms.search.keywords:
ms.date: 11/06/2023
ms.reviewer: bholtorf
ms.author: soalex
ms.service: dynamics-365-business-central
---

# Currency information, Import currency rates

Local currency information for printing forms is specified in **General Ledger Setup**.

Used fields on the **General tab**:

- LCY Code
- Local currency description

### Import currencies

Go to **Company information**. Fill fields:

| Field                          | Description                                                  |
| ------------------------------ | ------------------------------------------------------------ |
| **Import Curr. Exch. Rates**   | Specifies if it's possible to run the Import Currency Exch. Rate batch job. |
| **Import Conflict Resolution** | Specifies what happens if a user runs the Import Currency Exch. rate batch job and there are conflicting exchange rates. |

Go to **Currency**. Оn the **General tab** fill fields for each currency:

| Field                    | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| **Import**               | Specifies if the currency has an imported exchange rate.     |
| **Ru Bank Code**         | Specifies the Russian bank code associated with the currency. |
| **Ru Bank Digital Code** | Specifies the Russian bank digital code associated with the currency. |

##### Import currency rates:

1. Go to Departments -> Financial management -> Periodic activities -> Currency -> Import currency rates.

2. Enter the start and end dates of the period for which you want to adjust the exchange rates.

## Related information

[Adjust Exchange Rates](Adjust-Exchange-Rates.md)  
[Russia Local Functionality](russia-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
