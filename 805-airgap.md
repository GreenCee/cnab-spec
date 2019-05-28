---
title: Disconnected Scenario
weight: 805
---

# Disconnected Scenarios

This section is non-normative and describes the disconnected (air gapped) scenario mentioned in the introduction of [CNAB-Core](100-CNAB.md).

## Summary

Common cloud patterns today reference artifacts and code from multiple sources as described in
[CNAB-Sec](300-CNAB-security.md).
Industry best practices, particularly [NISTIR-8176](https://csrc.nist.gov/News/2017/NIST-Releases-NISTIR-8176), emphasise the importance of
private registries and avoiding the use of uncontrolled artifacts in production. CNAB aims to enable adherence to these best practices.

_TODO: Need to link the above to air gap._

## Internet Access

A typical disconnected scenario will have limited, intermitent or no internet access, whether by design or by situation.
As a result, everything required for installation ofa bundle needs to be included in a CNAB Thick Bundle for transfer into the disconnected environment. 

## Target Registry

A CNAB runtime is NOT required to provide registry functionality to a CNAB in a disconnected environment.
It is assumed that an OCI compliant registry is available in the disconnected environment for hosting the bundle and/or the images referenced by the bundle.

## Archive

A CNAB bundle may reference artifacts that are hosted in different repositories or registries. These remote artifacts may change over time without changing the references. While this is desireable in some cases, archiving the entirey of a CNAB at a point of time with artifacts will provide a central location for code auditing and digital forensics of all logic and references used in a CNAB.

## Relocation

After movement of a CNAB to a disconnected envrionment, there may need to be additional mutations to a bundle to adapt to the nuances of a specific disconnected evironment