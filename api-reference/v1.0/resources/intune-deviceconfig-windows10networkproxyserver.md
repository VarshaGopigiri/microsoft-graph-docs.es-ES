---
title: Tipo de recurso windows10NetworkProxyServer
description: Directiva del servidor proxy de red
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4e9f727916f055fe197f98b07625b00406e16e83
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921104"
---
# <a name="windows10networkproxyserver-resource-type"></a>Tipo de recurso windows10NetworkProxyServer

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva del servidor proxy de red
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|address|Cadena|Dirección del servidor proxy. Especifique una dirección en formato <server>\[":"<port>\]|
|excepciones|Colección string|Direcciones que el servidor proxy no debe usar. El sistema no usará el servidor proxy para las direcciones que empiecen por lo que se especifica en este nodo.|
|useForLocalAddresses|Booleano|Especifica si el servidor proxy se debe usar para direcciones locales (intranet).|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10NetworkProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10NetworkProxyServer",
  "address": "String",
  "exceptions": [
    "String"
  ],
  "useForLocalAddresses": true
}
```



