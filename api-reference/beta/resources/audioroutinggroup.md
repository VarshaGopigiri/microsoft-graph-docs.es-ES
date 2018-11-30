---
title: tipo de recurso audioRoutingGroup
description: El grupo de enrutamiento de audio almacena una ruta de audio privada entre los participantes en una conversación entre varias partes. Origen es el participante propio y los receptores son un subconjunto de los otros participantes de la conversación entre varias partes.
ms.openlocfilehash: 98c58e39773567f13a2723e94c0413efd2841cd0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083500"
---
# <a name="audioroutinggroup-resource-type"></a>tipo de recurso audioRoutingGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El grupo de enrutamiento de audio almacena una ruta de audio privada entre los participantes en una conversación entre varias partes. Origen es el participante propio y los receptores son un subconjunto de los otros participantes de la conversación entre varias partes.

> **Nota:** [ConfigureMixer](../api/participant-configuremixer.md) implican las rutas, para toda la llamada para establecer los niveles de volumen para combinaciones de receptor de origen.

## <a name="methods"></a>Métodos

| Método                                                  | Tipo de valor devuelto                               | Descripción                                  |
|:--------------------------------------------------------|:------------------------------------------|:---------------------------------------------|
| [Obtener audioRoutingGroup](../api/audioroutinggroup-get.md)| [audioRoutingGroup](audioroutinggroup.md) | Leer las propiedades y las relaciones del objeto audioRoutingGroup.|
| [Update](../api/audioroutinggroup-update.md)            | [audioRoutingGroup](audioroutinggroup.md) | Actualizar lista de receptores.                       |
| [Delete](../api/audioroutinggroup-delete.md)            | Ninguno                                      | Eliminar el grupo de enrutamiento de audio.              |

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo              | Descripción                                                          |
| :----------   | :---------------- | :--------------------------------------------------------------------|
| id            | String            | Solo lectura. Servidor que se generó.                                         |
| receptores de     | Colección de cadenas | Lista de la recepción de los identificadores de participantes.                                   |
| routingMode   | String            | Modo de grupo de enrutamiento.  Los valores posibles son: `oneToOne` y `multicast`.   |
| orígenes       | Colección de cadenas | Lista de identificadores de participantes de origen.                                      |

> **Nota:** Modo de enrutamiento determina las restricciones en los orígenes y receptores. Se admiten sólo los siguientes grupos de enrutamiento.
> - `oneToOne`-orígenes y receptores tienen un único participante.
> - `multicast`-origen tiene un participante pero hay varios receptores. Lista de receptores puede actualizarse.

> **Nota:** Si crea varios grupos de enrutamiento Audioconferencias (por ejemplo, un bot por participante), se transfiere sólo el sonido de los altavoces dominantes 4 superiores. Significa incluso con el grupo de enrutamiento de audio personalizado, si el altavoz no es lo suficientemente alto como en el mezclador principal, éste no podrán oír el robot incluso si hay un grupo de audio privado solo para este altavoz y el robot.

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioRoutingGroup"
}-->
```json
{
  "id": "String (identifier)",
  "receivers": [ "String" ],
  "routingMode": "oneToOne | multicast",
  "sources": [ "String" ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioRoutingGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
