---
title: Tipo de recurso proxiedDomain
description: Dominio con proxy
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dc90ebd57752fedcaf7acf069da6e653da04978e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968550"
---
# <a name="proxieddomain-resource-type"></a>Tipo de recurso proxiedDomain

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dominio con proxy
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|ipAddressOrFQDN|cadena|La dirección IP o FQDN|
|proxy|cadena|IP de proxy|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.proxiedDomain"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.proxiedDomain",
  "ipAddressOrFQDN": "String",
  "proxy": "String"
}
```



