# <a name="subscription-resource-type"></a>Tipo de recurso subscription

Una suscripción permite que una aplicación cliente reciba notificaciones sobre cambios en datos de Microsoft Graph. Actualmente, las suscripciones están habilitadas para los siguientes recursos:

- Correo, eventos y contactos de Outlook
- Conversaciones de los grupos de Office
- Elementos raíz de la unidad de OneDrive
- Usuarios y grupos de Azure Active Directory

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
| changeType | cadena | Obligatorio. Indica el tipo de cambio en el recurso suscrito que generará una notificación. Los valores admitidos son: `created`, `updated`, `deleted`. Se pueden combinar varios valores mediante una lista separada por comas.<br><br>Nota: Las notificaciones de elemento de raíz de unidad solo son compatibles con `updated` changeType. Las notificaciones de usuario y de grupo admiten `updated` y `deleted` changeType.|
| notificationUrl | cadena | Obligatorio. La dirección URL del extremo que va a recibir las notificaciones. Esta dirección URL debe hacer uso del protocolo HTTPS. |
| resource | cadena | Obligatorio. Especifica el recurso del que se supervisarán los cambios. No incluya la dirección URL base (`https://graph.microsoft.com/v1.0/`). |
| expirationDateTime | [dateTime](http://tools.ietf.org/html/rfc3339) | Obligatorio. Especifica la fecha y hora en que expira la suscripción de webhook. La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.  Consulte la tabla siguiente para la duración máxima de la suscripción compatible. |
| clientState | cadena | Opcional. Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación. Se permite una longitud máxima de 128 caracteres. El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación. |
| identificador | cadena | Identificador único de la suscripción. Solo lectura. |
| applicationId | cadena | Identificador de la aplicación utilizada para crear la suscripción. Solo lectura. |
| creatorId | cadena | Identificador del usuario o de la entidad de seguridad de servicio que creó la suscripción. Si la aplicación usada ha delegado permisos para crear la suscripción, este campo contiene el identificador del usuario que ha iniciado sesión en cuyo nombre llama la aplicación. Si la aplicación usa los permisos de aplicación, este campo contiene el identificador de la entidad de seguridad de servicio correspondiente a la aplicación. Solo lectura. |

## <a name="maximum-length-of-subscription-per-resource-type"></a>Duración máxima de la suscripción por tipo de recurso

| Recurso            | Tiempo de expiración máximo  |
|:--------------------|:-------------------------|
| Correo                | 4320 minutos (3 días)    |
| Calendario            | 4320 minutos (3 días)    |
| Contactos            | 4320 minutos (3 días)    |
| Conversaciones de grupo | 4320 minutos (3 días)    |
| Elementos raíz de la unidad    | 4320 minutos (3 días) |

> **Nota:** Las nuevas aplicaciones y las aplicaciones existentes no deben superar el valor admitido. En el futuro, se producirá un error en las solicitudes para crear o renovar una suscripción más allá del valor máximo.

## <a name="relationships"></a>Relaciones

Ninguna

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-------|:------------|:------------|
| [Crear suscripción](../api/subscription_post_subscriptions.md) | [subscription](subscription.md) | Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph. |
| [Actualizar suscripción](../api/subscription_update.md) | [subscription](subscription.md) | Renueva una suscripción al actualizar su tiempo de expiración. |
| [Listar subscripciones](../api/subscription_list.md) | [subscription](subscription.md) | Listas de suscripciones activas. |
| [Obtener suscripción](../api/subscription_get.md) | [subscription](subscription.md) | Lee las propiedades y relaciones del objeto subscription. |
| [Eliminar suscripción](../api/subscription_delete.md) | Ninguno |Elimina un objeto subscription. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
