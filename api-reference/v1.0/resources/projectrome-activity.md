---
title: tipo de recurso de actividad
description: Representa una sola actividad dentro de una aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un elemento de historial que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.
localization_priority: Normal
ms.openlocfilehash: 79ed44ef0f6a38fbef8ead233debce3fc9e66b42
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877073"
---
# <a name="activity-resource-type"></a>tipo de recurso de actividad

Representa una sola actividad dentro de una aplicación - por ejemplo, un programa de TV, un documento o una campaña actual en un juego de vídeo. Cuando un usuario se activa con esa actividad, la contratación se captura como un [elemento de historial](projectrome-historyitem.md) que indica la hora de inicio y finalización para esa actividad. Como el usuario volver a contrata con esa actividad a través del tiempo, se registran varios elementos de historial para una actividad de usuario único.

Puede usar las actividades en Microsoft Graph para que los usuarios puedan volver a lo que estaba haciendo en su aplicación en varios dispositivos. Las actividades que crea la aplicación aparecen en los dispositivos de todos los usuarios y se exponen a los usuarios como profundo vínculos a contenido específico dentro de la aplicación. Puede expresar contenido específico dentro de la aplicación como un destino que se mostrarán en Windows y accesibles en iOS y Android dispositivos a través de notificaciones de Cortana.

Debido a que cada aplicación es diferente, es copia de seguridad a comprender la mejor forma de asignar acciones dentro de la aplicación a las actividades del usuario que va a aparecer en Cortana y escala de tiempo. Por ejemplo, juegos podrían crear una actividad para cada campaña, aplicaciones de creación de documento es posible que crear una actividad para cada documento único y aplicaciones de línea de negocio podrían crear una actividad para cada flujo de trabajo.

Las actividades del usuario se mostrarán en experiencias de usuario Cortana y escala de tiempo de Windows, que se centran en aumentar la productividad y la eficacia de los usuarios al ayudarles a ponerse en contacto con el contenido que ha funcionado en el pasado.

## <a name="methods"></a>Métodos

|Método | Tipo de valor devuelto | Descripción|
|:------|:------------|:-----------|
|[Crear o reemplazar la actividad](../api/projectrome-put-activity.md) | [activity](projectrome-activity.md) |Crea o reemplaza una actividad existente (upsert). El appActivityId debe estar seguras de dirección URL (todos los caracteres excepto deben convertirse en su representación hexadecimal caracteres no reservados de RFC 2396), pero el appActivityId original no tiene que estar seguro de la dirección URL. |
|[Eliminar una actividad](../api/projectrome-delete-activity.md) | Sin contenido | Elimina la actividad para que el usuario especificada de la aplicación.|
|[Obtener las actividades](../api/projectrome-get-activities.md) | Colección de [actividades](projectrome-activity.md) | Obtiene las actividades de la aplicación para un usuario determinado.|
|[Obtener actividades recientes](../api/projectrome-get-recent-activities.md) | Colección de [actividades](projectrome-activity.md) | Obtiene las actividades más recientes de la aplicación para un usuario determinado, ordenar y según la más recientemente creado o actualizado [historyItems](projectrome-historyitem.md).|

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Description|
|:----|:-----|:-----------|
|userTimezone | Cadena | Opcional. La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad en tiempo de creación de la actividad; valores proporcionados como Olson identificadores con el fin de admitir la representación de multiplataforma.|
|createdDateTime | DateTimeOffset | Establecido por el servidor. Fecha y hora en UTC cuando se creó el objeto en el servidor. |
|lastModifiedDateTime | DateTimeOffset | Establecido por el servidor. Fecha y hora en UTC cuando se modificó el objeto en el servidor. |
|id | Cadena | Identificador generado por el servidor usado para direcciones URL.|
|appActivityId | Cadena | Necesario. El identificador de actividad único en el contexto de la aplicación - suministrada por el autor de la llamada e inmutable a partir de entonces.|
|activitySourceHost | Cadena | Necesario. Dirección URL para el dominio que representa la asignación de identidad de multiplataforma para la aplicación. La asignación es configurable a través del centro de desarrollo de Windows o bien almacenado como un archivo JSON hospedado en el dominio. El archivo JSON se denomina entre-plataforma-aplicación-identificadores y se hospeda en la raíz de su dominio HTTPS, ya sea en el dominio de nivel superior o incluir un dominio sub. Por ejemplo: https://contoso.com o https://myapp.contoso.com, pero NO https://myapp.contoso.com/somepath. Debe tener un archivo único y el dominio (o dominio sub) por identidad de aplicación multiplataforma. Por ejemplo, un archivo independiente y un dominio se necesita para Word y PowerPoint.|
|appDisplayName | Cadena | Opcional. Descripción de texto breve de la aplicación que se usa para generar la actividad para su uso en los casos, cuando la aplicación no está instalada en el dispositivo del usuario local.|
|activationUrl | Cadena | Necesario. Dirección URL utilizada para iniciar la actividad en la mejor experiencia nativa representada por el identificador de aplicación. Es posible que se inicie una aplicación basada en web si no existe ninguna aplicación nativa.|
|fallbackUrl | Cadena | Opcional. Dirección URL utilizada para iniciar la actividad en una aplicación basada en web, si está disponible.|
|contentUrl | Cadena | Opcional. Se usa en el caso de que el contenido se puede representar fuera de una experiencia de la aplicación nativa o basada en web (por ejemplo, un puntero a un elemento en una fuente RSS).|
|visualElements| [visualInfo](../resources/projectrome-visualinfo.md) | Necesario. El objeto que contiene información para representar la actividad en la UX.|
|contentInfo | Objeto JSON sin tipo | Opcional. Un fragmento personalizado de datos - descripción extensible JSON-larga distancia de contenido de acuerdo con la sintaxis [schema.org](https://schema.org) .|
|expirationDateTime | DateTimeOffset | Establecido por el servidor. Fecha y hora en UTC cuando el objeto caducado en el servidor.|
|status | status | Establecido por el servidor. Código de estado que se usa para identificar objetos válidos. Valores: activo, actualizar, eliminar, pasa por alto.|

## <a name="relationships"></a>Relaciones

|Relación | Tipo | Description|
|:------------|:-----|:-----------|
|historyItems| colección de [activityHistoryItem](../resources/projectrome-historyitem.md) | Opcional. NavigationProperty/contención; propiedad de navegación para historyItems de la actividad.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "appDisplayName",
    "fallbackUrl",
    "contentUrl",
    "contentInfo",
    "visualElements",
    "historyItems"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.userActivity",
  "@odata.annotations": [
    {
      "capabilities": {
        "countable": false,
        "selectable": false,
        "skippable": false
      }
    }
  ]
}-->

```json
{
    "appActivityId": "String",
    "activitySourceHost": "String (host name/domain/URL)",
    "userTimezone": "String",
    "appDisplayName": "String",
    "activationUrl": "String (URL)",
    "contentUrl": "String (URL)",
    "fallbackUrl": "String (URL)",
    "createdDateTime": "DateTimeOffset",
    "lastModifiedDateTime": "DateTimeOffset",
    "expirationDateTime": "DateTimeOffset",
    "id": "String",
    "status": "active | updated | deleted | ignored",
    "contentInfo": { "@odata.type": "microsoft.graph.Json" },
    "visualElements": { "@odata.type": "microsoft.graph.visualInfo" },
    "historyItems": [{ "@odata.type": "microsoft.graph.activityHistoryItem" }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "activity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
