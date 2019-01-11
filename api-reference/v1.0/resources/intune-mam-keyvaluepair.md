---
title: Tipo de recurso keyValuePair
description: Par clave-valor para almacenar la configuración personalizada
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 44f1765fb4f03a287665fe4ed1faef7012a43459
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805897"
---
# <a name="keyvaluepair-resource-type"></a>Tipo de recurso keyValuePair

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Par clave-valor para almacenar la configuración personalizada
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|name|cadena|Nombre de este par clave-valor|
|valor|cadena|Valor de este par clave-valor|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.keyValuePair"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.keyValuePair",
  "name": "String",
  "value": "String"
}
```



