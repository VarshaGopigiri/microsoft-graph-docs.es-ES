---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3a5204a4704eefc2d4e7c8e0d5b3b709e1750667
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937484"
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



