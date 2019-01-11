---
title: Tipo de recurso mimeContent
description: Contiene las propiedades de un contenido MIME genérico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a0b63289b3d7666eb27de7e6dc4e643dd9fa4772
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857046"
---
# <a name="mimecontent-resource-type"></a>Tipo de recurso mimeContent

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de un contenido MIME genérico.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|type|String|Indica el tipo de contenido MIME.|
|valor|Binario|Matriz de bytes que contiene el contenido real.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mimeContent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mimeContent",
  "type": "String",
  "value": "binary"
}
```



