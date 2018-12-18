---
title: Tipo de recurso exclusionGroupAssignmentTarget
description: Representa un grupo que debería excluirse de una tarea.
author: tfitzmac
ms.openlocfilehash: 783231c451668169ba85e8ce1cfecd669b5c0b7d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343186"
---
# <a name="exclusiongroupassignmenttarget-resource-type"></a>Tipo de recurso exclusionGroupAssignmentTarget

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





