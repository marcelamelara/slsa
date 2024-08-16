---
title: Hosting build environments
description: This page covers the detailed technical requirements for hosting build environments at each SLSA Environment level. The intended audience is build platform implementers, compute infrastructure providers and security engineers.
---

For an informative description of the levels intended for all audiences, see
[Environment Levels](attested-build-env-levels.md).

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD",
"SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be
interpreted as described in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119).

## Overview

### Environment levels

In order to host build environments with a specific Environment level,
responsibility lies primarily with the [build platform], although
higher Environment levels also add responsibilities for the underlying
[compute platform]. The build platform MUST adopt certain security measures
and meet specific [Build levels] in order to achieve a specific level. To
achieve Environment L3 or L4, the build platform MUST select a compute
platform that supports certain types of hardware features. Software
[producers] seeking further integrity properties and accoutjability for
their builds MAY choose a hosted build platform capable of achieving a
desired Environment level.

<table class="no-alternate">
<tr>
  <th>Implementer
  <th>Requirement
  <th>Degree
  <th>L1<th>L2<th>L3<th>L4
<tr>
  <td rowspan=3><a href="#build-platform">Build platform</a>
  <td colspan=2><a href="#follow-slsa">Follow SLSA Build track</a>
  <td>✓<td>✓<td>✓<td>✓
<tr>
  <td rowspan=3><a href="#build-env-measurement">Build environment measurement</a>
  <td><a href="#augmented-measured-boot">Augmented measured boot</a>
  <td> <td>✓<td>✓<td>✓
<tr>
  <td><a href="#measured-dispatch">Measured dispatch</a>
  <td> <td> <td>✓<td>✓
<tr>
  <td><a href="#encrypted">Encrypted</a>
  <td> <td> <td>✓<td>✓
<tr>
  <td colspan=2><a href="#select-specific-compute">Select a specific compute platform</a>
  <td><td><td>✓<td>✓
<tr>
  <td rowspan=6><a href="#compute-platform">Compute platform</a>
  <td rowspan=3><a href="#platform-">Platform trust</a>
  <td><a href="#trusted-boot">Trusted Boot</a>
  <td><td><td>✓<td>✓
<tr>
  <td><a href="#trusted-execution">Trusted Execution</a>
  <td><td><td><td>✓
</table>
