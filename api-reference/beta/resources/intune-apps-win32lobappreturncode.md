---
title: tipo de recurso win32LobAppReturnCode
description: Contiene las propiedades de código de retorno para una aplicación de Win32
ms.openlocfilehash: 5f32e7e5953ade1036c49ac2fb45555fd353fa1d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084961"
---
# <a name="win32lobappreturncode-resource-type"></a>tipo de recurso win32LobAppReturnCode

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de código de retorno para una aplicación de Win32
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|returnCode|Int32|Código de retorno.|
|type|[win32LobAppReturnCodeType](../resources/intune-apps-win32lobappreturncodetype.md)|El tipo de código de retorno. Los valores posibles son: `failed`, `success`, `softReboot`, `hardReboot` y `retry`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppReturnCode"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppReturnCode",
  "returnCode": 1024,
  "type": "String"
}
```





