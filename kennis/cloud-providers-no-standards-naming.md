---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [aws, azure, gcp, interoperability, naming, migration-tools]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# No real standards across cloud providers; identical services, different names

There are no real standards across the three big cloud providers (AWS, Google, Microsoft). Moving e.g. virtual machines from Azure to AWS is not a one-to-one operation, and the same holds for most services. Technically it's possible, but you'll always need a migration tool and/or manual steps (e.g. using PowerShell). All providers offer storage, networking, containers, etc., but for the most part these are not directly interchangeable. Migration tools increasingly appear in the Marketplace, making swapping services possible and easier - something to weigh when assembling an exit strategy.

Each provider invents its own service names. A virtual machine is an EC2 Instance on AWS, an Azure Virtual Machine on Azure, and a Compute Engine on Google. The underlying services/products are virtually identical; the naming is just confusing and hard to track, especially because providers occasionally rename things.

## Bron-citaten (NL, verbatim)

> In het kort: De Cloudprincipes zijn hetzelfde, de product en dienst naamgevingen niet.
