---
title: "deviceManagement resource type"
description: "Singleton that acts as container for a collection of Resource Access entities."
author: "jaiprakashmb"
ms.localizationpriority: medium
ms.subservice: "intune"
doc_type: resourcePageType
ms.date: 09/12/2024
---

# deviceManagement resource type

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Singleton that acts as container for a collection of Resource Access entities.

## Methods
|Method|Return Type|Description|
|:---|:---|:---|
|[Get deviceManagement](../api/intune-chromebooksync-devicemanagement-get.md)|[deviceManagement](../resources/intune-chromebooksync-devicemanagement.md)|Read properties and relationships of the [deviceManagement](../resources/intune-chromebooksync-devicemanagement.md) object.|
|[Update deviceManagement](../api/intune-chromebooksync-devicemanagement-update.md)|[deviceManagement](../resources/intune-chromebooksync-devicemanagement.md)|Update the properties of a [deviceManagement](../resources/intune-chromebooksync-devicemanagement.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|Id of ChromeOSOnboardingSettings.|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|chromeOSOnboardingSettings|[chromeOSOnboardingSettings](../resources/intune-chromebooksync-chromeosonboardingsettings.md) collection|Collection of ChromeOSOnboardingSettings settings associated with account.|

## JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```
