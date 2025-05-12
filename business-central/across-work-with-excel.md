---
title: Viewing and editing in Excel from Business Central
description: Learn how to open pages in Microsoft Excel from Business Central for better data analysis.
author: jswymer
ms.topic: concept-article
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/16/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# View and edit in Excel from Business Central

With pages that display a list of records in rows and columns, such as a list of customers, sale orders, or invoices, you can export the list to Microsoft Excel and view it there. Depending on the page, you have two options for viewing in Excel. Both are available from the **Share** icon ![Share a page in another app.](media/share-icon.png) at the top of a page. You can either select the **Open in Excel** action or the **Edit in Excel** action on the page. This article explains the two actions.

## Open in Excel

With the **Open in Excel** action, you can make changes to the records in Excel, but you can't publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)]. You can only save the changes to the Excel file, without affecting data in [!INCLUDE[prod_short](includes/prod_short.md)].

- Excel respects filters on the page that limit the records shown. The Excel workbook has the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].
- This action works on both Windows and macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

<!-- 
> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default. However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.-->

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> In Excel, whole numbers in columns will have a decimal symbol at the end (like a period `.` or comma `,`) even though the decimal symbol isn't shown in Business Central. The decimal symbol depends on your device's region settings. For example, `10` in Business Central could appear as `10.` or `10,` in Excel. You can change the format in Excel by selecting the values, then selecting <kbd>Ctrl</kbd>+<kbd>1</kbd>. To learn more about changing the number format in Excel, go to [Format numbers](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).

## Edit in Excel

The **Edit in Excel** action is available on most lists, but not all. With the **Edit in Excel** action, you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)]. When Excel opens, the **Excel Add-in** pane displays.

- With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook has almost the same records and columns.
- To get the latest data from [!INCLUDE[prod_short](includes/prod_short.md)], choose **Refresh** in the Excel Add-in pane.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### First-time sign-in

The **Edit in Excel** action requires that the Business Central add-in is installed in Excel. In some cases, your administrator might set up the add-in to install automatically for you. In this case, you just have to sign in to Business Central in the **Excel Add-in** pane with your user name and password. Otherwise, the **New Office Add-in** pane opens. To install the add-in, choose **Trust this add-in**, which installs the add-in directly from the Office Store.

If the add-in doesn't install, either contact your admin or try to install it manually. For more information, see [Install the add-in manually for your own use](admin-deploy-excel-addin.md#install).

### Work across environments and companies

You can switch the company that you're working with. To switch a company, select the **Options** icon ![Excel add-in options.](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.  

> [!IMPORTANT]
> When changing the company, make sure that the **Environment** field is not empty. If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.  

If you make changes to the add-in, you must reload it to update the connection. To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the upper-right corner of the add-in. If you can't load the add-in, talk to your administrator. If you're the administrator, see [Get the Business Central add-in for Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> The add-in works with Excel for the web (online) from any device as long as you use a supported browser. It also works with the Excel app for Windows (PC), but not for macOS.
>
> For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the web client. For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Business Central add-in for Excel in Business Central on-premises](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### Limits when using Excel for the web

When **Edit in Excel** is used on list pages for tables with many columns, the resulting workbook might have too many columns for the file to be viewed in Excel for the web. [!INCLUDE[prod_short](includes/prod_short.md)] automatically limits the exported workbook to 100 columns when OneDrive is configured for system features. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## Related information

[Analyze list data using data analysis mode](analysis-mode.md)   
[Work with Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
