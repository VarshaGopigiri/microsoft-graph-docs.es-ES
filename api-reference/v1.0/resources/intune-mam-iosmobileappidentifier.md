---
title: Tipo de recurso iosMobileAppIdentifier
description: El identificador de una aplicación móvil de iOS.
ms.openlocfilehash: dbf37da4f225a42b1686896e3fa1fafa472b4a67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031850"
---
# <a name="iosmobileappidentifier-resource-type"></a>Tipo de recurso iosMobileAppIdentifier

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El identificador de una aplicación móvil de iOS.

Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|bundleId|cadena|El identificador de una aplicación, como se especifica en la tienda de aplicaciones.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMobileAppIdentifier",
  "bundleId": "String"
}
```



