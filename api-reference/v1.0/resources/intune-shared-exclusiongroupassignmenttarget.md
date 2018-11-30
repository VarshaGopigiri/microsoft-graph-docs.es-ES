---
title: Tipo de recurso exclusionGroupAssignmentTarget
description: Representa un grupo que debería excluirse de una tarea.
ms.openlocfilehash: fdbb463687d75791965db2ef05abfea1a269d1a1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031227"
---
# <a name="exclusiongroupassignmenttarget-resource-type"></a>Tipo de recurso exclusionGroupAssignmentTarget

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un grupo que debería excluirse de una tarea.

Hereda de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|groupId|cadena|El identificador de grupo que es el destino de la tarea. Heredado de [groupAssignmentTarget](../resources/intune-shared-groupassignmenttarget.md)|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.exclusionGroupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.exclusionGroupAssignmentTarget",
  "groupId": "String"
}
```



