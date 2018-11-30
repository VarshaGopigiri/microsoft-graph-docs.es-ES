---
title: Crear synchronizationJob
description: Crear nuevo trabajo de sincronización con un esquema de sincronización predeterminado. El trabajo se crea en un estado deshabilitado. Llamada de trabajo de inicio para iniciar la sincronización.
ms.openlocfilehash: 3c7e3c3a9c89f95b031cd45d38848e0f2f451de7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090272"
---
# <a name="create-synchronizationjob"></a>Crear synchronizationJob

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear nuevo trabajo de sincronización con un esquema de sincronización predeterminado. El trabajo se crea en un estado deshabilitado. Llamar a [iniciar el trabajo](synchronization-synchronizationjob-start.md) para iniciar la sincronización.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     |Directory.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |No admitida.|
|Aplicación                            |No admitida.  | 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre           | Tipo    | Descripción|
|:---------------|:--------|:-----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [synchronizationJob](../resources/synchronization-synchronizationjob.md) que se creará. La única propiedad necesaria es `templateId`. El `templateId` (propiedad) debe coincidir con una de las plantillas creadas para esta entidad de seguridad de la aplicación o servicio. Para buscar plantillas disponibles, use [las plantillas de lista](synchronization-synchronizationtemplate-list.md).

## <a name="response"></a>Respuesta

Si se realiza correctamente, devuelve un `201 Created` código de respuesta y un objeto [synchronizationJob](../resources/synchronization-synchronizationjob.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud
El siguiente es un ejemplo de una solicitud.
<!-- {
  "blockType": "request",
  "name": "create_synchronizationjob_from_synchronization"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs
Content-type: application/json

{ 
    "templateId": "BoxOutDelta"
}
```

##### <a name="response"></a>Respuesta
El siguiente es un ejemplo de una respuesta. 

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationJob"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "{jobId}",
    "templateId": "BoxOutDelta",
    "schedule": {
        "expiration": null,
        "interval": "P10675199DT2H48M5.4775807S",
        "state": "Disabled"
    },
    "status": {
        "countSuccessiveCompleteFailures": 0,
        "escrowsPruned": false,
        "synchronizedEntryCountByType": [],
        "code": "NotConfigured",
        "lastExecution": null,
        "lastSuccessfulExecution": null,
        "lastSuccessfulExecutionWithExports": null,
        "steadyStateFirstAchievedTime": "0001-01-01T00:00:00Z",
        "steadyStateLastAchievedTime": "0001-01-01T00:00:00Z",
        "quarantine": null,
        "troubleshootingUrl": null
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create synchronizationJob",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->