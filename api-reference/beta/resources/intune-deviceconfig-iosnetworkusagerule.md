---
title: Tipo de recurso iosNetworkUsageRule
description: Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 7476f49c6049eb18e56fa57310aa75707f566bd0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912025"
---
# <a name="iosnetworkusagerule-resource-type"></a>Tipo de recurso iosNetworkUsageRule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|managedApps|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Información sobre las aplicaciones administradas a las que se va a aplicar esta regla. Esta colección puede contener un máximo de 500 elementos.|
|cellularDataBlockWhenRoaming|Booleano|Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en itinerancia.|
|cellularDataBlocked|Booleano|Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en ningún momento.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNetworkUsageRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNetworkUsageRule",
  "managedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "cellularDataBlockWhenRoaming": true,
  "cellularDataBlocked": true
}
```





