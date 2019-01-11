---
title: Tipo de recurso openTypeExtension (extensiones abiertas)
description: Extensiones Open (anteriormente conocidas como extensiones de datos de Office 365) proporcionan una forma sencilla de agregar propiedades sin tipo directamente en un recurso de Microsoft Graph.
localization_priority: Normal
ms.openlocfilehash: 4bab83766d1fc44e96043689677713cb59084f4f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870962"
---
# <a name="opentypeextension-resource-type-open-extensions"></a>Tipo de recurso openTypeExtension (extensiones abiertas)

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Extensiones Open (anteriormente conocidas como extensiones de datos de Office 365) proporcionan una forma sencilla de agregar propiedades sin tipo directamente en un recurso de Microsoft Graph.
El recurso **openTypeExtension** representa las extensiones abiertas. Las extensiones abiertas agregadas a un recurso se muestran en la propiedad de navegación **extensions**, que se deriva del tipo abstracto [extension](extension.md).  Cada extensión tiene una propiedad **extensionName** que es la única predefinida y que puede ser escrita para todas las extensiones, junto con los datos personalizados. Una forma de asegurarse de que los nombres de extensión son únicos es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`. No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.

Ejemplo de extensión abierta: [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)

Las extensiones abiertas son compatibles con los recursos siguientes en las versiones correspondientes: disponibilidad general (GA: /v1.0 y /beta) o en versión preliminar (/beta).

| Recurso | Versión |
|---------------|-------|
| [Unidad administrativa](administrativeunit.md)  | Solo versión preliminar |
| [Evento de calendario](event.md) | GA |
| [Evento de calendario](event.md) de grupo | GA |
| [Publicación](post.md) de subproceso de conversación de grupo | GA |
| [device](device.md) | GA |
| [group](group.md) | GA |
| [message](message.md) | GA |
| [organization](organization.md) | GA |
| [Contacto personal](contact.md) | GA |
| [user](user.md) | GA |

## <a name="outlook-specific-considerations"></a>Consideraciones sobre específica de Outlook

Cada extensión open presente en un recurso de Outlook (evento, mensaje o contacto personal) se almacena en una [propiedad con nombre de MAPI](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx). Al crear extensiones open para Outlook, tenga en cuenta que con el nombre de las propiedades de MAPI son un recurso finito en el buzón del usuario. Cuando se agota la cuota de la propiedad con nombre de un usuario, no se puede crear las propiedades más con nombre de dicho usuario. Esto se puede producir un comportamiento inesperado de clientes que se basan en las propiedades con nombre para la función.

Aplique las siguientes directrices al crear extensiones open en recursos de Outlook:

- Cree el número mínimo de extensiones necesarias. La mayoría de las aplicaciones deben requerir no más de una extensión. Las extensiones no tienen propiedades de conjunto definido ni estructura, por lo que puede almacenar varios valores en una única extensión.
- Evitar extensiones de nombres de una forma variable (por ejemplo, basándose en la entrada del usuario, etcetera.). Cada vez que se crea una extensión abierta con un nombre nuevo que no se ha usado en el buzón de un usuario antes, se crea un nuevo MAPI con nombre de propiedad. Quitar la extensión no quita la propiedad con nombre.

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a>Utilizar extensiones open (para recursos de Outlook) o las propiedades extendidas

Extensiones de Open es la solución recomendada para la mayoría de los escenarios que implican almacenar y obtener acceso a datos personalizados. Si, sin embargo, necesita tener acceso a datos personalizados para las propiedades de MAPI de Outlook que ya no están expuestas a través de los [metadatos de la API de Microsoft Graph](https://developer.microsoft.com/graph/docs/overview/call_api), puede usar [las propiedades extendidas y su API de REST](extended-properties-overview.md). Puede comprobar qué propiedades expone los metadatos en [ https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.opentypeextension"
}-->

```json
{
  "extensionName": "string",
  "id": "string (identifier)"
}

```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|extensionName|String|Un identificador de texto único para una extensión de datos de tipo abierto. Necesario.|
|id|String| Un identificador completo que concatena el tipo de extensión con el **extensionName**. Solo lectura.|

## <a name="relationships"></a>Relaciones

Ninguno

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Post](../api/opentypeextension-post-opentypeextension.md) | [openTypeExtension](opentypeextension.md) (en una instancia recurso existente), o un nuevo [contacto](../resources/contact.md), [evento](../resources/event.md)o [mensaje](../resources/message.md) que contiene un objeto openTypeExtension. | Cree un objeto openTypeExtension en una instancia de recursos nueva o existente.|
|[Get](../api/opentypeextension-get.md) | [openTypeExtension](opentypeextension.md) |Lea las propiedades y las relaciones del objeto openTypeExtension.|
|[Actualizar](../api/opentypeextension-update.md) | [openTypeExtension](opentypeextension.md) |Actualice el objeto openTypeExtension. |
|[Eliminar](../api/opentypeextension-delete.md) | Ninguno |Elimine el objeto openTypeExtension. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
