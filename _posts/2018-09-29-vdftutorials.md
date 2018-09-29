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

### Item Namespace

The VDFItem section of the library is stored in the namespace 'VDFLib.Items'

```csharp
using VDFLib.Items;
```

### Item Types

Before we create an item, lets go through the provided item types.

```
Boolean - VDFBoolItem
Double - VDFDoubleItem
Float - VDFFloatItem
Int - VDFIntItem
Long - VDFLongItem
String - VDFStringItem
Base class - VDFItem
```

You can create your own types of item as well.

### Creating an Item

We can create an item by making a new VDFItem object.

```csharp
VDFItem item = new VDFItem("Name as a string", initialValue);
```

You can replace the second VDFItem with a more specific type of item, such as VDFIntItem.

### Adding an Item to the Root Catagory of a VDF

We can easily add an item object to the root directory of a VDF object.

```csharp
vdf.AddItem(item);
```

### Removing an Item from the Root Catagory of a VDF

We can easily remove an item object from the root directory of a VDF object.

```csharp
vdf.RemoveItem(item);
```

There is also a RemoveItemAt method.

### Creating a Catagory

We can create a catagory by making a new VDFCatagory object.

```csharp
VDFCatagory catagory = new VDFCatagory("Name as a string");
```

### Adding an Item to a Catagory

We can add an item to a catagory via the AddItem method.

```csharp
catagory.AddItem(item);
```

### Removing an Item from a Catagory

We can easily remove an item object from a catagory.

```csharp
catagory.RemoveItem(item);
```

There is also a RemoveItemAt method.

### Adding a Catagory to a VDF

Using the AddCatagory method, we can add a catagory to a VDF.

```csharp
vdf.AddCatagory(catagory);
```

### Removing a Catagory from a VDF

Using the RemoveCatagory method, we can remove a catagory from a VDF.

```csharp
vdf.RemoveCatagory(catagory);
```

There is also a RemoveCatagoryAt method.

### Save a VDF

All below methods return void.

```csharp
vdf.Save();
```

This method saves the VDF at the path stored at the VDFs 'savePath' value. The savePath value is saved. It creates a FileStream which is safely disposed.

```csharp
vdf.Save(filePath);
```

This method saves the VDF by creating a new stream at the path provided and saves via that stream.

```csharp
vdf.Save(fileStream);
```

This method takes in a FileStream and saves via that stream.

### Loading a VDF

All methods below return a VDF object.

These methods use the VDFReader class, a class that has some static utility methods to load a VDF.

```csharp
VDFReader.LoadVDF(path);
```

This method loads a VDF from the file at the specified path.

```csharp
VDFReader.LoadVDF(fileStream)
```

This method loads a VDF from the file loaded in the provided FileStream.

[VDFLib Main Page]({% post_url 2018-09-29-vdflib %})

{% include advertisements.html %}
