---
title: tipo de recurso targetResource
description: Indica una colección de tipos de recurso de destino asociado con la actividad de auditoría. Cada tipo de recurso de destino heredará las propiedades que se describen a continuación de este recurso.
ms.openlocfilehash: ba3bee7ce89f73ed97610d62676c22d14488ed9f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083563"
---
# <a name="targetresource-resource-type"></a>tipo de recurso targetResource
Indica una colección de tipos de recurso de destino asociado con la actividad de auditoría. Cada tipo de recurso de destino heredará las propiedades que se describen a continuación de este recurso.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|Indica el nombre para mostrar de los recursos que se describen en los siguientes tipos de recurso de destino.|
|id|String|Indica el identificador único del recurso (por ejemplo: el identificador de función UserId, AppId,.).|
|modifiedProperties|colección de [modifiedProperty](modifiedproperty.md)|Indica el nombre, el valor anterior y el nuevo valor de cada atributo que ha cambiado. Esto es aplicable para las actividades de "Actualización"|

### <a name="target-resource-types"></a>Tipos de recursos de destino

El tipo de recurso de destino varía según el recurso subyacente:

|Nombre de recurso| Referencia|
|-------------|----------|
Dispositivo|[targetResourceDevice](targetresourcedevice.md)
Directorio|[targetResourceDirectory] (targetresourcedirectory.md]
Group|[targetResourceGroup](targetresourcegroup.md)
Directiva|[targetResourcePolicy](targetresourcepolicy.md)
Role|[targetResourceRole](targetresourcerole.md)
Entidad de seguridad de servicio|[targetResourceServicePrincipal](targetresourceserviceprincipal.md)
User|[targetResourceUser](targetresourceuser.md)
Otro|[targetResourceOther](targetresourceother.md)

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResource"
}-->

```json
{
  "displayName": "String",
  "id": "String",
  "modifiedProperties": [{"@odata.type": "microsoft.graph.modifiedProperty"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->