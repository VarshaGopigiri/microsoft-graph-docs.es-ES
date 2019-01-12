---
title: Trabajar con acciones de larga duración (beta)
description: Este artículo describe cómo trabajar con acciones de ejecución prolongada.
localization_priority: Normal
ms.openlocfilehash: d7ee9631e9e18ae1972e2b156366c66d3d3dd455
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868057"
---
# <a name="working-with-long-running-actions-beta"></a>Trabajar con acciones de ejecución prolongada (beta)

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Algunas respuestas de API requieren un tiempo indeterminado para completarse.
En lugar de esperar hasta que se completa la acción antes de devolver una respuesta, Microsoft Graph puede usar un modelo de acciones de larga duración.
Este patrón le proporciona a su aplicación una espera para sondear actualizaciones de estado en una acción de larga duración, sin ninguna solicitud que espere a que se complete la acción.

El modelo general sigue estos pasos:

1. La aplicación solicita una acción de larga duración mediante la API. La API acepta la acción y devuelve una respuesta `202 Accepted` junto con un encabezado de ubicación para la dirección URL de la API para recuperar los informes de estado de la acción.
2. La aplicación solicita la dirección URL del informe de estado de la acción y recibe una respuesta [AsyncJobStatus](/graph/api/resources/asyncjobstatus?view=graph-rest-beta) con el progreso de la acción de larga duración
3. Se completa la acción de larga duración. 
4. La aplicación vuelve a solicitar la dirección URL del informe de estado de la acción y recibe una respuesta [AsyncJobStatus](/graph/api/resources/asyncjobstatus?view=graph-rest-beta) en la que se muestra la finalización de la acción.

## <a name="initial-action-request"></a>Solicitud de acción inicial

Vamos a recorrer los pasos para obtener un ejemplo del escenario [copiar de DriveItem](/graph/api/driveitem-copy?view=graph-rest-beta).
En este escenario, la aplicación solicita copiar una carpeta que contiene una gran cantidad de datos.
Esta solicitud probablemente tardará varios segundos en completarse ya que la cantidad de datos es grande.

<!-- { "blockType": "request", "name": "lro-copy-item-example", "scopes": "files.readwrite" } -->

```http
POST https://graph.microsoft.com/beta/me/drive/items/{folder-item-id}/copy
Content-Type: application/json

{
  "parentReference": {
    "path": "/drive/root:/Documents"
  },
  "name": "Copy of LargeFolder1"
}
```

La API responde que la acción se ha aceptado junto con la dirección URL para recuperar el estado de la acción de larga duración.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 202 Accepted
Location: https://api.onedrive.com/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

**Nota**: La dirección URL devuelta no puede estar en el punto de conexión de la API de Microsoft Graph.

En muchos casos esto puede ser el final de la solicitud, ya que la acción de copia se completará sin que la aplicación realice ninguna acción adicional. En cambio, si la aplicación tiene que mostrar el estado de la acción de copia o garantizar que finaliza sin errores, puede hacerlo con la dirección URL de supervisión.

## <a name="retrieve-a-status-report-from-the-monitor-url"></a>Recuperar un informe de estado desde la dirección URL de supervisión

Para comprobar el estado de la acción de copia, la aplicación realiza una solicitud a la dirección URL proporcionada en la respuesta anterior.
*Nota:* Esta solicitud no necesita autenticación, ya que la dirección URL es de corta duración y única para el autor de la llamada original. 

<!-- { "blockType": "request", "opaqueUrl": true, "name": "lro-check-status", "scopes": "files.readwrite" } -->

```http
GET https://api.onedrive.com/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

El servicio responde con información de que la acción de larga duración todavía está en curso:

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.asyncJobStatus" } -->

```http
HTTP/1.1 202 Accepted
Content-type: application/json

{
  "operation": "ItemCopy",
  "percentageComplete": 27.8,
  "status": "inProgress"
}
```

Esta información puede usarse para proporcionar una actualización al usuario sobre el progreso de la acción de copia.
La aplicación puede continuar sondeando la dirección URL de supervisión para solicitar actualizaciones de estado y mantener el seguimiento del progreso de la acción.

## <a name="retrieve-a-completed-status-report-from-the-monitor-url"></a>Recuperar un informe de estado completado desde la dirección URL de supervisión

Después de unos segundos, la operación de copia se ha completado.
Esta vez, cuando la aplicación realiza una solicitud a la dirección URL de supervisión, la respuesta es un redireccionamiento al resultado finalizado de la acción.

<!-- { "blockType": "request", "opaqueUrl": true, "name": "lro-check-status-complete", "scopes": "files.readwrite" } -->

```http
GET https://api.onedrive.com/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

Una vez finalizada la acción, la respuesta del servicio de supervisión devolverá el valor resourceId de los resultados.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.asyncJobStatus" } -->

```http
HTTP/1.1 202 Accepted
Content-type: application/json

{
    "percentageComplete": 100.0,
    "resourceId": "01MOWKYVJML57KN2ANMBA3JZJS2MBGC7KM",
    "status": "completed"
}
```

## <a name="retrieve-the-results-of-the-completed-operation"></a>Recuperar los resultados de la operación completada

Una vez que haya finalizado el trabajo, la dirección URL de supervisión devuelve el resourceId del resultado, en este caso la nueva copia del elemento original.
Puede dirigir este nuevo elemento mediante resourceId, por ejemplo:

<!-- {
  "blockType": "request",
  "name": "lro-copy-item-example-complete",
  "scopes": "files.readwrite"
} -->

```http
GET https://graph.microsoft.com/beta/me/drive/items/{item-id}
```

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "",
    "name": "Copy of LargeFolder1",
    "folder": { },
    "size": 12019
}
```

## <a name="supported-resources"></a>Recursos admitidos

Las acciones de larga duración son compatibles con los siguientes métodos de la API

| **Recurso** | **API** |
|:------ | :------ |
| DriveItem | [Copiar](/graph/api/driveitem-copy?view=graph-rest-beta) |

## <a name="prerequisites"></a>Requisitos previos

Para consultar el estado de una acción de larga duración se requieren los mismos [permisos](./permissions-reference.md) que para realizarla.




<!-- {
  "type": "#page.annotation",
  "description": "Monitor the progress of long-running actions in the API.",
  "keywords": "monitor,long,running,operation,action",
  "section": "documentation",
  "suppressions": [
    "Error: lro-check-status:
      Unable to locate a definition for resource type: microsoft.graph.asyncJobStatus",
    "Error: lro-check-status-complete:
      Unable to locate a definition for resource type: microsoft.graph.asyncJobStatus"
  ],
  "tocPath": "Concepts/Long running actions"
} -->
