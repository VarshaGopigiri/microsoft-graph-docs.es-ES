---
title: Tipo de recurso de extremo
description: 'Los extremos representan las direcciones URL para los recursos asociados a una entidad.  Por ejemplo, cuando se crea un nuevo grupo de Office 365, también se crean los recursos adicionales como parte del grupo de Office 365. Éstas incluyen aspectos como un buzón de grupo para las conversaciones y una carpeta de OneDrive de grupo para los documentos y archivos. Ahora se puede leer para obtener más información acerca de estos recursos de grupo de Office 365, incluidos sus direcciones URL de recursos asociados utilizando la navegación de *extremos* en el tipo de recurso de grupo. Esto permite a las aplicaciones comprender estos recursos e incluso incrustar el recurso de que dirección URL se pueden observar en sus propias experiencias. '
localization_priority: Normal
ms.openlocfilehash: 5a342bee0a1918eb142542693198173239d1b3c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871291"
---
# <a name="endpoint-resource-type"></a>Tipo de recurso de extremo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Los extremos representan las direcciones URL para los recursos asociados a una entidad.  Por ejemplo, cuando se crea un nuevo grupo de Office 365, también se crean los recursos adicionales como parte del grupo de Office 365. Éstas incluyen aspectos como un buzón de grupo para las conversaciones y una carpeta de OneDrive de grupo para los documentos y archivos. Ahora se puede leer para obtener más información acerca de estos recursos de grupo de Office 365, incluidos sus direcciones URL de recursos asociados utilizando la navegación de *extremos* en el tipo de recurso de grupo. Esto permite a las aplicaciones comprender estos recursos e incluso incrustar el recurso de que dirección URL se pueden observar en sus propias experiencias. 

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Extremos de lista](../api/group-list-endpoints.md) |Colección de [extremo](endpoint.md)| Obtener una colección de objetos de extremo. |
|[Obtener el extremo](../api/endpoint-get.md) | [Punto de conexión](endpoint.md) |Leer las propiedades y relaciones de un objeto de extremo.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
| capacidad     | Cadena  | Describe la capacidad que está asociada a este recurso. (por ejemplo, los mensajes, las conversaciones, etcetera.)  No acepta valores NULL. Solo lectura. |
| id             | Cadena  | Identificador único para el extremo; Clave. No admite valores NULL. Solo lectura.|
| providerId     | Cadena  | Identificador de aplicación de la publicación subyacentes de servicio. No admite valores NULL. Solo lectura.|
| providerName   | Cadena  | Nombre de la publicación subyacentes de servicio. Solo lectura.|
| providerResourceId|Cadena| Para los grupos de Office 365, esto se establece en un nombre para el recurso (por ejemplo, Yammer.FeedURL etcetera.) conocido. No admite valores NULL. Solo lectura.|
| URI            | Cadena  | Dirección URL del recurso publicado. No admite valores NULL. Solo lectura.|

## <a name="relationships"></a>Relaciones

Ninguna.


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.Endpoint"
}-->

```json
{
  "capability": "String",
  "id": "String (identifier)",
  "providerId": "String",
  "providerName": "String",
  "providerResourceId": "String",
  "uri": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Endpoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
