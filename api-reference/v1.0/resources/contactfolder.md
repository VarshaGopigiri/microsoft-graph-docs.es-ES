---
title: Tipo de recurso contactFolder
description: Una carpeta que contiene contactos.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 14d7ddef1f8acae183e406f85582153905130cda
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886110"
---
# <a name="contactfolder-resource-type"></a>Tipo de recurso contactFolder

Una carpeta que contiene contactos.

Este recurso es compatible con el uso de una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contactfolder-delta.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener contactFolder](../api/contactfolder-get.md) | [contactFolder](contactfolder.md) |Obtenga una carpeta de contactos mediante el identificador de carpeta de contactos.|
|[Actualizar](../api/contactfolder-update.md) | [contactFolder](contactfolder.md) |Actualice el objeto contactFolder. |
|[Eliminar](../api/contactfolder-delete.md) | Ninguno |Elimine el objeto contactFolder. |
|[Enumerar childFolders](../api/contactfolder-list-childfolders.md) |Colección [ContactFolder](contactfolder.md)| Obtenga una colección de carpetas secundarias en la carpeta de contactos especificada.|
|[Crear contactFolder secundario](../api/contactfolder-post-childfolders.md) |[ContactFolder](contactfolder.md)| Cree una contactFolder como elemento secundario de una carpeta especificada.|
|[delta](../api/contact-delta.md)|Colección [contact](contact.md)| Obtenga un conjunto de carpetas de contactos que se hayan agregado, eliminado o quitado del buzón del usuario.|
|[Enumerar contactos en la carpeta](../api/contactfolder-list-contacts.md) |Colección [contact](contact.md)| Obtenga una colección de contactos de la carpeta de contactos predeterminada del usuario que ha iniciado sesión (`.../me/contacts`) o de la carpeta de contactos especificada.|
|[Crear contacto en la carpeta](../api/contactfolder-post-contacts.md) |[Contact](contact.md)| Agregue un contacto a la carpeta de contactos raíz o al extremo de `contacts` de otra carpeta de contactos.|
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[contactFolder](contactfolder.md)  |Cree una o varias propiedades extendidas de valor único en un objeto contactFolder nuevo o existente.   |
|[Obtener contactFolder con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [contactFolder](contactfolder.md) | Obtenga objetos contactFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [contactFolder](contactfolder.md) | Cree una o varias propiedades extendidas de varios valores en un objeto contactFolder nuevo o existente.  |
|[Obtener contactFolder con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [contactFolder](contactfolder.md) | Obtenga un objeto contactFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|El nombre para mostrar de la carpeta.|
|id|String|Identificador único de la carpeta de contactos. Solo lectura.|
|parentFolderId|String|El identificador de la carpeta principal de la carpeta.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|childFolders|Colección [ContactFolder](contactfolder.md)|La colección de carpetas secundarias de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.|
|contactos|Colección [contact](contact.md)|Los contactos de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "contacts",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.contactFolder",
  "@odata.annotations": [
    {
      "property": "childFolders",
      "capabilities": {
        "navigability": "single",
        "changeTracking": false,
        "searchable": false
      }
    },
    {
      "property": "contacts",
      "capabilities": {
        "changeTracking": true,
        "navigability": "single",
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string"
}

```

## <a name="see-also"></a>Consulte también

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview)
- [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contactFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
