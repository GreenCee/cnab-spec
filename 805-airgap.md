---
title: Disconnected Scenario
weight: 805
---

# Disconnected Scenarios

This section is non-normative, but is here to describe the scenario noted in the introduction [100-CNAB](100-CNAB.md) and the explicit attributes that make up a disconnected scenario.

## Summary

Common cloud patterns today reference artifacts and code from multiple sources as described in [300-CNAB-security]
(300-CNAB-security.md). Industry best practices [NISTIR-8176](https://csrc.nist.gov/News/2017/NIST-Releases-NISTIR-8176) describe the importance of private registries and limiting use of uncontrolled artifacts in production. CNAB aims to enable adherence to 

## Internet Access

A typical disconnected scenario will have limited, intermitent or no internet access whether by design or by situation. As a result, everything required for installation needs to be included in a CNAB Thick Bundle for transfer into a disconnected envrionment. 

## Target Registry

A CNAB runtime is NOT required to provide registry functionality to a CNAB in a disconnected scenario. It can be assumed that an OCI Artifact compliant registry will be available to push the bundle to for further consumption. 

## Archive

A CNAB bundle may reference artifacts that are hosted in different repositories or registries. These remote artifacts may change over time without changing the references. While this is desireable in some cases, archiving the entirey of a CNAB at a point of time with artifacts will provide a central location for code auditing and digital forensics of all logic and references used in a CNAB.

## Relocation

After movement of a CNAB to a disconnected envrionment, there may need to be additional mutations to a bundle to adapt to the nuances of a specific disconnected evironment