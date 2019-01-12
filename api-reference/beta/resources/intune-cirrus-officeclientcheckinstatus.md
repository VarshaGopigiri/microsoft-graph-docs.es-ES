---
title: tipo de recurso officeClientCheckinStatus
description: Entidad que describe el inquilino protección de estadísticas.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a387e04b9ebc15d65eb8dd883ecd4a9bae78ad6d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969292"
---
# <a name="officeclientcheckinstatus-resource-type"></a>tipo de recurso officeClientCheckinStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que describe el inquilino protección de estadísticas.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|userPrincipalName|Cadena|Nombre principal de usuario con el dispositivo.|
|deviceName|Cadena|Nombre del dispositivo intenta protección.|
|devicePlatform|Cadena|Plataforma de dispositivo intenta protección.|
|devicePlatformVersion|Cadena|Versión de plataforma de dispositivo intenta protección.|
|wasSuccessful|Booleano|Si el último registro se realizó correctamente.|
|userId|Cadena|Identificador de usuario usando el dispositivo.|
|checkinDateTime|DateTimeOffset|Dispositivo última verificación en hora en UTC.|
|errorMessage|Cadena|Aparece un mensaje de error si hay alguno asociado para el último registro.|
|appliedPolicies|Colección String|Lista de directivas de entrega en el dispositivo como último checkin.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeClientCheckinStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeClientCheckinStatus",
  "userPrincipalName": "String",
  "deviceName": "String",
  "devicePlatform": "String",
  "devicePlatformVersion": "String",
  "wasSuccessful": true,
  "userId": "String",
  "checkinDateTime": "String (timestamp)",
  "errorMessage": "String",
  "appliedPolicies": [
    "String"
  ]
}
```



