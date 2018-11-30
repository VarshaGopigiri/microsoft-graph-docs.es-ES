---
title: tipo de recurso synchronizationJob
description: Realiza la sincronización por sondeo para que los cambios en un directorio y la inserción de ellos en otro directorio, periódicamente que se ejecuta en segundo plano. El trabajo de sincronización siempre es específico de una instancia determinada de una aplicación en el inquilino. Como parte de la configuración del trabajo de sincronización, debe conceder autorización para leer y escribir objetos en el directorio de destino y personalizar el esquema de sincronización de la tarea.
ms.openlocfilehash: 0e6428f2a088e5326f4412e743489c4d94b10296
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090579"
---
# <a name="synchronizationjob-resource-type"></a>tipo de recurso synchronizationJob

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Realiza la sincronización por sondeo para que los cambios en un directorio y la inserción de ellos en otro directorio, periódicamente que se ejecuta en segundo plano. El trabajo de sincronización siempre es específico de una instancia determinada de una aplicación en el inquilino. Como parte de la configuración del trabajo de sincronización, debe conceder autorización para leer y escribir objetos en el directorio de destino y personalizar el esquema de sincronización de la tarea.

## <a name="methods"></a>Métodos

| Método        | Tipo de valor devuelto               | Descripción                  |
|:--------------|:--------------------------|:-----------------------------|
|[List](../api/synchronization-synchronizationjob-list.md)             |colección de [synchronizationJob](synchronization-synchronizationjob.md)  |Lista de trabajos existentes para una instancia de aplicación determinada (entidad de seguridad de servicio).|
|[Obtener synchronizationJob](../api/synchronization-synchronizationjob-get.md) | [synchronizationJob](synchronization-synchronizationjob.md) |Leer las propiedades y relaciones de un objeto synchronizationJob.|
|[Create](../api/synchronization-synchronizationjob-post.md)         |[synchronizationJob](synchronization-synchronizationjob.md)   |Crear nuevo trabajo de una aplicación determinada.|
|[Start](../api/synchronization-synchronizationjob-start.md)          |Ninguno   |Iniciar la sincronización. Si el trabajo está en un estado en pausa, continúa desde el punto donde se ha pausado el trabajo. Si el trabajo está en cuarentena, se borra el estado de la cuarentena.|
|[Restart](../api/synchronization-synchronizationjob-restart.md)      |Ninguno   |Forzar el trabajo para empezar de nuevo y volver a procesar todos los objetos en el directorio.|
|[Pause](../api/synchronization-synchronizationjob-pause.md)          |Ninguno   |Detener temporalmente la sincronización. Se conserva el progreso, incluido el estado de trabajo, y el trabajo continuará desde donde la dejó cuando se realiza una llamada de [Inicio](../api/synchronization-synchronizationjob-start.md) .|
|[Delete](../api/synchronization-synchronizationjob-delete.md)        |Ninguno   |Detener la sincronización y eliminar de forma permanente todos los el estado asociado con el trabajo.|
|[Obtener synchrnoizationSchema](../api/synchronization-synchronizationschema-get.md)    |[synchronizationSchema](synchronization-synchronizationschema.md)   |Recuperar el esquema de sincronización eficaz del trabajo.|
|[Actualizar synchroizationSchema](../api/synchronization-synchronizationschema-update.md)    |Ninguno   |Actualizar el esquema de sincronización de la tarea. |
|[Validar credenciales](../api/synchronization-synchronizationjob-validatecredentials.md)|Ninguno|Pruebe las credenciales proporcionadas en el directorio de destino.|

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo      | Descripción    |
|:--------------|:----------|:---------------|
|id             |String                     |Identificador de trabajo de sincronización únicas. Solo lectura.|
|programación       |[synchronizationSchedule](synchronization-synchronizationschedule.md)|Programación que se usa para ejecutar el trabajo. Solo lectura.|
|status         |[synchronizationStatus](synchronization-synchronizationstatus.md)     |Estado del trabajo, que incluye cuando se ejecutó el trabajo por última vez, el estado actual del trabajo y los errores.|
|templateId     |String    |Identificador de la [plantilla de sincronización](synchronization-synchronizationtemplate.md) de en que este trabajo se basa.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|esquema|[synchronizationSchema](synchronization-synchronizationschema.md)| El esquema de sincronización configurado para el trabajo.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationJob"
}-->

```json
{
  "id": "String (identifier)",
  "schedule": {"@odata.type": "microsoft.graph.synchronizationSchedule"},
  "status": {"@odata.type": "microsoft.graph.synchronizationStatus"},
  "templateId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationJob resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->