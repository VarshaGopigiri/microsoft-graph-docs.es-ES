---
title: Tipo de recurso profilePhoto
description: Foto de perfil de un usuario, grupo o un contacto de Outlook al que se accede desde Exchange Online. Son datos binarios no codificados en base 64.
localization_priority: Priority
ms.openlocfilehash: b1901928a97356b2a9808a446d34981fd74bf456
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876569"
---
# <a name="profilephoto-resource-type"></a>Tipo de recurso profilePhoto
Foto de perfil de un usuario, grupo o un contacto de Outlook al que se accede desde Exchange Online. Son datos binarios no codificados en base 64.

Los tamaños de fotos HD admitidos en Exchange Online son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'. 

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get profilePhoto](../api/profilephoto-get.md) | [profilePhoto](profilephoto.md) |Obtiene el **profilePhoto** especificado o sus metadatos (propiedades profilePhoto).|
|[Update](../api/profilephoto-update.md) | [profilePhoto](profilephoto.md)  |Asigna una foto al usuario, grupo o contacto que se especifique. La foto debe estar en formato binario. Reemplaza la foto existente, si existe.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|Solo lectura.|
|height|int32|Alto de la foto. Solo lectura.|
|width|int32|Ancho de la foto. Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "isMediaEntity": true,
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.profilePhoto"
}-->

```json
{
  "id": "240X240",
  "height": 240,
  "width": 240
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "profilePhoto resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
