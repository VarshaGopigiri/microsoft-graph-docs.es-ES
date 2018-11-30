---
title: tipo de recurso managedDeviceModelsAndManufacturers
description: Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta
ms.openlocfilehash: c61026a6caa097e01e09a4343dd54f769c743460
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090945"
---
# <a name="manageddevicemodelsandmanufacturers-resource-type"></a>tipo de recurso managedDeviceModelsAndManufacturers

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
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





