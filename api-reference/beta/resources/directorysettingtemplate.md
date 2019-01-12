---
title: tipo de recurso directorySettingTemplate
description: Plantillas de configuración de Active Directory representan definidas por el sistema de configuración disponible para el inquilino. Configuración de Active Directory se puede crear en función de la directorySettingTemplates disponibles y los valores que ha cambiado desde sus valores predeterminados. Plantillas de configuración de Active Directory no se crea, actualiza o elimina. Esta configuración puede representan la configuración de todo el inquilino, o puede representan la configuración de la entidad específica.  Actualmente, las plantillas sólo disponibles se aplican a los grupos de Office e incluyen opciones de configuración, como si los usuarios pueden crear grupos o invitar a personas de fuera de la organización para convertirse en miembros de un grupo.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d950b94c71bae70474bf9cdb9eee76fb8a3d9134
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957637"
---
# <a name="directorysettingtemplate-resource-type"></a>tipo de recurso directorySettingTemplate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Plantillas de configuración de Active Directory representan definidas por el sistema de configuración disponible para el inquilino. [Configuración de Active Directory](directorysetting.md) se pueden crear en función de la directorySettingTemplates disponibles y los valores que ha cambiado desde sus valores predeterminados. Plantillas de configuración de Active Directory no se crea, actualiza o elimina. Esta configuración puede representan la configuración de todo el inquilino, o puede representan la configuración de la entidad específica.  Actualmente, las plantillas sólo disponibles se aplican a los grupos de Office e incluyen opciones de configuración, como si los usuarios pueden crear grupos o invitar a personas de fuera de la organización para convertirse en miembros de un grupo.

> **Nota**: la versión de /beta del tipo de recurso directorySettingTemplate sólo se aplica a los grupos. Se ha cambiado la versión de /v1.0 a groupSettingTemplate.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener directorySettingTemplate](../api/directorysettingtemplate-get.md) | [directorySettingTemplate](directorysettingtemplate.md) |Lea las propiedades específicas de uno de los objetos de directorySettingTemplate definida por el sistema.|
|[Lista directorySettingTemplate](../api/directorysettingtemplate-list.md) | [Colección de directorySettingTemplate](directorysettingtemplate.md) |Lista de todos los objetos de directorySettingTemplate definida por el sistema.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|string|Descripción de la plantilla. Solo lectura.|
|displayName|string|Muestra el nombre de la plantilla. Solo lectura. |
|id|string| Identificador único de la plantilla. Solo lectura.|
|values|Colección de [settingTemplateValue](settingtemplatevalue.md)| Colección de settingTemplateValues que enumera el conjunto de opciones disponibles, los valores predeterminados y los tipos que forman esta plantilla.  Solo lectura. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directorySettingTemplate"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "values": [{"@odata.type": "microsoft.graph.settingTemplateValue"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directorySettingTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
