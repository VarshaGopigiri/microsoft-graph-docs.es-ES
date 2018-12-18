---
title: Tipo de recurso educationRoot
description: 'El espacio de nombres `/education` expone funcionalidad específica del sector educativo. '
author: mmast-msft
ms.openlocfilehash: 11aaaec20ccd688b16b74224d1a8c6937e52c5cd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342472"
---
# <a name="educationroot-resource-type"></a>Tipo de recurso educationRoot

El espacio de nombres `/education` expone funcionalidad específica del sector educativo. Algunos objetos del espacio de nombres `/education` pueden encontrarse en otras partes de Microsoft Graph (por ejemplo, [users](user.md)). El espacio de nombres de educación ofrece características y propiedades específicas del ámbito educativo en esos objetos.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear educationClass](../api/educationroot-post-classes.md) |[educationClass](educationclass.md)| Cree un objeto **educationClass** publicando en la colección de clases.|
|[Enumerar clases](../api/educationroot-list-classes.md) |Colección [educationClass](educationclass.md)| Obtenga una colección de objetos **educationClass**.|
|[Crear educationSchool](../api/educationroot-post-schools.md) |[educationSchool](educationschool.md)| Cree un objeto **educationSchool** publicando en la colección de centros educativos.|
|[Enumerar centros educativos](../api/educationroot-list-schools.md) |Colección [educationSchool](educationschool.md)| Obtenga una colección de objetos **educationSchool**.|
|[Crear educationUser](../api/educationroot-post-users.md) |[educationUser](educationuser.md)| Cree un objeto **educationUser** publicando en la colección de usuarios.|
|[Enumerar usuarios](../api/educationroot-list-users.md) |Colección [educationUser](educationuser.md)| Obtenga una colección de objetos **educationUser**.|

## <a name="properties"></a>Propiedades
Ninguna.

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classes|Colección [educationClass](educationclass.md)| Solo lectura. Admite valores NULL.|
|me|[educationUser](educationuser.md)| Solo lectura. Admite valores NULL.|
|schools|Colección [educationSchool](educationschool.md)| Solo lectura. Admite valores NULL.|
|users|Colección [educationUser](educationuser.md)| Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.educationRoot"
}-->

```json
{
}
```

<!-- {
  "blockType": "request",
  "name": "get_education"
}-->
```http
GET https://graph.microsoft.com/v1.0/education
```

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationRoot"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRoot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->