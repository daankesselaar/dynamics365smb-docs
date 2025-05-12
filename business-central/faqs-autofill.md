---
title: Responsible AI FAQ for autofill (preview)
description: Learn about the AI technology of Autofill in Business Central, considerations, details about how AI is used, tested, evaluated, and limitations.
ms.date: 04/01/2025
ms.custom: 
  - responsible-ai-faqs
ms.topic: faq
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: copilot, AI, chat 
---
# Responsible AI FAQ for autofill (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

These frequently asked questions (FAQ) describe the AI impact of Copilot’s Autofill feature in Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

<!--[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]-->

## What is Autofill?

Manually entering data can be time-consuming and error-prone, both for casual users of Business Central, and expert users that are tasked with entering records throughout their entire workday.  

Microsoft Copilot is an AI-powered assistant that sparks creativity, boosts productivity, and eliminates tedious tasks. Copilot uses AI to suggest and fill out field values automatically on your page, instead of typing or looking up things across screens. You can choose to keep or discard the suggestions. 

## What are the capabilities of Autofill?

When you ask Copilot to autofill fields on a page in Business Central, it suggests values for all fields within a field group (FastTab). These suggestions aren't always AI-generated. Copilot uses various mechanisms described in the following table to provide suggestions for each field, indicating the most appropriate mechanism.

Regardless of whether the suggested value is AI-generated, Copilot always uses AI to determine the appropriate mechanism for a field.

|Mechanism|Description|
|-|-|
|Most-Frequently Used |The value most frequently assigned to records in your company. The suggested value isn't computed using AI and comes directly from your Business Central data. |
|Most-Recently Used |For fields that reference another table, the most recently used reference, or most recently viewed record for that table. The suggested value isn't computed using AI and comes directly from your Business Central data. |
|Lookup selection |For fields that reference another table and have a short list of possible choices, AI is used to intelligently select from the possible values.|
|AI-generated |AI is used to intelligently generate the suggested value. |

> [!IMPORTANT]
> Copilot runs under your user context. It only has access to data that you already have access to. Your assigned permissions and all other security and compliance controls also apply when you use Copilot.

## What is the intended use of Autofill? 

Autofill is an assistive feature intended to help people enter data into Business Central. It isn't designed to run autonomously and enter data on behalf of others. Since the suggestions aren't automatically saved to Business Central, you must review and accept each field for it to be saved. 

When you choose to keep a suggestion, you're saving the change to Business Central similar to if you entered that value yourself without the assistance of Copilot.

When you leave the page or record, any suggestions that you didn't choose to keep are automatically discarded. 

Suggested values are displayed directly within the field editing experience, making it easy for you to review each suggestion and choose to keep, discard, or replace the suggestion. 

## How was Autofill evaluated? What metrics are used to measure performance? 

This feature is built in accordance with Microsoft's Responsible AI Standard. Learn more about responsible AI from Microsoft in [Empowering responsible AI practices](https://aka.ms/RAI).

The feature underwent extensive AI testing using Business Central's demonstration data and other fictitious business data. Testing covered various fields and pages from Business Central. Copilot’s output was evaluated for accuracy of suggested values, selection of the appropriate mechanism to suggest a value, grounding of suggested values in database data, and other metrics.

To ensure customer safety and data protection, this feature underwent rigorous testing to detect and deflect harmful content, jailbreaks, and other risks.

## How does Microsoft monitor the quality of generated content? 

Microsoft has various automated systems in place to ensure that output from Copilot is of the highest quality. Automated systems also detect abuse, and ensure safety for our customers and their data by filtering harmful content. 

Microsoft might disable the Copilot features for selected customers if abuse of the functionality is detected. 

Users have the opportunity to provide feedback to every Copilot response and report inaccurate or inappropriate content to help Microsoft improve this feature. If you encounter inappropriate content, report it to Microsoft by using this feedback form: [Report abuse](https://go.microsoft.com/fwlink/?linkid=2249810). We analyze user feedback on the feature and use it to help us improve responses.

You provide feedback by using the like (thumbs up) or dislike (thumbs down) icon in the information about an individual suggestion or for all suggestions in the group of fields.

## What are the AI limitations of Autofill? How can users minimize the impact of the limitations when using the system?

- General AI limitations

  AI systems are valuable tools but they're nondeterministic. The content they generate might not be accurate. It's important to use your judgment to review and verify responses before making decisions that could affect stakeholders like customers and partners. 

- Geographic and language availability

  [!INCLUDE [copilot-geo-and-language-availability-en-only](includes/copilot-geo-and-language-availability-en-only.md)]

- Certain industry, product, and subject limitations

  Organizations that operate in some business domains, such as medical, drugs, legal, and weapons, might experience lower quality or limited output from Copilot due to the sensitive nature of that domain.

## What data does Autofill collect and how is it used?

Business Central collects the minimum data required for Microsoft to offer the service. 

- Microsoft collects anonymized information about decisions made by Copilot and your choice to keep or discard a suggestion. It doesn't collect suggested field values or other company data used by Copilot to provide suggestions.
- Microsoft doesn't use your business data to train the foundational models for the benefit of others. Learn more in [Dynamics 365 terms for Azure OpenAI-powered features](https://go.microsoft.com/fwlink/?linkid=2236010).

## Related information

[Autofill fields with Copilot](autofill-fields-with-copilot.md)  
[FAQ for Copilot data security and privacy](/dynamics365/faqs-copilot-data-security-privacy?toc=/dynamics365/business-central/toc.json)  
[Azure OpenAI Service and Business Central data](azure-openai-data.md)  
[Copilot data movement across geographies](ai-copilot-data-movement.md)  
