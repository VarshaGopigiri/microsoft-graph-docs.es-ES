---
title: tipo de recurso privilegedOperationEvent
description: Representa un evento de auditoría que se genera con privilegios de administración de identidades para las operaciones de función, como un administrador administra las funciones con privilegios, un usuario activa su función y un usuario desactiva su rol.
ms.openlocfilehash: e35e0744a8a8d54ad9f1cc8cd536b05283eaa9fb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088042"
---
# <a name="privilegedoperationevent-resource-type"></a>tipo de recurso privilegedOperationEvent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un evento de auditoría que se genera con privilegios de administración de identidades para las operaciones de función, como un administrador administra las funciones con privilegios, un usuario activa su función y un usuario desactiva su rol.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista privilegedOperationEvent](../api/privilegedoperationevent-list.md) | colección de [privilegedOperationEvent](privilegedoperationevent.md) . |Obtener la colección de objetos privilegedOperationEvent.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|información adicional|string|Información legible humana detallada para el evento.|
|creationDateTime|dateTimeOffset|Indica la hora cuando se creó el evento.|
|expirationDateTime|dateTimeOffset|Sólo se utiliza cuando la requestType es "Activar", e indica la hora de expiración de la activación de la función.|
|id|string|El identificador único para privilegedOperationEvent. Solo lectura.|
|referenceKey|string|Número de incidente/solicitud de vale durante la activación de la función. El valor se presenta sólo si se proporciona el número de vale durante la activación de la función.|
|referenceSystem|string|Incidente/solicitud de sistema que se proporcionan durante la activación de tole de vales. El valor se presenta sólo si se proporciona el sistema de vales durante la activación de la función.|
|requestType|string|El tipo de operación de solicitud. El valor de requestType puede ser: ```Assign``` (asignación de rol), ```Activate``` (activación de rol), ```Unassign``` (quitar la asignación de rol), ```Deactivate``` (desactivación de rol), ```ScanAlersNow``` (examinar las alertas de seguridad), ```DismissAlert``` (descartar la alerta de seguridad), ```FixAlertItem``` (corrección de seguridad problema de alerta), ```AccessReview_Review``` (revisar una revisión de Access), ```AccessReview_Create``` (crear una revisión de Access), ```AccessReview_Update``` (actualizar una revisión de Access), y ```AccessReview_Delete``` (eliminar una revisión de Access).|
|requestorId|string|El identificador de usuario del solicitante que inicia la operación.|
|requestorName|string|El nombre de usuario del solicitante que inicia la operación.|
|identificador de función|string|El identificador de la función que está asociada con la operación.|
|nombre de rol|string|El nombre de la función.|
|tenantId|string|El identificador de inquilino (organización).|
|userId|string|El identificador del usuario que está asociado con la operación.|
|userMail|string|Correo electrónico del usuario.|
|userName|string|El nombre para mostrar del usuario.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedOperationEvent"
}-->

```json
{
  "additionalInformation": "string",
  "creationDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "requestType": "string",
  "requestorId": "string",
  "requestorName": "string",
  "roleId": "string",
  "roleName": "string",
  "tenantId": "string",
  "userId": "string",
  "userMail": "string",
  "userName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedOperationEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
