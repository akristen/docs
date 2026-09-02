---
title: Security
linkTitle: Security
description: Secure Docker accounts and organizations in Docker Home, for administrators and developers.
keywords: docker, docker hub, security, 2FA, access tokens, SSO, OIDC, provisioning, roles, administrators, developers
weight: 40
aliases:
  - /security/for-developers/
  - /platform/security/
params:
  sidebar:
    group: Accounts and admin
grid_administrators:
  - title: Single sign-on
    description: Sign in to Docker through your identity provider.
    icon: key
    link: /security/authentication/single-sign-on/
  - title: Provisioning
    description: Provision users with SCIM, JIT, auto-provisioning, and domain management.
    icon: arrow-path
    link: /security/provisioning/
  - title: Roles and permissions
    description: Assign core or custom roles to control access in your organization.
    icon: shield-check
    link: /security/roles-and-permissions/
  - title: Organization access tokens
    description: Grant org-owned Hub access to CI/CD without tying it to one person.
    icon: building-office-2
    link: /security/access-tokens/organization-access-tokens/
  - title: OIDC connections
    description: Authenticate GitHub Actions with short-lived tokens.
    icon: lock-closed
    link: /security/authentication/oidc-connections/
grid_developers:
  - title: Two-factor authentication
    description: Add a TOTP security code to your Docker account.
    icon: device-phone-mobile
    link: /security/authentication/2fa/
  - title: Personal access tokens
    description: Authenticate the Docker CLI and tools without using your password.
    icon: finger-print
    link: /security/access-tokens/personal-access-tokens/
grid_related:
  - title: Docker Engine security
    description: Keep the Docker Engine daemon and host secure.
    icon: shield-check
    link: /engine/security/
  - title: Secrets in Docker Compose
    description: Use secrets in Compose applications.
    icon: shield-exclamation
    link: /compose/how-tos/use-secrets/
  - title: Static vulnerability scanning
    description: Run a point-in-time scan on Docker Hub images.
    icon: magnifying-glass
    link: /docker-hub/repos/manage/vulnerability-scanning/
  - title: Suppress CVEs with VEX
    description: Suppress non-applicable or fixed vulnerabilities in image analysis.
    icon: chart-bar
    link: /scout/guides/vex/
  - title: Docker Hardened Images
    description: Use hardened images for software supply chain security.
    icon: lock-closed
    link: /dhi/
  - title: Security best practices
    description: Steps you can take to improve container security.
    icon: squares-2x2
    link: /develop/security-best-practices/
  - title: Security FAQs
    description: Common questions about SSO, identity providers, and domains.
    icon: question-mark-circle
    link: /faqs/security/
---

Docker account and organization security in Docker Home covers how users
sign in and how organization and company owners control access.

## For administrators

Configure SSO, provisioning, roles, and organization-level credentials for
the organizations and companies you manage.

{{< grid items="grid_administrators" >}}

## For developers

Add two-factor authentication to your Docker account, and authenticate
the CLI with a personal access token.

{{< grid items="grid_developers" >}}

## Related product security

Engine, Compose, Hub, Scout, and Hardened Images have their own security
controls. Those topics live with those products, not under Accounts and admin.

For organization-wide Docker Desktop controls, see
[Hardened Docker Desktop](/manuals/enterprise/security/hardened-desktop/_index.md)
and [Enforce sign-in](/manuals/enterprise/security/enforce-sign-in/_index.md).

{{< grid items="grid_related" >}}
