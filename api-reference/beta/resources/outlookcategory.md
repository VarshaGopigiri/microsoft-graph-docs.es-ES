---
title: Tipo de recurso outlookCategory
description: Representa una categoría en la que un usuario puede agrupar elementos de Outlook tales como mensajes y eventos. En Outlook, el usuario define las categorías en una lista maestra y puede aplicar uno o varios de estos definidos por el usuario
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 9e4aa0c381e42522f80d933052ad7f0386643c60
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925171"
---
# <a name="outlookcategory-resource-type"></a>Tipo de recurso outlookCategory

> **Importante:** Las API de la versión de /beta en Microsoft Graph están sujetos a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una categoría en la que un usuario puede agrupar elementos de Outlook tales como mensajes y eventos. En Outlook, el usuario define las categorías en una lista maestra y puede aplicar una o varias de estas categorías definidas por el usuario a un elemento. 

Con la API de REST, puede [crear](../api/outlookuser-post-mastercategories.md) y definir categorías en la lista principal de categorías de un usuario. También puede [obtener esta lista principal de categorías](../api/outlookuser-list-mastercategories.md), [obtener una categoría específica](../api/outlookcategory-get.md), [actualizar](../api/outlookcategory-update.md) el color asociado a una categoría o [eliminar](../api/outlookcategory-delete.md) una categoría. Puede aplicar una categoría a un elemento asignando la propiedad **displayName** de la categoría a la colección **categories** del elemento.
Recursos que se pueden asignar categorías incluyen [póngase en contacto con](contact.md), [evento](event.md), [mensaje](message.md), [outlookTask](outlooktask.md)y [registrar](post.md).   

A cada categoría se le asignan atributos con dos propiedades: **displayName** y **color**. El valor de **displayName** debe ser único en la lista principal de un usuario. Pero el valor de **color** no tiene que ser único; puede asignarse el mismo color a varias categorías de la lista principal. Puede asignar hasta 25 colores distintos a las categorías de la lista principal de un usuario.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|Nombre único que identifica una categoría en el buzón del usuario. Después de crear una categoría, no puede cambiarse el nombre. Solo lectura.|
|color|String|Constante de color preestablecida que caracteriza a una categoría y a la que se asigna uno de los 25 colores predefinidos. Vea la nota siguiente. |

> **Nota** Los posibles valores de **color** son constantes preestablecidas tales como `None`, `preset0` y `preset1`. A cada constante preestablecida se le asigna asimismo un color; el color real depende del cliente de Outlook en que se muestran las categorías. La siguiente tabla muestra los colores asignados a cada constante preestablecida en Outlook (cliente de escritorio). 


| Constante preestablecida  | Color al que se asigna en Outlook |
|:---------------|:--------|
| Ninguno | Ningún color asignado |
| Preset0 | Rojo |
| Preset1 | Naranja |
| Preset2 | Marrón |
| Preset3 | Amarillo |
| Preset4 | Verde |
| Preset5 | Verde azulado |
| Preset6 | Oliva |
| Preset7 | Azul |
| Preset8 | Púrpura |
| Preset9 | Arándano |
| Preset10 | Acero |
| Preset11 | Acero oscuro |
| Preset12 | Gris |
| Preset13 | Gris oscuro |
| Preset14 | Negro |
| Preset15 | Rojo oscuro |
| Preset16 | Anaranjado oscuro |
| Preset17 | Marrón oscuro |
| Preset18 | Amarillo oscuro |
| Preset19 | Verde oscuro |
| Preset20 | Verde azulado oscuro |
| Preset21 | Oliva oscuro |
| Preset22 | Azul oscuro |
| Preset23 | Púrpura oscuro |
| Preset24 | Arándano oscuro |

## <a name="json-representation"></a>Representación JSON
Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookCategory"
}-->

```json
{
  "color": "String",
  "displayName": "String"
}

```

## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar categorías](../api/outlookuser-list-mastercategories.md) | Colección [outlookCategory](../resources/outlookcategory.md) |Obtener todas las categorías que han sido definidas por el usuario.|
|[Obtener categoría](../api/outlookcategory-get.md) | [outlookCategory](../resources/outlookcategory.md) |Obtener las propiedades y relaciones del objeto **outlookCategory** especificado.|
|[Crear](../api/outlookuser-post-mastercategories.md) | [outlookCategory](../resources/outlookcategory.md) |Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.|
|[Actualizar](../api/outlookcategory-update.md) | [outlookCategory](../resources/outlookcategory.md) |Actualizar la propiedad modificable **color** del objeto **outlookCategory** especificado. |
|[Eliminar](../api/outlookcategory-delete.md) | Ninguno |Eliminar el objeto **outlookCategory** especificado. |


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookCategory resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/beta/resources/outlookcategory.md:
      Failed to parse any rows out of table with headers: |Pre-set constant|Color mapped to in Outlook|"
  ],
  "tocPath": ""
}-->
 
