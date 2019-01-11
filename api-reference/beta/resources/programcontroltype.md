---
title: tipo de recurso programControlType
description: 'En el anuncio de Azure access revisa la característica, el tipo de control de programa se utiliza cuando el control se asocia un control a un programa, para indicar el tipo de revisión de access es para.  '
localization_priority: Normal
ms.openlocfilehash: 0091c23fd5d537e7c1fd62051778e56b510a3dab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808235"
---
# <a name="programcontroltype-resource-type"></a>tipo de recurso programControlType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el tipo de control de programa se usa al asociar un control a un programa, para indicar el tipo de revisión de acceso para que es el control.  

Los objetos de tipo de control de programa se generan automáticamente cuando el onboards el inquilino de para usar el acceso de administrador global revisa la característica.  No se puede crear ningún tipo de control de programa adicionales.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista programControlTypes](../api/programcontroltype-list.md) | colección de [programControlType](programcontroltype.md)| Lista de tipos de control de programa. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
| `id`                     |`String`                | El identificador asignado a la función del tipo de control de programa                                      |
| `displayName`            |`String`                | El nombre del tipo de control de programa                                                             |


## <a name="relationships"></a>Relaciones

Ninguno.


## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear programControl](../api/programcontrol-create.md) |     [programControl](programcontrol.md) |   Agregar un programControl a un programa.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.programControlType"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "programControlType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
