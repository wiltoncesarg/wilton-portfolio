# Case 05 — Proxmox Virtualization

## Overview

Hands-on construction and operation of a Proxmox virtualization cluster built from physical infrastructure, with 3 physical hosts.

## Cluster Construction

The cluster was built from scratch in collaboration with a colleague.

Activities included Proxmox installation/configuration, cluster configuration, physical network-interface identification, trunk connectivity preparation, NFS storage, host addition and migration testing.

The physical switch trunk configuration was performed by another network team.

## Networking Challenge

An initial challenge was identifying the correct physical interfaces and preparing virtualization-side connectivity. The network team handled physical switch configuration, while the infrastructure team performed virtualization configuration and validation.

## VMware → Proxmox Migration

Migration tests included preparing target VMs, validating operation and performing live migration between Proxmox nodes.

Live migration was successfully tested without VM downtime.

## Day-to-Day Operations

- VM creation/removal
- CPU, memory, storage and network adjustments
- NFS storage management
- VM migration testing
- Backup routines supported by scripts

## VMware Background

Previous VMware experience includes operational VM creation, removal and resource adjustments. Platform installation was not part of that scope.

## Result / Impact

A functional clustered virtualization platform was established with shared storage and tested live migration capabilities, providing practical experience transitioning workloads and operational practices from VMware toward Proxmox.

## Technologies

Proxmox VE · Linux · NFS · VMware · Virtual machines · Network trunking · Shell scripting
