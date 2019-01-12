---
title: Tipo de recurso vppLicensingType
description: Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 47ee634c8fa488bb27c6c0a4beb7728fc7e427cb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948684"
---
# <a name="vpplicensingtype-resource-type"></a>Tipo de recurso vppLicensingType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|supportUserLicensing|Booleano|Si el programa es compatible con el tipo de licencia de usuario.|
|supportDeviceLicensing|Booleano|Si el programa es compatible con el tipo de licencia de dispositivo.|
|supportsUserLicensing|Booleano|Si el programa es compatible con el tipo de licencia de usuario.|
|supportsDeviceLicensing|Booleano|Si el programa es compatible con el tipo de licencia de dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppLicensingType"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppLicensingType",
  "supportUserLicensing": true,
  "supportDeviceLicensing": true,
  "supportsUserLicensing": true,
  "supportsDeviceLicensing": true
}
```





