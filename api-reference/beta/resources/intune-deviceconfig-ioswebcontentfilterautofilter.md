---
title: tipo de recurso iosWebContentFilterAutoFilter
description: Representa un tipo de configuración de filtro de contenido Web, que habilita la característica de filtro automático de iOS y permite para control de acceso de dirección URL adicional de iOS. Cuando se construye sin valores de propiedad, el dispositivo iOS habilitará el filtro automático independientemente.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 03e3c4f51e673be1e2bada89e06a26048fe4e385
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916784"
---
# <a name="ioswebcontentfilterautofilter-resource-type"></a>tipo de recurso iosWebContentFilterAutoFilter

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un tipo de configuración de filtro de contenido Web, que habilita la característica de filtro automático de iOS y permite para control de acceso de dirección URL adicional de iOS. Cuando se construye sin valores de propiedad, el dispositivo iOS habilitará el filtro automático independientemente.

Hereda de [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|allowedUrls|Colección String|Direcciones URL adicionales permitidas para el acceso|
|blockedUrls|Colección String|Bloqueada el acceso de las direcciones URL adicionales|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosWebContentFilterAutoFilter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosWebContentFilterAutoFilter",
  "allowedUrls": [
    "String"
  ],
  "blockedUrls": [
    "String"
  ]
}
```





