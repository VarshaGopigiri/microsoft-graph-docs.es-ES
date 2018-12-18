---
title: Tipo de recurso windows10NetworkProxyServer
description: Directiva del servidor proxy de red
author: tfitzmac
ms.openlocfilehash: f0f56da348203c2b30a6d49e40e5148f4e7d818b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316824"
---
# <a name="windows10networkproxyserver-resource-type"></a>Tipo de recurso windows10NetworkProxyServer

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





