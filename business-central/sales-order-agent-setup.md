---
title: Set up Sales Order Agent
description: Learn how to activate the Sales Order Agent and manage user access.
ms.date: 04/01/2025
ms.topic: how-to
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
ms.search.form: 4400_Primary, 4410
---
# Set up Sales Order Agent (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

The Sales Order Agent in Business Central automates processing sales orders from customer email requests. This article explains how to set up, activate, configure the Sales Order Agent, and manage user access.

Learn more about the agent in [Sales Order Agent overview](sales-order-agent.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

<!--[!INCLUDE [limited-public-preview](includes/limited-public-preview.md)]-->

## Prerequisites

Before configuring and activating the sales order agent, ensure the following prerequisites are met:

- The Business Central environment is one of these country/region versions: AU (Australia), CA (Canada), GB (Great Britain), NZ (New Zealand), or US (United States).

  Sales Order Agent is currently unavailable in other countries/region versions. Learn more about geographic and language availability at [Copilot international availability](https://aka.ms/bapcopilot-intl-report-external).
- Set up the email account for receiving incoming requests for sales quotes and orders.

   The Sales Order Agent monitors incoming emails to this mailbox. The email account must be a **Microsoft 365** type (user mailbox or shared mailbox) in your organization. Learn more at [Set up email](admin-how-setup-email.md).

   > [!IMPORTANT]
   > To activate and configure the agent, you need **Read and manage (Full Access)** and **Send as** permission on the mailbox, unless it's your personal mailbox. As an Exchange admin, delegate these permissions to all users who need to activate and configure the agent. Learn more in [Use the Exchange admin center to edit shared mailbox delegation](/microsoft-365/admin/email/create-a-shared-mailbox#use-the-eac-to-edit-shared-mailbox-delegation).
   >
   > When a user activates the agent, it runs as a background task in the context of that user and needs access to the shared mailbox to process emails. It might take a few hours for Exchange to propagate the permissions to the selected users.
- Set up the Business Central environment for billing agent capabilities (preview version 26.0 sandbox environments in the United Kingdom and United States only).

   Agents use Microsoft Copilot Studio messages when a user runs it, which your company is charged for. Learn more in [Manage consumption-based billing](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-consumption-billing).

- Turn on the **Allow HttpClient Requests** toggle in the **Sales Order Agent** extension settings (sandbox environments only)

   Open the [Extension management](https://businesscentral.dynamics.com/?page=2500) page, select **Sales Order Agent**, and then turn on the **Allow HttpClient Requests** toggle.

## Turn on the Sales Order Agent capability for the environment

The agent capability is on if the ![Shows the Sales Order Agent icon](media/soa-icon.png) **Sales Order Agent** icon appears in the top navigation menu of the role center.

![Shows the Sales Order Agent icon on a role center](media/soa-in-role-center.svg)

If the icon isn't present, turn it on from the **Copilot & agent capabilities** page, like other Copilot features in Business Central. The Sales Order Agent is listed under **Production ready previews**. Learn more in [Configure Copilot and AI agent capabilities](enable-ai.md).

Next, configure and activate the agent so it can process customer sales orders.

## Configure and activate Sales Order Agent

Configure and activate the Sales Order Agent for your company. Only one Sales Order Agent is allowed per company, but you can give access to many users.

1. In the navigation bar at the upper right of the role center, select ![Shows the Sales Order Agent icon](media/soa-icon.png) **Sales Order Agent** > **Activate**.

1. On the **Configure the Copilot agent** page, turn on the **Monitor incoming information** toggle, select the **Mailbox** check box, and then set **Mailbox** field to the email account you want the agent to monitor.

   ![Shows the Sales Order Agent configuration page](media/soa-configuration.png)

1. Select **Manage user access** to specify the users who can manage or interact with the agent. You can add more users now or later. Learn more in [Manage user access to the Sales Order Agent](#manage-agent-permissions-and-user-access).
1. Turn on the **Active** toggle.
1. On the right side of the page, select the **Go to next card** arrow to choose how the agent helps with inquiries, quotes, and orders.

    There are several options described in the following table:

    |Option|Description|Default|
    |-|-|-|
    |Select only available items|Specifies whether the agent considers item availability when searching for the customer's requested items.<br><br>When on, the agent checks inventory to determine whether the customer's requested item quantity is available based on their requested delivery date and location code. If there aren't enough items, the agent prepares the reply to the user that the requested items aren't available, even in situations when fewer items are available. <br><br>When off, the agent includes the customer's requested item quantity regardless of availability. That is, quotes can be created for the items which aren't available and their availability can become negative.<br><br>Learn more about item availability in [Get an availability overview](inventory-how-availability-overview.md) or open the [Item Availability page](https://businesscentral.dynamics.com?page=4410).|On|
    |Create sales documents|When on, the agent can create sales quotes and orders from email inquiries based on the remaining options in this table.<br><br>When off, the agent handles only email communication and doesn't create quotes or orders. The remaining options are irrelevant and can’t be set.|On|
    |Review quotes when created and updated|When on, the agent adds a review step for a Business Central user to review and confirm the sales quote before creating an outgoing email with the quote details and attachment. <br><br>When off, the agent creates or modifies sales quotes as requested and then automatically proceeds with creating an outgoing email with the quote as an attachment. The user must review and confirm the email before the agent sends it to the customer. |Off|
    |Make orders from quotes|When on, the agent converts confirmed sales quotes into orders after the customer agrees to the quote via email and the Business Central user confirms the email.<br><br>When off, you have to create the order manually.|On|
    |Review orders when created and updated|When on, the agent adds a review step for a Business Central user to review and confirm the sales order before creating an outgoing email with the order details and attachment. <br><br>When off, the agent creates the sales order as requested and then automatically proceeds with creating an outgoing email with the order as an attachment. The user must review and confirm the order before the agent sends it to the customer. |Off|

1. Select **Update** to complete the setup.
1. Ensure the Sales Order Agent's language is set to a supported language.

   When you configure the agent, it uses the same language as the display language of your workspace. [Learn how to change the agent's language](#change-language-and-regional-settings).

The **Sales Order Agent** icon changes to ![Shows the Sales Order Agent icon after configured](media/soa-activated-icon.png), indicating the agent is active and ready to handle incoming quote requests to the mailbox.

When the Sales Order Agent is active, a scheduled task added to job queue runs every 20 seconds on the mailbox. This task monitors new unread messages in the mailbox. If a new unread message is found, the Sales Order Agent imports the message into Business Central and verifies whether there's already a task for the mail thread. If a task for the thread already exists, the Sales Order Agent incorporates the new message into the existing task. Otherwise, it creates a new task for the message.

> [!NOTE]
> The ![Shows the Sales Order Agent icon when the agent is configure but not active](media/soa-not-activated-icon.png) icon indicates the agent is configured with mailbox, but it's not active. To activate it, select the icon, then select ![Shows the configuration icon for Sales Order Agent](media/soa-configure-icon.png) **Configure Sales Order Agent** to reopen the configuration page. From there, turn on the **Active** toggle.

## Manage agent permissions and user access

### Add agent users

As an administrator, you can specify which users have permission to use or configure the Sales Order Agent. There are two ways to add and configure agent users:

#### [From Configure Sales Order Agent](#tab/soaconfig)

1. Open the **Configure Sales Order Agent** page by selecting ![Shows the Sales Order Agent icon after configured](media/soa-activated-icon.png) **Sales Order Agent** > ![Shows the configuration icon for Sales Order Agent](media/soa-configure-icon.png) **Configure**.
1. Turn off the **Active** toggle.
1. Select **Manage user access**.
1. On the **Select users that can manage or interact with the Agent** page, you can do the following steps:

   - To add a user, select an empty line, select the **User Name** field, then select the user from the list.
   - To give a user permission to configure Sales Order Agent, select the **Can configure** check box. <br><br> The **Can configure** setting defines whether a user has access to update the agent configuration (for example, updating the designated mailbox, activating and deactivating the agent, and other settings) or only to work with the agent tasks (for example, reviewing and confirming agent steps).
   - To remove a user's access to the agent, select ![Shows the icon to show more option on a field](media/show-more-options-icon.png) **Show more options** next to the user name, and then select **Delete**.

#### [From Sales Order Agent card page](#tab/soapage)

1. To open the **Sales Order Agent** card page, search (<kbd>Alt</kbd>+<kbd>Q</kbd>) for  **Agents**, and then select **SALES ORDER AGENT - [COMPANY]**.
1. Set **Status** to **Disabled** to deactivate the agent.
1. In the **User access** section, you can do the following steps:

   - To add a user, select an empty line, select the **User Name** field, then select the user from the list.
   - To give a user permission to configure Sales Order Agent, select the **Can configure** check box.
   - To remove a user's access to the agent, select ![Shows the icon to show more option on a field](media/show-more-options-icon.png) **Show more options** next to the user name, and then select **Delete**.

---

### Manage agent permissions to objects, data, and UI elements

The Sales Order Agent has a user account in Business Central, similar to other users. To access this account, search for and open the **Agents** page, and then select **SALES ORDER AGENT - [COMPANY]** to open the agent card page.

The **Agent Permission Sets** section lists all the permission sets currently assigned to the agent. By default, the Sales Order Agent has the **SOA AGENT – EDIT** permission set. This set restricts access to only the objects, data, and UI elements (such as pages, fields, and actions) necessary for handling sales quote requests.

You can't modify the **SOA AGENT – EDIT** permission set directly, because it's a system permissions set. However, you can create a copy of **SOA AGENT – EDIT** permission set, modify the copy to suit your needs, then add it to **Agent Permission Sets** section, along with any other permission sets.

Before you can add or delete permission sets applied to the agent, change the **State** to disabled. When you're done making changes, set it back to **Enabled**.

The following system permissions are available for controlling user access to the agent's functionality:

- **Configure All Agents** (ID 9665): Grants a user access to manage the configuration settings of the Sales Order Agent.
- **Manage Agent Tasks** (ID 9670): Allows a user to work with agent tasks displayed in the Copilot pane.

These system permissions are also included in the following permission sets, entitlements, and license types:

- The **SECURITY** permission set includes the **Configure All Agents** permission.
- The **System Execute - Basic** permission set includes the **Manage Agent Tasks** permission.
- The **System Tables - Basic** permission set includes all virtual tables used by the agent (labeled as "Agent *" tables).
- Essential and Premium license entitlements now include **Manage Agent Tasks** permissions.
- All license types include **Configure All Agents** permissions.

Users can configure the Sales Order Agent if they have the **Configure All Agents** permission or are listed as an agent user with the **Can Configure** field selected.

Users can work with agent tasks in the Copilot pane if they have the **Manage Agent Tasks** permission (either explicitly or as part of their Essential or Premium license permissions) and are listed as an agent user.

## Change language and regional settings

[!INCLUDE[soa-language-support](includes/soa-language-support.md)]

1. To open the **Sales Order Agent** card page, search (<kbd>Alt</kbd>+<kbd>Q</kbd>) for  **Agents**, and then select **SALES ORDER AGENT - [COMPANY]**.
1. Select **User Settings**.
1. Set **Lanaguage** to a supported English locale.

## Next steps

[Process sales quotes and orders with Sales Order Agent](sales-order-agent-process.md)

## Related information

[Sales Order Agent overview](sales-order-agent.md)  
[FAQ for Sales Order Agent](faqs-sales-order-taker-agent.md)  
[Configure Copilot and agent capabilities](enable-ai.md)  