---
title: SQL Server Transport Upgrade Version 6 to 7
summary: Migration instructions on how to upgrade SQL Server Transport from Version 8 to 9.
reviewed: 2020-11-09
component: SqlTransport
related:
- transports/sql
- nservicebus/upgrades/7to8
isUpgradeGuide: true
upgradeGuideCoreVersions:
 - 7
 - 8
---

## Timeout manager

The [timeout manager is removed from core](/nservicebus/upgrades/7to8/#timeout-manager-removed) which makes timeout manager backwards compatibility mode obsolete. If backwards compatibility mode was enabled these APIs must be removed.

## WithPeekDelay replaced by QueuePeekerOptions

In version 6 of the transport, the message peek delay can be defined using the `WithPeekDelay` configuration option. The configuration setting has been moved to a more generic `QueuePeekerOptions` that allows configuration of other parameters related to message peeking.