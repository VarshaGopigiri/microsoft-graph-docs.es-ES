---
title: Tipo de recurso auditEvent
description: Una clase que contiene las propiedades del evento de auditoría.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e39d6fb744ee1af2289efec8a7dec722672029d3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864123"
---
# <a name="auditevent-resource-type"></a>Tipo de recurso auditEvent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades del evento de auditoría.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar auditEvents](../api/intune-auditing-auditevent-list.md)|Colección [auditEvent](../resources/intune-auditing-auditevent.md)|Enumere las propiedades y las relaciones de los objetos [auditEvent](../resources/intune-auditing-auditevent.md).|
|[Obtener auditEvent](../api/intune-auditing-auditevent-get.md)|[auditEvent](../resources/intune-auditing-auditevent.md)|Lea las propiedades y las relaciones del objeto [auditEvent](../resources/intune-auditing-auditevent.md).|
|[Crear auditEvent](../api/intune-auditing-auditevent-create.md)|[auditEvent](../resources/intune-auditing-auditevent.md)|Cree un objeto [auditEvent](../resources/intune-auditing-auditevent.md).|
|[Eliminar auditEvent](../api/intune-auditing-auditevent-delete.md)|Ninguna|Elimina un [auditEvent](../resources/intune-auditing-auditevent.md).|
|[Actualizar auditEvent](../api/intune-auditing-auditevent-update.md)|[auditEvent](../resources/intune-auditing-auditevent.md)|Actualice las propiedades de un objeto [auditEvent](../resources/intune-auditing-auditevent.md).|
|[Función getAuditCategories](../api/intune-auditing-auditevent-getauditcategories.md)|Colección de cadenas|Todavía no documentado|
|[Función getAuditActivityTypes](../api/intune-auditing-auditevent-getauditactivitytypes.md)|Colección de cadenas|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|displayName|String|Nombre para mostrar del evento.|
|componentName|String|Nombre del componente.|
|actor|[auditActor](../resources/intune-auditing-auditactor.md)|Usuario y aplicación de AAD que están asociados al evento de auditoría.|
|actividad|String|Nombre descriptivo de la actividad.|
|activityDateTime|DateTimeOffset|La fecha y hora en UTC a la que se realizó la actividad.|
|activityType|String|El tipo de actividad que se realizó.|
|activityOperationType|String|El tipo de operación HTTP de la actividad.|
|activityResult|String|El resultado de la actividad.|
|correlationId|Guid|El identificador de la solicitud de cliente que se usa para correlacionar las actividades dentro del sistema.|
|recursos|Colección [auditResource](../resources/intune-auditing-auditresource.md)|Recursos que se están modificando.|
|.|String|Categoría de auditoría.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.auditEvent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditEvent",
  "id": "String (identifier)",
  "displayName": "String",
  "componentName": "String",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "String",
    "userPermissions": [
      "String"
    ],
    "applicationId": "String",
    "applicationDisplayName": "String",
    "userPrincipalName": "String",
    "servicePrincipalName": "String",
    "ipAddress": "String",
    "userId": "String"
  },
  "activity": "String",
  "activityDateTime": "String (timestamp)",
  "activityType": "String",
  "activityOperationType": "String",
  "activityResult": "String",
  "correlationId": "Guid",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "String",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "String",
          "oldValue": "String",
          "newValue": "String"
        }
      ],
      "type": "String",
      "resourceId": "String"
    }
  ],
  "category": "String"
}
```





