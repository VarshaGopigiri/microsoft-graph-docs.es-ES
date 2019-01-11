---
title: tipo de recurso synchronizationTemplate
description: " cualquier usuario puede recuperar la plantilla para ver la configuración predeterminada, incluido el esquema de sincronización."
localization_priority: Normal
ms.openlocfilehash: e98d3fa16d0a80ac9353aaa75200d8cb24d3e904
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833078"
---
# <a name="synchronizationtemplate-resource-type"></a>tipo de recurso synchronizationTemplate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Proporciona opciones de configuración de sincronización preconfigurado para una aplicación concreta. Estas opciones de configuración se usará de forma predeterminada para cualquier [trabajo de sincronización](synchronization-synchronizationjob.md) que se basa en la plantilla. El desarrollador de la aplicación especifica la plantilla; cualquier usuario puede recuperar la plantilla para ver la configuración predeterminada, incluido el [esquema de sincronización](synchronization-synchronizationschema.md).

Puede proporcionar varias plantillas de una aplicación y designar una plantilla predeterminada. Si varias plantillas están disponibles para la aplicación que le interesa, seek instrucciones específicas de la aplicación para determinar qué una mejor adapte a sus necesidades.

## <a name="methods"></a>Métodos

| Método        | Tipo de valor devuelto               | Descripción                  |
|:--------------|:--------------------------|:-----------------------------|
|[List](../api/synchronization-synchronizationtemplate-list.md)    |colección de [synchronizationTemplate](synchronization-synchronizationtemplate.md)  |Lista de las plantillas que están disponibles para una aplicación o una instancia de la aplicación (entidad de seguridad de servicio).|
|[Get](../api/synchronization-synchronizationtemplate-get.md)      |[synchronizationTemplate](synchronization-synchronizationtemplate.md)   |Lea las propiedades y relaciones del objeto **synchronizationTemplate** .|
<!-- 
|[Create](../api/synchronization-synchronizationtemplate-post.md) |[synchronizationTemplate](synchronization-synchronizationtemplate.md)   |Create a new template for an application.|
|[Update](../api/synchronization-synchronizationtemplate-put.md)   |[synchronizationTemplate](synchronization-synchronizationtemplate.md)   |Update the template.| 
-->

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo                      | Descripción                  |
|:--------------|:--------------------------|:-----------------------------|
|id             |Cadena                     |Identificador de plantilla único.|
|applicationId  |cadena                     |Identificador de la aplicación al que pertenece esta plantilla.|
|Es el valor predeterminado.        |Booleano                    |`true`Si esta plantilla se recomienda que tenga el valor predeterminado de la aplicación.|
|descripción    |String                     |Descripción de la plantilla.|
|que se pueda detectar   |Cadena                     |`true`Si esta plantilla debe aparecer en la colección de plantillas disponibles para la instancia de aplicación (entidad de seguridad de servicio).|
|factoryTag     |Cadena                     |Una de las etiquetas de fábrica Well-known compatibles con el motor de sincronización. La **factoryTag** indica que el motor de sincronización a qué implementación a utilizar al procesamiento de trabajos basados en esta plantilla.|
|metadatos       |colección de metadataEntry   |Propiedades de extensión adicionales. A menos que se mencionan explícitamente, no se deben cambiar los valores de metadatos.|

## <a name="relationships"></a>Relaciones
| Relación      | Tipo      |Description|
|:------------------|:----------|:----------|
|esquema             |[synchronizationSchema](synchronization-synchronizationschema.md)     |Esquema de sincronización predeterminado para las tareas basadas en esta plantilla.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationTemplate"
}-->

```json
{
  "applicationId": "String (identifier)",
  "default": true,
  "description": "String",
  "discoverable": true,
  "factoryTag": "String",
  "id": "String (identifier)",
  "metadata": [{"@odata.type": "microsoft.graph.metadataEntry"}],
  "schema": {"@odata.type": "microsoft.graph.synchronizationSchema"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
