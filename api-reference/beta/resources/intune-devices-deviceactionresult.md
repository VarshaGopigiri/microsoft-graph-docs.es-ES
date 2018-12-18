---
title: Tipo de recurso deviceActionResult
description: Resultado de la acción de dispositivo
author: tfitzmac
ms.openlocfilehash: fd2160c501820ec04a94b618b3456a3f8fafa6cd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324951"
---
# <a name="deviceactionresult-resource-type"></a>Tipo de recurso deviceActionResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resultado de la acción de dispositivo
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|actionName|cadena|Nombre de acción|
|actionState|[actionState](../resources/intune-shared-actionstate.md)|Estado de la acción. Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.|
|startDateTime|DateTimeOffset|Hora a la que se inició la acción|
|lastUpdatedDateTime|DateTimeOffset|Hora en la que se actualizó por última vez el estado de la acción|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```





