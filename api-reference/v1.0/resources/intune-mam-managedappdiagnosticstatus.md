---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
ms.openlocfilehash: 8a462b49231323288d66a660c769ce7359cb5ab3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031021"
---
# <a name="managedappdiagnosticstatus-resource-type"></a>Tipo de recurso managedAppDiagnosticStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa el estado de diagnóstico.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|validationName|cadena|El nombre descriptivo de validación|
|estado|cadena|El estado actual de la operación.|
|mitigationInstruction|cadena|Instrucciones sobre cómo reducir un error de validación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedAppDiagnosticStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppDiagnosticStatus",
  "validationName": "String",
  "state": "String",
  "mitigationInstruction": "String"
}
```



