---
title: Tipo de recurso outlookUser
description: Representa los servicios de Outlook disponibles para un usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: bf772eb1598b38550797458df955495dafdd4282
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943602"
---
# <a name="outlookuser-resource-type"></a>Tipo de recurso outlookUser

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los servicios de Outlook disponibles para un usuario.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear categoría](../api/outlookuser-post-mastercategories.md) | [outlookCategory](outlookcategory.md) |Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.|
|[Enumerar categorías](../api/outlookuser-list-mastercategories.md) | Colección [outlookCategory](outlookcategory.md) |Obtener todas las categorías que han sido definidas por el usuario.|
|[Crear outlookTaskFolder](../api/outlookuser-post-taskfolders.md) |[outlookTaskFolder](outlooktaskfolder.md)| Cree una carpeta de tarea en el grupo de tarea predeterminado (`My Tasks`) del buzón de usuario.|
|[Lista taskFolders](../api/outlookuser-list-taskfolders.md) |colección de [outlookTaskFolder](outlooktaskfolder.md)| Obtenga todas las carpetas de tareas de Outlook en el buzón del usuario.|
|[Crear outlookTaskGroup](../api/outlookuser-post-taskgroups.md) |[outlookTaskGroup](outlooktaskgroup.md)| Cree un grupo de tareas de Outlook en el buzón del usuario.|
|[Lista taskGroups](../api/outlookuser-list-taskgroups.md) |colección de [outlookTaskGroup](outlooktaskgroup.md)| Obtener todos los grupos de tareas de Outlook en el buzón del usuario.|
|[Crear outlookTask](../api/outlookuser-post-tasks.md) |[outlookTask](outlooktask.md)| Crear una tarea de Outlook en el grupo de tarea predeterminado (`My Tasks`) y la carpeta de tareas predeterminada (`Tasks`) en el buzón del usuario.|
|[Enumerar tareas](../api/outlookuser-list-tasks.md) |colección de [outlookTask](outlooktask.md)| Obtenga todas las tareas de Outlook en el buzón del usuario.|
|[supportedLanguages](../api/outlookuser-supportedlanguages.md) | Colección [localeInfo](localeinfo.md) | Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario. |
|[supportedTimeZones](../api/outlookuser-supportedtimezones.md) | Colección [timeZoneInformation](timezoneinformation.md) | Obtener una lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario. |


## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|masterCategories|Colección [outlookCategory](../resources/outlookcategory.md)| Lista de categorías definidas para el usuario. | 
|taskFolders|colección de [outlookTaskFolder](outlooktaskfolder.md)| Carpetas de tareas de Outlook del usuario. Solo lectura. Admite valores NULL.|
|taskGroups|colección de [outlookTaskGroup](outlooktaskgroup.md)| Grupos de tareas de Outlook del usuario. Solo lectura. Admite valores NULL.|
|tasks|colección de [outlookTask](outlooktask.md)| Tareas de Outlook del usuario. Solo lectura. Admite valores NULL.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
