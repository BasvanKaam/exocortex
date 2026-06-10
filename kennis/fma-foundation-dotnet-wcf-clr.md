---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, dotnet, wcf, clr, architecture, foundation]
layer: reference
bron: inside-citrix-fma
---

# FMA foundation: .NET, WCF, CLR and just-in-time compilation

The FlexCast Management Architecture is a Microsoft .NET-based, service-orientated architecture built on the WCF (Windows Communication Foundation) framework. Its deployment model is based on Controllers (and agents) running multiple highly available, stateless services.

The layering Bas untangles:
- The .NET Framework (first beta late 2000, developed by Microsoft in the late 1990s) provides language interoperability across multiple languages via a large Framework Class Library (FCL).
- WCF is itself built using the .NET Framework; it is a runtime plus a set of APIs for sending messages between services and clients (local or over the Internet).
- Visual Studio uses WCF as its base development platform, and from there the FMA/XenDesktop is created.

.NET applications run in the Common Language Runtime (CLR), the virtual-machine component of .NET. At execution, just-in-time (JIT) compilation converts compiled code into machine instructions run by the CPU in the CLR. The CLR also provides garbage collection, memory management and type safety. Supported .NET languages: Visual Basic, Visual C#, Visual F#, Visual C++. Citrix offers SDKs, APIs and a free Citrix Developer Visual Studio Extension ('Google for Citrix developer overview').

Note: the book abbreviates the Common Language Runtime as 'CRL' throughout, but the correct acronym is CLR.

## Verwante notities

- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [FMA services: Network Service account and service isolation](fma-services-network-account-and-isolation.md)
