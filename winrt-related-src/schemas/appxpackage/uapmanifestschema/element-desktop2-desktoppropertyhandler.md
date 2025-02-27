---
ms.assetid: 97d6c3ae-db3f-46c8-b7b0-418bd30bcbdd
title: desktop2:DesktopPropertyHandler
description: Enables declaration of a property handler for a file type association.
ms.date: 04/05/2017
ms.topic: reference
keywords: windows 10, uwp, schema, manifest, desktop, extension 
---

# desktop2:DesktopPropertyHandler

Enables declaration of a property handler for a file type association.

## Element hierarchy

[\<Package\>](element-package.md)

&nbsp;&nbsp;&nbsp;&nbsp;[\<Applications\>](element-applications.md)

&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;[\<Application\>](element-application.md)

&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;[\<Extensions\>](element-1-extensions.md)

&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;[\<uap:Extension\>](element-uap-extension.md)

&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;[\<uap:FileTypeAssociation\>](element-uap-filetypeassociation.md)

&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;**\<desktop2:DesktopPropertyHandler\>**

## Syntax

```xml
<desktop2:DesktopPropertyHandler
  Clsid = 'A GUID in the form xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.'
  ManualSafeSave = 'An optional boolean value.'
  EnableShareDenyNone = 'An optional boolean value.'
  EnableShareDenyWrite = 'An optional boolean value.'
  NoOplock = 'An optional boolean value.' />   
```

## Attributes and elements

### Attributes

| Attribute | Description | Data type | Required | Default value |
|-|-|-|-|-|
| **Clsid** | The ID of the class in the app's package. | A GUID in the form xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. | Yes |  |
| **ManualSafeSave** | Sets STGM_TRANSACTED (true = off). | An optional boolean value. | No |  |
| **EnableShareDenyNone** | Sets STGM_SHARE_DENY_NONE. | An optional boolean value. | No |  |
| **EnableShareDenyWrite** | Sets STGM_SHARE_DENY_WRITE. | An optional boolean value. | No |  |
| **NoOplock** | Disables oplock logic. This is used to close the file if another process attempts to access the file. | An optional boolean value. | No |  |

### Child elements

None.

### Parent elements

| Parent element | Description |
|-|-|
| [uap:FileTypeAssociation](element-uap-filetypeassociation.md) | Declares an app extensibility point of type **windows.fileTypeAssociation**. A file type association indicates that the app is registered to handle files of the specified types. |

## Remarks

Note that the Clsid attribute from PropertyHandler **must** match the ID attribute under the Class element in the [SurrogateServer](element-com-surrogateserver.md) element from the COM registration in the app manifest.

## Requirements

| Item  | Value  |
|--|--|
| Namespace | `http://schemas.microsoft.com/appx/manifest/desktop/windows10/2` |
