---
title: tipo de recurso managedDeviceModelsAndManufacturers
description: Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 86d9f9dd0642abab73f6b750b997c75851f6be02
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875624"
---
# <a name="manageddevicemodelsandmanufacturers-resource-type"></a>tipo de recurso managedDeviceModelsAndManufacturers

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|deviceModels|Colección String|Lista de modelos para los dispositivos administrados en la cuenta|
|deviceManufacturers|Colección String|Lista de fabricantes de los dispositivos administrados en la cuenta|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceModelsAndManufacturers"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceModelsAndManufacturers",
  "deviceModels": [
    "String"
  ],
  "deviceManufacturers": [
    "String"
  ]
}
```





