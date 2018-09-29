---
layout: post
title: "VDF Tutorial"
date: 2018-08-29 18:26:18
---

## VDF Tutorials and Examples

This post will tell you how to use the C# VDF library.

### Namespace

All of the VDF Lib (except items) is included in the VDFLib namespace.

Make sure to include this at the top of any file you wish to use the API in:

```csharp
using VDFLib;
```

### Creating a VDF

You must create a VDF object to add items and catagories to it.

```csharp
VDF vdf = new VDF("Put a vdf name here as a string");
```

[VDFLib Main Page]({% post_url 2018-09-29-vdflib %})

{% include advertisements.html %}
