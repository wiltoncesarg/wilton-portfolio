# Case 03 — ExpressoMG Collaboration Platform

## Overview

ExpressoMG was a collaboration and communication suite used by state agencies, supporting approximately 25,000 active accounts and roughly 50 virtual servers across production, homologation and development. The infrastructure was predominantly Debian Linux.

## Team & Ownership

A team of two professionals with complementary skills and shared knowledge had end-to-end responsibility for deployment, configuration, maintenance, troubleshooting and service continuity.

The work also involved agency IT administrators and multiple infrastructure/application teams.

## Messaging Architecture

### Access

```text
User → SOGo → Cyrus → Mailbox
```

### Receiving Mail

```text
Internet → Antispam → Cyrus → Backend Identification
                              ↓
                        Sieve Rules / Filters
                         ├──→ Mailbox
                         └──→ Other Destination
```

### Sending Mail

```text
SOGo / Application → Outbound SMTP → Internet
```

## Collaboration Services

### Drive

Nextcloud with 3 web servers, database and ONLYOFFICE Document Server.

### Meet

Jitsi Community Edition with 1 node receiving communications and 4 Videobridges distributing meetings. Stabilizing meeting distribution across the Videobridges was a significant technical challenge.

### Chat

The environment initially used Rocket.Chat. The team evaluated alternatives and adopted Zulip Community Edition, participating in installation, testing and production maintenance.

## Linux Infrastructure

Responsibilities included Debian Linux, OS updates and tuning, service updates, Nginx/Apache configuration, Keepalived and VIP-based redundancy, certificates, LDAP and operational database administration.

CA-issued certificates were requested from the responsible area and distributed/configured across web, SMTP, IMAP and POP3S. Jitsi and Zulip used Let's Encrypt.

## LDAP & Antispam

LDAP work included structure changes, replication configuration, troubleshooting, tuning, queries and application integration.

Antispam responsibilities included rule creation/adjustment, false-positive analysis, sender/domain allowlisting and blocked-message investigation.

## Virtualization

For production VMs, the team defined sizing and another infrastructure area provisioned the VM. The team then owned service configuration and operation.

Testing and internal services used VMware and later Proxmox.

## Open Source Adoption

A recurring workflow was:

```text
Need → Research → Evaluation → Installation → Testing → Homologation → Production → Maintenance
```

Application versions were tested and homologated before production adoption rather than necessarily deploying the latest release immediately.

## Troubleshooting Approach

The team used logs and service behavior to identify failing components, research fixes, apply corrections/workarounds and validate the result.

## Result / Impact

A broad collaboration and communication suite was operated by a small technical team using open-source and Community technologies, with high technical autonomy and a favorable cost-benefit relationship.

## Technologies

Debian Linux · SOGo · Cyrus · Nextcloud · ONLYOFFICE · Jitsi · Zulip · LDAP · Nginx · Apache · Keepalived · VMware · Proxmox · SMTP · IMAP · POP3S · Let's Encrypt
