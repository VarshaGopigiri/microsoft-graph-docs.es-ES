---
title: tipo de recurso historyItem
description: Representa un elemento de historial para una actividad en una aplicación. Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.
localization_priority: Normal
ms.openlocfilehash: 510913be6a3f70190c7cf657d9540d75f481c3a9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882918"
---
# <a name="historyitem-resource-type"></a>tipo de recurso historyItem

Representa un elemento de historial para una [actividad](projectrome-activity.md) en una aplicación. Actividades de usuario representan un destino único dentro de la aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.

Cuando una aplicación crea una sesión, se debe agregar un objeto **historyItem** para el objeto de **actividad** para reflejar el período de contratación de usuario. Cada vez que volver a contrata a un usuario con una actividad, se agrega un nuevo **historyItem** a la actividad para acumular compromiso de usuario.

## <a name="methods"></a>Métodos

|Método | Tipo de valor devuelto | Descripción|
|:------|:------------|:-----------|
|[Crear o reemplazar historyItem](../api/projectrome-put-historyitem.md) | [historyItem](projectrome-historyitem.md) | Crea o reemplaza una existente **historyItem** para esa actividad (upsert). El identificador debe ser un GUID.|
|[Eliminar un historyItem](../api/projectrome-delete-historyitem.md) | Sin contenido | Elimina el especificado **historyItem** para esa actividad.|

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|status | status | Establecido por el servidor. Código de estado que se usa para identificar objetos válidos. Valores: activo, actualizar, eliminar, pasa por alto.|
|userTimezone | Cadena | Opcional. La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad en tiempo de creación de la actividad. Valores proporcionados como Olson identificadores con el fin de admitir la representación de multiplataforma.|
|createdDateTime | DateTimeOffset | Establecido por el servidor. Fecha y hora en UTC cuando se creó el objeto en el servidor.|
|lastModifiedDateTime | DateTimeOffset | Establecido por el servidor. Fecha y hora en UTC cuando se modificó el objeto en el servidor.|
|id | Cadena | Necesario. GUID del conjunto de clientes para el objeto **historyItem** .|
|startedDateTime | DateTimeOffset | Necesario. DateTime de UTC cuando se inició la **historyItem** (sesión de actividad). Requerida para el historial de escala de tiempo.|
|lastActiveDateTime | DateTimeOffset | Opcional. DateTime de UTC cuando la **historyItem** (sesión actividad) se entiende por última vez como estado activo o terminado - si es nulo, **historyItem** debe estar en curso.|
|expirationDateTime | DateTimeOffset | Opcional. DateTime de UTC cuando el **historyItem** experimentará eliminar disco duro. Se puede establecer por el cliente.|
|activeDurationSeconds | int | Opcional. La duración de contratación de usuario activo. Si no se proporciona, esto se calcula a partir de la **startedDateTime** y **lastActiveDateTime**.|

## <a name="relationships"></a>Relaciones

|Relación | Tipo | Description|
|:------------|:-----|:-----------|
|actividad| [userActivity](../resources/projectrome-activity.md) | Opcional. NavigationProperty/contención; propiedad de navegación a la actividad asociada.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "lastActiveDateTime",
    "activeDurationSeconds"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.activityHistoryItem",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
    "status": "active | updated | deleted | ignored",
    "createdDateTime": "DateTimeOffset",
    "lastModifiedDateTime": "DateTimeOffset",
    "id": "String",
    "expirationDateTime": "DateTimeOffset",
    "startedDateTime": "DateTimeOffset",
    "userTimezone": "String",
    "lastActiveDateTime": "DateTimeOffset",
    "activeDurationSeconds":"int"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "historyitem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
