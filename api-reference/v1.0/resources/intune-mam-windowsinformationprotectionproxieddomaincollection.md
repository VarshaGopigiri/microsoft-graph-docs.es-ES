---
title: Tipo de recurso windowsInformationProtectionProxiedDomainCollection
description: Colección de dominios con proxy de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: c95c54c5bbfcc1b5202a0c56a6e3932b35ffac88
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309474"
---
# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a>Tipo de recurso windowsInformationProtectionProxiedDomainCollection

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Colección de dominios con proxy de Windows Information Protection
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar|
|proxiedDomains|Colección [proxiedDomain](../resources/intune-mam-proxieddomain.md)|Conjunto de dominios con proxy|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
  "displayName": "String",
  "proxiedDomains": [
    {
      "@odata.type": "microsoft.graph.proxiedDomain",
      "ipAddressOrFQDN": "String",
      "proxy": "String"
    }
  ]
}
```



