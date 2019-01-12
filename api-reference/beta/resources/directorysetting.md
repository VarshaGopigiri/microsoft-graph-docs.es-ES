---
title: Establecer el tipo de recurso
description: Configuración del directorio puede crear en función de la directorySettingTemplates disponibles y se ha cambiado desde sus valores predeterminados. Esta configuración puede controlar comportamientos de entidad o una característica, en un nivel de todo el inquilino o en un nivel de la entidad específica. Cuando la misma configuración se define en el nivel de entidad todo el inquilino y específica, la configuración del nivel de entidad específica puede voluntaria de la configuración de todo el inquilino.  Por ejemplo, la configuración de todo el inquilino puede permitir que los invitados puedan ser invitados por los miembros de grupos existentes, pero una configuración de grupo específico puede voluntaria y no permitir que los invitados puedan ser invitados por los miembros del grupo. Actualmente configuraciones de definidas por el sistema sólo se rigen el comportamiento de los grupos de Office.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: fbe1879a22b2dc7e69258d34f7e25c37bfd0cd5a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990554"
---
# <a name="directorysetting-resource-type"></a>Establecer el tipo de recurso

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Configuración del directorio puede crear en función de la disponible [directorySettingTemplates](directorysettingtemplate.md)y se ha cambiado desde sus valores predeterminados. Esta configuración puede controlar comportamientos de entidad o una característica, en un nivel de todo el inquilino o en un nivel de la entidad específica. Cuando la misma configuración se define en el nivel de entidad todo el inquilino y específica, la configuración del nivel de entidad específica puede voluntaria de la configuración de todo el inquilino.  Por ejemplo, la configuración de todo el inquilino puede permitir que los invitados puedan ser invitados por los miembros de grupos existentes, pero una configuración de grupo específico puede voluntaria y no permitir que los invitados puedan ser invitados por los miembros del grupo. Actualmente configuraciones de definidas por el sistema sólo se rigen el comportamiento de los grupos de Office.

> **Nota**: la versión de /beta del tipo de recurso establecer solo se aplica a los grupos. Se ha cambiado la versión de /v1.0 a groupSetting.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Create setting](../api/directorysetting-post-settings.md) | [Establecer](directorysetting.md) |Crear un objeto de configuración basado en un directorySettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración definida en la plantilla.|
|[Get setting](../api/directorysetting-get.md) | [Establecer](directorysetting.md) |Lee las propiedades de un objeto de configuración específico.|
|[List settings](../api/directorysetting-list.md) | colección de [establecer](directorysetting.md) |Enumera las propiedades de todos los objetos de configuración.|
|[Configuración de actualización](../api/directorysetting-update.md) | [Establecer](directorysetting.md)  |Actualiza el objeto de configuración. SettingValues sólo se puede cambiar en una actualización.|
|[Delete setting](../api/directorysetting-delete.md) | Ninguno |Elimina un objeto de configuración. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|string|El nombre para mostrar de este grupo de configuraciones, que proviene de la plantilla asociada. Solo lectura.|
|id|string| Identificador único de esta configuración. Solo lectura.|
|templateId|string| Identificador único para la plantilla que se usa para crear este grupo de configuraciones. Solo lectura.|
|values|Colección de [settingValue](settingvalue.md)| Colección de pares de nombre y valor. Debe contener y establecer todas las configuraciones definidas en la plantilla.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directorySetting"
}-->

```json
{
  "displayName": "string",
  "id": "string (identifier)",
  "templateId": "string",
  "values": [{"@odata.type": "microsoft.graph.settingValue"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directorySetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
