---
title: Tipo de recurso educationRoot
description: 'El espacio de nombres `/education` expone funcionalidad específica del sector educativo. '
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: c268c7b910bd9f6f14763f3a7b5445af0ac12826
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890660"
---
# <a name="educationroot-resource-type"></a>Tipo de recurso educationRoot

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRoot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
