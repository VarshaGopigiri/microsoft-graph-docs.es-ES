---
title: Tipo de recurso windows10NetworkProxyServer
description: Directiva del servidor proxy de red
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7efe08c565aaeab109339c43e80225b6946299c3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876261"
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





