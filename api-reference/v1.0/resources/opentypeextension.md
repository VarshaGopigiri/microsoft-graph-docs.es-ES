# <a name="opentypeextension-resource-type-open-extensions"></a>Tipo de recurso openTypeExtension (extensiones abiertas)

Las extensiones abiertas (anteriormente conocidas como extensiones de datos de Office 365) ofrecen una manera fácil de agregar propiedades sin tipo directamente a un recurso en Microsoft Graph.

El recurso **openTypeExtension** representa las extensiones abiertas. Las extensiones abiertas agregadas a un recurso se muestran en la propiedad de navegación **extensions**, que se deriva del tipo abstracto [extension](extension.md). Cada extensión tiene una propiedad **extensionName** que es la única predefinida y que puede ser escrita para todas las extensiones, junto con los datos personalizados.

Una forma de asegurarse de que los nombres de extensión son únicos es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`. No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.

Ejemplo de extensión abierta: [Agregar datos personalizados a los usuarios mediante extensiones abiertas](../../../concepts/extensibility_open_users.md)

Las extensiones abiertas son compatibles con los recursos siguientes en las versiones correspondientes: disponibilidad general (GA: /v1.0 y /beta) o en versión preliminar (/beta).

|Recurso |Versión |
|:---------------|:-------|
| [Unidad administrativa](../../beta/resources/administrativeunit.md)  | Solo versión preliminar |
| [Evento de calendario](event.md) | GA |
| [Evento de calendario](event.md) de grupo | GA |
| [Publicación](post.md) de subproceso de conversación de grupo | GA |
| [device](device.md) | GA |
| [group](group.md) | GA |
| [message](message.md) | GA |
| [organization](organization.md) | GA |
| [Contacto personal](contact.md) | GA |
| [usuario](user.md) | GA |

## <a name="outlook-specific-considerations"></a>Consideraciones específicas sobre Outlook

Cada extensión abierta presente en un recurso de Outlook (evento, mensaje o contacto personal) se almacena en una [propiedad con nombre MAPI](https://msdn.microsoft.com/en-us/library/cc765864(v=office.15).aspx). Al crear extensiones abiertas para Outlook, tenga en cuenta que las propiedades con nombre MAPI son un recurso finito en el buzón de un usuario. Cuando se agota la cuota de propiedades con nombre de un usuario, no puede crear más propiedades con nombre para ese usuario. Esto puede resultar en un comportamiento inesperado de los clientes que dependen de las propiedades con nombre para funcionar.

Aplique las siguientes directrices al crear extensiones abiertas en los recursos de Outlook:

- Cree el número mínimo de extensiones necesarias. La mayoría de las aplicaciones no requieren más de una extensión. Las extensiones no tienen una estructura o propiedades definidas, por lo que puede almacenar varios valores en una sola extensión.
- Evite nombrar las extensiones de una manera variable (como por ejemplo, basado en la entrada del usuario, etc.). Cada vez que se crea una extensión abierta con un nuevo nombre que no se ha utilizado antes en el buzón de un usuario, se crea una nueva propiedad con nombre MAPI. Quitar la extensión no elimina la propiedad con nombre.

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a>¿Se deben utilizar extensiones abiertas (para recursos de Outlook) o propiedades extendidas?

Las extensiones abiertas son la solución recomendada para la mayoría de los escenarios que implican el almacenamiento y el acceso a datos personalizados. Sin embargo, si necesita acceder a datos personalizados para las propiedades MAPI de Outlook que aún no están expuestas a través de los [metadatos de la API de Microsoft Graph](http://developer.microsoft.com/en-us/graph/docs/overview/call_api), puede usar las [propiedades extendidas y su API de REST](extended-properties-overview.md). Puede verificar qué propiedades expone el metadato en [https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "baseType": "microsoft.graph.extension",
  "@odata.type": "microsoft.graph.openTypeExtension"
}-->

```json
{
  "extensionName": "string",
  "id": "string (identifier)"
}

```

## <a name="properties"></a>Propiedades

|Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|extensionName|Cadena|Un identificador de texto único para una extensión abierta de tipo abierto. Necesario.|
|id|Cadena| Un identificador completo que concatena el tipo de extensión con el **extensionName**. Solo lectura.|

## <a name="relationships"></a>Relaciones

Ninguna

## <a name="methods"></a>Métodos

|Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Post](../api/opentypeextension_post_opentypeextension.md) | [openTypeExtension](opentypeextension.md) (en una instancia de recurso existente) o un [contacto](../resources/contact.md), [evento](../resources/event.md) o [mensaje](../resources/message.md) nuevo que contenga un objeto openTypeExtension. | Cree un objeto openTypeExtension en una instancia de recursos nueva o existente.|
|[Get](../api/opentypeextension_get.md) | [openTypeExtension](opentypeextension.md) |Lea las propiedades y las relaciones del objeto openTypeExtension.|
|[Actualizar](../api/opentypeextension_update.md) | [openTypeExtension](opentypeextension.md) |Actualice el objeto openTypeExtension. |
|[Eliminar](../api/opentypeextension_delete.md) | Ninguno |Elimine el objeto openTypeExtension. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
