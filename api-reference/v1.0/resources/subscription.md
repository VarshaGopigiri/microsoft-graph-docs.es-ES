# <a name="subscription-resource-type"></a>Tipo de recurso Subscription
Una suscripción permite que una aplicación cliente reciba notificaciones sobre los datos de Microsoft Graph. Actualmente las suscripciones están habilitadas para los conjuntos de datos siguientes:

1. Correo, eventos y contactos de Outlook
1. Conversaciones de los grupos de Office.
1. Elementos raíz de la unidad de OneDrive 


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.subscription"
}-->

```json
{
  "changeType": "string",
  "notificationUrl": "string",
  "resource": "string",
  "expirationDateTime": "string (timestamp)",
  "id": "string (identifier)",
  "clientState": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|changeType|string|Indica el tipo de cambio en el recurso suscrito que generará una notificación. Los valores admitidos son: `created`, `updated`, `deleted`. Se pueden combinar varios valores mediante una lista separada por comas.|
|notificationUrl|string|La dirección URL del extremo que recibirá las notificaciones. Esta dirección URL tiene que usar el protocolo HTTPS.|
|recurso|string|Especifica el recurso al que se le supervisarán los cambios. No incluya la dirección URL base ("https://graph.microsoft.com/v1.0/").|
|expirationDateTime|[dateTime](http://tools.ietf.org/html/rfc3339)|Especifica la fecha y hora en que expira la suscripción de webhook. La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.  Consulte la tabla siguiente para la duración máxima de la suscripción compatible. |
|clientState|string|Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación. Se permite una longitud máxima de 128 caracteres. El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación.|
|identificador|string|Identificador único de la suscripción. Solo lectura.|

## <a name="maximum-length-of-subscription-per-resource-type"></a>Duración máxima de la suscripción por tipo de recurso
| Recurso | Tiempo de expiración máximo |
|:---------------------|:--------------------|
|Correo| 4230 minutos.|
|Calendario| 4230 minutos.|
|Contactos| 4230 minutos.|
|Conversaciones de grupo| 4230 minutos.|
|Elementos raíz de la unidad| 43 200 minutos. Las nuevas aplicaciones y las aplicaciones existentes no deben superar el valor admitido. En las próximas versiones no se permitirán valores superiores. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear suscripción](../api/subscription_post_subscriptions.md) | [subscription](subscription.md) |Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph.|
|[Actualizar suscripción](../api/subscription_update.md) | [subscription](subscription.md) |Renueva una suscripción al actualizar su tiempo de expiración.|
|[Obtener suscripción](../api/subscription_get.md) | [subscription](subscription.md) |Lee las propiedades y relaciones del objeto subscription.|
|[Eliminar suscripción](../api/subscription_delete.md) | Ninguno |Elimina un objeto subscription.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
