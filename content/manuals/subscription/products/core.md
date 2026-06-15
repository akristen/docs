---
title: Docker Core subscription
linkTitle: Docker Core
description:
  Manage Docker Team and Business subscriptions, including seats, upgrades, and
  cancellation
keywords: docker core, docker team, docker business, subscription seats, upgrade
  subscription, downgrade subscription, docker pricing, subscription changes
weight: 10
aliases:
  - /subscription/core/
  - /subscription/testcontainers-cloud/
  - /subscription/products/testcontainers-cloud/
  - /docker-hub/upgrade/
  - /docker-hub/billing/upgrade/
  - /subscription/upgrade/
  - /subscription/downgrade/
  - /subscription/core-subscription/upgrade/
  - /subscription/core-subscription/downgrade/
  - /docker-hub/cancel-downgrade/
  - /docker-hub/billing/downgrade/
  - /billing/scout-billing/
  - /billing/subscription-management/
---

Docker Core subscriptions — Docker Team and Docker Business — provide
commercial Docker Desktop licensing and collaboration features for
organizations. Team covers small to mid-size teams; Business adds enterprise
controls like SSO, SCIM, and enhanced support.

To purchase, sign in to [Docker Home](https://app.docker.com/), go to
**Billing**, select **Browse products**, then choose **View plans** from the
Docker tile.

## Usage

A Docker Core subscription gives every organization member access to:

- Docker Desktop (commercial use)
- Private repositories on Docker Hub (up to the plan limit)
- Included build minutes for Docker Build Cloud
- Included Testcontainers Cloud runtime minutes
- Docker Scout image analysis (up to the plan limit)

Docker Business additionally includes SSO, SCIM provisioning, registry access
management, and enhanced support options.

For a full feature comparison, see
[Docker Pricing](https://www.docker.com/pricing?ref=Docs&refAction=DocsSubscriptionCore).

## Upgrade seats

When you upgrade your Docker Core subscription, you get immediate access to all
features in your new tier.

> [!TIP]
> If you're upgrading from a Personal subscription to a Team subscription and
> want to keep your username,
> [convert your user account into an organization](../../admin/organization/setup/convert-account.md).

To upgrade your subscription:

1. Sign in to [Docker Home](https://app.docker.com/) and select the organization
   you want to upgrade.
1. Select **Billing** to view your current plans.
1. Select **Browse products**.
1. Choose **View plans** from the Docker product tile on the products catalog
   page.
1. Choose a Docker Team or Docker Business plan for the organization.
1. Follow the on-screen instructions to complete your upgrade. If you choose to
   pay using a US bank account, you must verify the account. For more
   information, see
   [Verify a bank account](/manuals/billing/payment-method.md#verify-a-bank-account).

For detailed feature information, see
[Docker Pricing](https://www.docker.com/pricing?ref=Docs&refAction=DocsSubscriptionCore).

### Add seats to an existing subscription

To add seats to a Docker Team or Business subscription, see
[Manage subscription seats](/manuals/admin/organization/manage/manage-seats.md).

## Deactivate

You can downgrade or cancel your Docker Core subscription at any time before the
renewal date. The unused portion is not refundable, but you retain access to
paid features until the end of the current billing cycle.

### Downgrade considerations

Before downgrading, review the following:

- **Team size and repositories**: You may need to reduce team members and
  convert private repositories to public or delete them based on your new
  subscription limits.
- **SSO and SCIM**: If downgrading from Docker Business and your organization
  uses single sign-on, remove your SSO connection and verified domains first.
  Organization members auto-provisioned through SCIM need to reset their
  passwords to sign in without SSO.
- **Private repository collaborators**: Personal subscriptions don't include
  collaborators for private repositories. When downgrading from Pro to Personal,
  all collaborators are removed and additional private repositories are locked.

For feature limits in each tier, see
[Docker Pricing](https://www.docker.com/pricing?ref=Docs&refAction=DocsSubscriptionCore).

### Cancel or downgrade

1. Sign in to [Docker Home](https://app.docker.com/) and select the organization
   you want to downgrade.
1. Select **Billing**.
1. Select the action menu, then **Cancel subscription**.
1. Fill out the feedback survey to continue with cancellation.

> [!IMPORTANT]
>
> If you have a sales-assisted Docker Business subscription, contact your
> account manager to downgrade your subscription.

### Subscription pause policy

You can't pause or delay a subscription. If a subscription invoice isn't paid
by the due date, there's a 15-day grace period starting from the due date.

## What's next

- [Manage subscription seats](/manuals/admin/organization/manage/manage-seats.md)
- [Manage licenses](/manuals/admin/organization/manage/manage-licenses.md)
- [Change your billing cycle](/manuals/billing/cycle.md)
- [Docker Desktop overview](/manuals/desktop/_index.md)
- [Docker Hub overview](/manuals/docker-hub/_index.md)

## Docker Personal subscription

Docker Individual subscriptions cover personal Docker accounts. Docker Personal
is included at no cost when you create a Docker ID and gives access to essential
Docker tools. Docker Pro adds higher usage limits and additional features for
individual professional use.

To upgrade to Docker Pro, sign in to [Docker Home](https://app.docker.com/),
go to **Billing**, select **Browse products**, then choose **View plans** from
the Docker tile.

## Usage

**Docker Personal** includes:

- Docker Desktop (for eligible personal, educational, and small-business use)
- Public repositories on Docker Hub (unlimited)
- One private repository on Docker Hub
- Included Gordon usage allowance

**Docker Pro** additionally includes:

- Docker Desktop for commercial use by individual professionals
- Unlimited private repositories on Docker Hub
- Higher included build minutes
- Increased Docker Scout image analysis

For a full feature comparison, see
[Docker Pricing](https://www.docker.com/pricing?ref=Docs&refAction=DocsSubscriptionIndividual).

For information about Docker Desktop's commercial use requirements, see
[Docker Desktop license agreement](./desktop-license.md).

## Upgrade subscription

When you create your Docker ID, you automatically receive a Docker Personal
subscription. To upgrade to Docker Pro:

1. Sign in to [Docker Home](https://app.docker.com/) and select your personal
   account.
1. Select **Billing** to view your current plans.
1. Select **Browse products**.
1. Choose **View plans** from the Docker tile on the products catalog page.
1. Select **Docker Pro**.
1. Follow the on-screen instructions to complete your upgrade.

To increase your Gordon usage allowance beyond what's included in your
individual subscription, see
[Gordon plans](./gordon.md).

## Deactivate

You can cancel your Docker Pro subscription at any time before your renewal
date. The unused portion is not refundable, but you retain access to Pro
features until the end of the current billing cycle.

When you cancel, your account reverts to Docker Personal. Private repository
collaborators are removed and additional private repositories are locked.

To cancel your subscription:

1. Sign in to [Docker Home](https://app.docker.com/) and select your personal
   account.
1. Select **Billing**.
1. Select the action menu, then **Cancel subscription**.
1. Fill out the feedback survey to continue with cancellation.

## What's next

- [Create a Docker account](/manuals/accounts/create-account.md)
- [Gordon plans](./gordon.md)
- [Docker Desktop overview](/manuals/desktop/_index.md)
- [Docker Desktop license agreement](./desktop-license.md)
