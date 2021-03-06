---
title: Change the Azure subscription your VSTS account uses for billing
description: Steps for how to unlink the Azure subscription your Visual Studio Team Services account uses for billing via the Visual Studio Marketplace
ms.prod: devops
ms.technology: devops-billing
ms.assetid: e447adb1-6208-49f6-a488-515aa4b2fdcf
ms.topic: conceptual
ms.manager: douge
ms.author: chcomley
author: chcomley
ms.date: 07/10/2018
---
[//]: # (monikerRange: 'vsts')

# Change the Azure subscription that your VSTS account uses for billing

**VSTS**

If you want to use a different Azure subscription to bill purchases for your VSTS account, you can either move it to a different Azure subscription that you have access to, or remove the current Azure subscription and then buy again using a new subscription.

## Move to a different subscription

If the target subscription is in the same Azure Active Directory as the destination subscription and you have access to both, just follow the steps below or learn more about [moving resources to new resource groups or subscriptions](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-move-resources).

1. Sign in to the [Azure portal](https://portal.azure.com).
2. Choose **Resource groups**.

   ![Choose Azure Resource groups](_img/change-azure-subscription/azure-resource-groups.PNG)

3. Select the resource group containing your VSTS account.
4. Choose **Move** and then **Move to another subscription**.

   ![Select Move and then Move to another resource group](_img/change-azure-subscription/select-move-to-another-subscription.png)

5. Select your target subscription and resource group.
6. Choose **OK**.

## Remove billing subscription and purchase again

### Prerequisites

1. [VSTS project collection administrator or account owner permissions](../organizations/accounts/faq-add-delete-users.md#find-owner)
2. [The **owner** or **contributor** role on your Azure subscription](add-backup-billing-managers.md)

>[!NOTE]
> When you remove the billing subscription from your account, any paid quantities of VSTS Basic, Package Management users, Test Manager users, Microsoft-hosted Pipelines, and self-hosted Pipelines you’ve paid for this month will continue uninterrupted until the 1st of next month, but your account will revert immediately to the Free Tier for cloud-based load testing. Removing the subscription will also cancel any non-Microsoft paid extensions without refund or credit.

### Change subscription

1. [Sign in to the Azure portal](https://portal.azure.com/) as VSTS account owner and as Azure subscription co-administrator or greater.

    If you experience browser problems with Azure,
    make sure that you use a [supported browser](/azure/azure-preview-portal-supported-browsers-devices).

2. Go to **All services** > **Team Services accounts**. 

   ![Choose All services and Team Services accounts](_img/change-azure-subscription/all-services-team-services-accounts.png)

3. Select your account and remove billing.

   ![Remove billing from your account](_img/change-azure-subscription/choose-account-and-remove-billing.png)

### Purchase again using the new subscription

1. Make your purchases again in the [VSTS Marketplace](https://marketplace.visualstudio.com/vsts). During your first purchase, select the new Azure subscription to use for billing going forward.

>[!NOTE]
> You will only incur incremental charges if the quantities of Microsoft resources you select exceed what you've already paid for the current month. Purchases of non-Microsoft extensions will be treated as new purchases and billed immediately to your new Azure subscription.
If you wait until the 1st of next month to make your purchases again, your VSTS account will revert to the Free Tier and users in excess of the free limits will appear as expired.

## Related articles

- [VSTS users](https://marketplace.visualstudio.com/items?itemName=ms.vss-vstsuser)
- [Microsoft-hosted CI/CD](https://marketplace.visualstudio.com/items?itemName=ms.build-release-hosted-pipelines)
- [Self-hosted CI/CD](https://marketplace.visualstudio.com/items?itemName=ms.build-release-private-pipelines)
- [Test Manager](https://marketplace.visualstudio.com/items?itemName=ms.vss-testmanager-web)
- [Package Management](https://marketplace.visualstudio.com/items?itemName=ms.feed)
- Any non-Microsoft services you're buying through the [Visual Studio Marketplace](https://marketplace.visualstudio.com/vsts).
