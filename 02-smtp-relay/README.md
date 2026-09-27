# Case 02 — SMTP Relay

## Overview

Administration and troubleshooting of a critical SMTP Relay environment responsible for processing millions of messages per day.

## Architecture

```text
Corporate Applications
          │
          ▼
       HAProxy
          │
    ┌─────┼─────┐
    ▼     ▼     ▼
 Postfix Postfix Postfix ...
    │
    ├── Authentication
    └── OpenDKIM
          │
          ▼
       Internet
```

The environment contains approximately 7–8 servers.

## Technical Challenge

The relay must handle high message volumes while maintaining reliable delivery, authentication, message signing and reputation.

## My Role

- Linux administration
- Postfix administration and troubleshooting
- OpenDKIM configuration and troubleshooting
- HAProxy operation
- Queue analysis
- Delivery troubleshooting
- Investigation of IP blocks and reputation
- Investigation of abnormal sending behavior
- Investigation of compromised accounts/applications
- Health monitoring
- Coordination with application, network and security teams
- SPF, DKIM and DMARC best practices

## Troubleshooting Approach

```text
Application
    ↓
SMTP Relay
    ↓
HAProxy
    ↓
Postfix
    ↓
Queue
    ↓
OpenDKIM
    ↓
Destination Server
```

This path helps isolate whether a problem originates with the application, relay, queue, signing process or external destination.

## Common Incidents

Queue growth, delivery failures, abnormal message volumes, compromised accounts/applications, IP reputation problems, IP blocks and destination-server rejections.

## Result / Impact

A centralized SMTP service supporting multiple applications, with operational processes focused on reliability, troubleshooting and secure mail delivery.

## Technologies

Linux · HAProxy · Postfix · OpenDKIM · SPF · DKIM · DMARC · SMTP
