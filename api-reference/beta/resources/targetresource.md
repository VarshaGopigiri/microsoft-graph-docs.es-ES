---
title: tipo de recurso targetResource
description: Indica una colección de tipos de recurso de destino asociado con la actividad de auditoría. Cada tipo de recurso de destino heredará las propiedades que se describen a continuación de este recurso.
localization_priority: Normal
ms.openlocfilehash: f86cfe45870292dae93327859c32d38aa2b252fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828682"
---
# <a name="targetresource-resource-type"></a>tipo de recurso targetResource
Indica una colección de tipos de recurso de destino asociado con la actividad de auditoría. Cada tipo de recurso de destino heredará las propiedades que se describen a continuación de este recurso.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|Cadena|Indica el nombre para mostrar de los recursos que se describen en los siguientes tipos de recurso de destino.|
|id|Cadena|Indica el identificador único del recurso (por ejemplo: el identificador de función UserId, AppId,.).|
|modifiedProperties|colección de [modifiedProperty](modifiedproperty.md)|Indica el nombre, el valor anterior y el nuevo valor de cada atributo que ha cambiado. Esto es aplicable para las actividades de "Actualización"|

### <a name="target-resource-types"></a>Tipos de recursos de destino

El tipo de recurso de destino varía según el recurso subyacente:

|Nombre de recurso| Referencia|
|-------------|----------|
Device|[targetResourceDevice](targetresourcedevice.md)
Directorio|[targetResourceDirectory] (targetresourcedirectory.md]
Group|[targetResourceGroup](targetresourcegroup.md)
Directiva|[targetResourcePolicy](targetresourcepolicy.md)
Role|[targetResourceRole](targetresourcerole.md)
Entidad de seguridad de servicio|[targetResourceServicePrincipal](targetresourceserviceprincipal.md)
User|[targetResourceUser](targetresourceuser.md)
Otros|[targetResourceOther](targetresourceother.md)

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
