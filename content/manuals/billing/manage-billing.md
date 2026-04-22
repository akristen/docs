---
title: Manage billing
weight: 30
description: Learn how to update your billing information in Docker Hub
keywords: payments, billing, subscription, invoices, update billing email, change billing address, VAT ID, Docker billing account
aliases:
  - /billing/cycle/
  - /billing/details/
  - /billing/history/
  - /billing/core-billing/history/
---

## Billing cycle

> [!IMPORTANT]
> Pay by invoice is not
> available for subscription upgrades
> or changes.

You can choose between a monthly or annual billing cycle when purchasing a subscription.

- If you're on a monthly plan, you can switch to a yearly plan at any time
- However, switching from a yearly to a monthly cycle isn't supported.

### Overview

When you change your billing cycle, your next billing date reflects the new cycle.

- If the monthly subscription started on March 1 and ended on April 1, switching the billing duration on March 15, 2024, resets the new start date to March 15, 2024.
- The new end date is March 15, 2025.

Any unused portion of your monthly subscription is prorated and applied as credit toward an annual subscription. For example, if your monthly cost is $10 and you're used value is $5, when you switch to an annual cycle ($100), the final charge is $95 ($100-$5).

### Change billing cycle

{{< accordion title="Annual cycle for personal accounts" >}}

To change your billing cycle:

1. Sign in to [Docker Home](https://app.docker.com/) and select
   your organization.
2. Select **Billing**.
3. On the plans and usage page, select **Switch to annual billing**.
4. Verify your billing information.
5. Select **Continue to payment**.
6. Verify payment information and select **Upgrade subscription**. If you choose to pay using a US bank account, you must verify the account. For more information, see [Verify a bank account](payment-method.md#verify-a-bank-account).

The billing plans and usage page will now reflect your new annual plan details.
{{< /accordion >}}

{{< accordion title="Annual cycle for organizations" >}}

> [!TIP]
> You must be an organization owner to make changes to the payment
> information.

Follow these steps to switch from a monthly to annual billing cycle for your
organization's Docker subscription:

1. Sign in to [Docker Home](https://app.docker.com/) and select
   your organization.
1. Select **Billing**.
1. On the plans and usage page, select **Switch to annual billing**.
1. Verify your billing information.
1. Select **Continue to payment**.
1. Verify payment information and select **Upgrade subscription**. If you choose to pay using a US bank account, you must verify the account. For more information, see [Verify a bank account](payment-method.md#verify-a-bank-account).
   {{< /accordion >}}

## Manage billing details

Changes made by updating billing information apply to future billing invoices.

The email address you provide for a billing account is where Docker sends all invoices and other billing related communications. Messages to this address can include the following:

- Confirmations: new subscriptions, paid invoices
- Notifications: card failure, card expiration
- Reminders: subscription renewal

You can update the billing contact email any time you update your billing information using the steps below.

> [!NOTE]
>
> Existing invoices, whether paid or unpaid, cannot be updated.
> Changes only apply to future invoices.

{{< accordion title="Personal account" >}}
To update your billing information:

1. Sign in to [Docker Home](https://app.docker.com/) and select your
   organization.
2. Select **Billing**.
3. Select **Billing information** from the left-hand navigation.
4. On your billing information card, select **Change**.
5. Update your billing contact and billing address information.
6. Optional. To add or update a VAT ID, select the **I'm purchasing as a business** checkbox and enter your Tax ID.

   > [!IMPORTANT]
   >
   > Your VAT number must include your country prefix. For example, if you are
   > entering a VAT number for Germany, you would enter `DE123456789`.

7. Select **Update**.{{< /accordion >}}

{{< accordion title="Organization" >}}

> [!NOTE]
>
> You must be an organization owner to make changes to the billing information.

To update your billing information:

1. Sign in to [Docker Home](https://app.docker.com/) and select your
   organization.
1. Select **Billing**.
1. Select **Billing information** from the left-hand navigation.
1. On your billing information card, select **Change**.
1. Update your billing contact and billing address information.
1. Optional. To add or update a VAT ID, select the **I'm purchasing as a business** checkbox and enter your Tax ID.

   > [!IMPORTANT]
   >
   > Your VAT number must include your country prefix. For example, if you are
   > entering a VAT number for Germany, you would enter `DE123456789`.

1. Select **Update**.
   {{< /accordion >}}

## View billing information and history

Learn how to view and pay invoices, view your billing history, and verify
your billing renewal date. All monthly and annual subscriptions are
automatically renewed at the end of the subscription term using your default
payment method.

{{< accordion title="View renewal date" >}}
You receive your invoice when the subscription renews. To verify your renewal
date:

1. Sign in to [Docker Home Billing](https://app.docker.com/billing).
1. Find your renewal date and amount on your subscription plan card.

{{< /accordion >}}

{{< accordion title="View billing history" >}}

### Personal account

To view billing history:

1. Sign in to [Docker Home](https://app.docker.com/) and choose your
   organization.
1. Select **Billing**.
1. Select **Invoices** from the left-hand menu.
1. Optional. Select the **Invoice number** to open invoice details.
1. Optional. Select the **Download** button to download an invoice.

### Organization

You must be an owner of the organization to view the billing history.

To view billing history:

1. Sign in to [Docker Home](https://app.docker.com/) and select your
   organization.
1. Select **Billing**.
1. Select **Invoices** from the left-hand menu.
1. Optional. Select the **invoice number** to open invoice details.
1. Optional. Select the **download** button to download an invoice.
   {{< /accordion >}}

## Add VAT number to invoice

> [!NOTE]
>
> If the VAT number field is not available, complete the
> [Contact Support form](https://hub.docker.com/support/contact/). This field
> may need to be manually added.

To add or update your VAT number:

1. Sign in to [Docker Home](https://app.docker.com/) and choose your
   organization.
1. Select **Billing**.
1. Select **Billing information** from the left-hand menu.
1. Select **Change** on your billing information card.
1. Ensure the **I'm purchasing as a business** checkbox is checked.
1. Enter your VAT number in the Tax ID section.

   > [!IMPORTANT]
   >
   > Your VAT number must include your country prefix. For example, if you are
   > entering a VAT number for Germany, you would enter `DE123456789`.

1. Select **Update**.

Your VAT number will be included on your next invoice.

## Next steps
