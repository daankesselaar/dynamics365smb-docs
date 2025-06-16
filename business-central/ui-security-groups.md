---
title: Control Access Using Security Groups
description: This article describes how to use security groups to define user permissions.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: access, right, security, permissions
ms.search.form: 1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862, 9875_Primary, 9874_Primary, 9873_Primary, 9872_Primary, 9877_Primary, 9869_Primary, 9868_Primary, 9871_Primary
ms.date: 09/13/2024
ms.service: dynamics-365-business-central
---

# Control access to Business Central using security groups

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Security groups make it easier for administrators to manage user permissions. For example, for [!INCLUDE [prod_short](includes/prod_short.md)] online, they're reusable across Dynamics 365 applications, such as SharePoint Online, CRM Online, and [!INCLUDE [prod_short](includes/prod_short.md)]. Administrators add permissions to their [!INCLUDE [prod_short](includes/prod_short.md)] security groups, and when they add users to the group the permissions apply to all members. For example, an administrator can create a [!INCLUDE [prod_short](includes/prod_short.md)] security group that gives salespeople the ability to create and post sales orders. Or, let purchasers do the same for purchase orders.

> [!NOTE]
> This article describes how to grant certain permissions to users based on their membership of a security group. To control whether users can access an environment based on their membership of a security group, see [Manage Access to Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access).

## Business Central online and on-premises

You can use security groups for the online and on-premises versions of [!INCLUDE [prod_short](includes/prod_short.md)]. Depending on your version, create groups in one of the following ways:

* For the online version, use Microsoft Entra security groups. To learn more about creating the group, go to [Create, edit, or delete a security group in the Microsoft 365 admin center](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* For on-premises, security groups are only supported if the deployment is using Windows authentication. To create security groups for on-premises, use Windows Active Directory groups. To learn more, go to [Create a Group Account in Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

Afterward, create a corresponding security group in [!INCLUDE [prod_short](includes/prod_short.md)], and then link it to the group you created. To learn more, go to [Add a security group in Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> If you've set up a special type of user with a Windows Group license type in a version of [!INCLUDE [prod_short](includes/prod_short.md)] on-prem that's earlier than 2023 release wave 1, when you upgrade [!INCLUDE [prod_short](includes/prod_short.md)] converts the user to a security group. The new security group has the same name as the Windows group name. The security group gives you a better overview of the group members and their effective permissions.

## Add a security group in Business Central

1. Choose the ![Lightbulb that opens the Tell Me feature 1.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Security Groups**, and then choose the related link.
1. Choose **New** to create a group.
1. Create the link to your group, as follows:

    * For [!INCLUDE [prod_short](includes/prod_short.md)] online, choose the group in the **Microsoft Entra security group name** field.
    * For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, choose the group in the **Windows group name** field.

> [!NOTE]
> The users show in the **Members** card on the FactBox pane or the **Security Group Members** page only if they're added as users in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about adding users, go to [To add users or update user information and license assignments in Business Central](ui-how-users-permissions.md#adduser).  

### Assign permissions to a security group

1. On the **Security Groups** page, choose the group, and then choose the **Permissions** action.
1. Assign permissions in the following ways:

    * To assign permission sets individually, in the **Permission Set** field, choose the permissions to assign.
    * To assign multiple permission sets, choose the **Add multiple** action, and then choose the sets to assign.
1. If you want the permission sets to apply only to a specific company, set the **Company** column to that company. If you want the permission set to apply to all companies, leave the **Company** column blank. [Learn more](ui-define-granular-permissions.md#control-access-to-specific-companies).

## Related information

[Create Users According to Licenses](ui-how-users-permissions.md)  
[Set Up Business Central Access in Teams with Microsoft 365 Licenses](admin-access-with-m365-license-setup.md)  
[Learn about groups and access rights in Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Microsoft Entra security groups](/windows-server/identity/ad-ds/manage/understand-security-groups)  
