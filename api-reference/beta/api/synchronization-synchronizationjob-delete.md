---
title: Eliminar synchronizationJob
description: Detener el trabajo de sincronización y eliminar de forma permanente todos los Estados asociados con ella. Sincronizadas cuentas se dejan como-es.
localization_priority: Normal
ms.openlocfilehash: 95a7d52e9e6fba9bc3f528aedfc5a082d459a003
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835689"
---
# <a name="delete-synchronizationjob"></a>Eliminar synchronizationJob

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Detener el trabajo de sincronización y eliminar de forma permanente todos los Estados asociados con ella. Sincronizadas cuentas se dejan como-es.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     |Directory.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |No admitida.  |
|Aplicación                            |No admitida. | 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
DELETE /servicePrincipals/{id}/synchronization/jobs/{jobId}/
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre           | Tipo    | Descripción|
|:---------------|:--------|:-----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se realiza correctamente, devuelve un `204 No Content` respuesta. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud
El siguiente es un ejemplo de una solicitud.
<!-- {
  "blockType": "request",
  "name": "delete_synchronizationjob"
}-->
```http
DELETE https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/
```

##### <a name="response"></a>Respuesta
Este es un ejemplo de la respuesta. 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete synchronizationJob",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
