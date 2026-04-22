---
title: Pay by invoice
linkTitle: Pay by invoice
weight: 20
description: Learn how to add or update a payment method in Docker Hub
keywords: payments, billing, subscription, supported payment methods, failed payments, add credit card, bank transfer, Stripe Link, payment failure
---

## Prerequisites

## Invoice overview

The following tables list the main sections on an invoice and the billing fields that supply the bill-to information.

You can’t change a paid or unpaid billing invoice. Updating billing information does not change existing invoices—update before your subscription renewal when the invoice is finalized. For more information, see
[Update billing information](/manuals/billing/manage-billing.md#manage-billing-details).

### View invoice

| Section     | Details                                                         |
| ----------- | --------------------------------------------------------------- |
| Identifiers | Invoice number, date of issue, due date                         |
| Bill to     | Your bill-to information (from your billing profile)            |
| Payment     | Amount due (USD) and a link to pay online                       |
| Line items  | Description, quantity (if applicable), unit price, amount (USD) |
| Summary     | Subtotal, discount (if applicable), total                       |

### View billing fields

| Field         | Required? | Description                                         |
| ------------- | --------- | --------------------------------------------------- |
| Name          | Required  | Administrator or company name                       |
| Address       | Required  | —                                                   |
| Email address | Required  | Receives all billing-related emails for the account |
| Phone number  | Optional  | —                                                   |
| Tax ID or VAT | Optional  | —                                                   |

## Pay invoice

> [!NOTE]
>
> Pay by invoice is only available for subscribers on an annual billing cycle.
> To change your billing cycle, see
> [Change your billing cycle](/manuals/billing/manage-billing.md#billing-cycle).

If you've selected pay by invoice for your subscription, you'll receive email
reminders to pay your invoice at 10 days before the due date, on the due date,
and 15 days after the due date.

You can pay an invoice from the Docker Billing Console:

1. Sign in to [Docker Home](https://app.docker.com/) and choose your organization.
1. Select **Billing**.
1. Select **Invoices** and locate the invoice you want to pay.
1. In the **Actions** column, select **Pay invoice**.
1. Fill out your payment details and select **Pay**.

When your payment has processed, the invoice's **Status** column will update to
**Paid** and you will receive a confirmation email.

If you choose to pay using a US bank account, you must verify the account. For
more information, see [Verify a bank account](/manuals/billing/payment-method.md#verify-a-bank-account).

## Enable or disable pay by invoice

> [!TIP]
> Do you need to pay by invoice? [Upgrade to a Docker Business or Docker Team plan](https://www.docker.com/pricing?ref=Docs&refAction=DocsBillingPaymentMethod) and choose the annual subscription.

Pay by invoice requires you to pay upfront for your first subscription period using a payment card or ACH bank transfer. At renewal time, instead of automatic payment, you'll receive an invoice via
email that you must pay manually.

Follow these steps to enable or disable pay by invoice:

1. Sign in to [Docker Home](https://app.docker.com/) and select your
   organization.
2. Select **Billing**, then **Payment methods**.
3. Select **Pay by invoice**, then select the pay by invoice toggle to enable or disable.
4. Confirm your billing contact details. If you need to change them, select
   **Change** and enter your new details.

Pay by invoice is not available for
subscription upgrades or changes.

## View pay by invoice history

## Next steps
