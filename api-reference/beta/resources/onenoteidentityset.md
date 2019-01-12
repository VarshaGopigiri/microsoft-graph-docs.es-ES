---
title: tipo de recurso oneNoteIdentitySet
description: '**Compatibilidad con próximamente**'
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 9043b08a8586bcc9a0043a2fde13f0d5d9eea4a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947172"
---
# <a name="onenoteidentityset-resource-type"></a>tipo de recurso oneNoteIdentitySet

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

**Compatibilidad con próximamente**

El tipo de OneNoteIdentitySet es una colección de claves de objetos [OneNoteIdentity](onenoteidentity.md) .
Se usa para representar un conjunto de identidades asociado con varios eventos para un _Bloc de notas_, _sección_ o _página_, como _creado por_ o _modificado por última vez_. 
 
Actualmente contiene una clave, un solo _**usuario**_.  En el futuro, se pueden agregar claves como el dispositivo o la aplicación para cambiar el elemento.

En el futuro, este tipo se combinarán con [IdentitySet](identityset.md)

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteidentityset"
}-->

```json
{
  "user": {"@odata.type": "microsoft.graph.oneNoteIdentity"}
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|usuario|[oneNoteIdentity](onenoteidentity.md)|Un recurso de OneNoteIdentity que representa a un usuario.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oneNoteIdentitySet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
