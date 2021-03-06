---
title: Tipo de recurso auditEvent
description: Una clase que contiene las propiedades del evento de auditoría.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 445ed776de946c3b557e387164f81dcf4ee16ab2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940970"
---
# <a name="auditevent-resource-type"></a>Tipo de recurso auditEvent

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
|id|String|Clave de la entidad.|
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



