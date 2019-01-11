---
title: tipo de recurso de suscripción
description: 'Una suscripción a permite que una aplicación de cliente recibir notificaciones sobre cambios en los datos en Microsoft Graph. Actualmente, las suscripciones están habilitadas para los siguientes recursos:'
localization_priority: Priority
ms.openlocfilehash: b70daca8eb0f7c303173945b3cacf2cf53af56ec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867014"
---
# <a name="subscription-resource-type"></a>tipo de recurso de suscripción

Una suscripción a permite que una aplicación de cliente recibir notificaciones sobre cambios en los datos en Microsoft Graph. Actualmente, las suscripciones están habilitadas para los siguientes recursos:

- Correo, eventos y los contactos de Outlook.
- Conversaciones de los grupos de Office.
- Los elementos raíz de unidad de OneDrive.
- Los usuarios y grupos de Azure Active Directory.
- Alertas de la API de seguridad de Microsoft Graph.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.subscription",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "toppable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false,
        "sortable": false
      }
    }
  ]
}-->

```json
{
  "changeType": "string",
  "notificationUrl": "string",
  "resource": "string",
  "applicationId" : "string",
  "expirationDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "clientState": "string",
  "creatorId": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
| changeType | string | Necesario. Indica el tipo de cambio en el recurso suscrito que generará una notificación. Los valores admitidos son: `created`, `updated`, `deleted`. Se pueden combinar varios valores mediante una lista separada por comas.<br><br>Nota: Las notificaciones de elemento de raíz de unidad sólo son compatibles con el `updated` changeType. Admiten notificaciones de usuario y de grupo `updated` y `deleted` changeType.|
| notificationUrl | string | Necesario. La dirección URL del extremo que va a recibir las notificaciones. Esta dirección URL debe hacer uso de la HTTPS protocolo. |
| resource | string | Necesario. Especifica el recurso al que se van a supervisar para que los cambios. No incluya la dirección URL base (`https://graph.microsoft.com/v1.0/`). |
| expirationDateTime | [dateTime](https://tools.ietf.org/html/rfc3339) | Necesario. Especifica la fecha y hora en que expira la suscripción de webhook. La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.  Consulte la tabla siguiente para la duración máxima de la suscripción compatible. |
| clientState | string | Opcional. Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación. Se permite una longitud máxima de 128 caracteres. El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación. |
| identificador | string | Identificador único de la suscripción. Solo lectura. |
| applicationId | string | Identificador de la aplicación utilizada para crear la suscripción. Solo lectura. |
| Creador de | string | Identificador del usuario o de la entidad de seguridad de servicio que creó la suscripción. Si la aplicación usada delegado permisos para crear la suscripción, este campo contiene el identificador del usuario ha iniciado sesión de que la aplicación llama en nombre. Si la aplicación usa los permisos de aplicación, este campo contiene el identificador de la entidad de seguridad de servicio correspondiente a la aplicación. Solo lectura. |

## <a name="maximum-length-of-subscription-per-resource-type"></a>Duración máxima de la suscripción por tipo de recurso

| Recurso            | Tiempo de expiración máximo  |
|:--------------------|:-------------------------|
| Correo                | 4230 minutos (en 3 días)    |
| Calendario            | 4230 minutos (en 3 días)    |
| Contactos            | 4230 minutos (en 3 días)    |
| Conversaciones de grupo | 4230 minutos (en 3 días)    |
| Elementos raíz de la unidad    | 4230 minutos (en 3 días)    |
| Alertas de seguridad     | 43200 minutos (en 30 días)  |

> **Nota:** Las aplicaciones existentes y nuevas aplicaciones no deben superar el valor admitido. En el futuro, se producirá un error en las solicitudes para crear o renovar una suscripción más allá del valor máximo.

## <a name="relationships"></a>Relaciones

Ninguno

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-------|:------------|:------------|
| [Crear suscripción](../api/subscription-post-subscriptions.md) | [subscription](subscription.md) | Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph. |
| [Actualizar suscripción](../api/subscription-update.md) | [subscription](subscription.md) | Renueva una suscripción al actualizar su tiempo de expiración. |
| [Suscripciones de lista](../api/subscription-list.md) | [subscription](subscription.md) | Listas de suscripciones activas. |
| [Obtener suscripción](../api/subscription-get.md) | [subscription](subscription.md) | Lee las propiedades y relaciones del objeto subscription. |
| [Eliminar suscripción](../api/subscription-delete.md) | Ninguno |Elimina un objeto subscription. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
