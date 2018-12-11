---
title: Equipo de archivo
description: 'Archivar el equipo especificado. '
ms.openlocfilehash: 3e25a6b5cf5475eeacfb7b01e52775e0b483b2be
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222558"
---
# <a name="archive-team"></a>Equipo de archivo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Archivar el [equipo](../resources/team.md)de especificado. Cuando un equipo se archiva, los usuarios pueden enviar ya no o como mensajes en cualquier canal en el equipo, modificar otras opciones de configuración, descripción o nombre del grupo o en general realizar mayoría de los cambios en el equipo.
Continuarán con los cambios de pertenencia en el equipo que se permitirán.

El archivado es una operación asíncrona. Un equipo se archiva una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.

Para poder archivar el equipo, el equipo y el [grupo](../resources/group.md) deben tener un propietario.

Para restaurar un equipo de su estado archivado, use la API de [unarchive](team-unarchive.md).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.ReadWrite.All    |

> **Nota**: esta API es compatible con permisos de administrador. Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/archive
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En la solicitud, _opcionalmente_ puede incluir la `shouldSetSpoSiteReadOnlyForMembers` parámetro en un JSON body, como se indica a continuación.
```JSON
{
    "shouldSetSpoSiteReadOnlyForMembers": true
}
```
Este parámetro opcional define si se va a establecer permisos para los miembros del equipo de solo lectura en el sitio de Sharepoint Online asociado con el equipo. Si se establece en false o se omite el cuerpo por completo, se producirá este paso se omitirá.

## <a name="response"></a>Respuesta

Si el archivado se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta. La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar el archivado del equipo. Comprobar el estado de la operación de archivado mediante la realización de una solicitud GET en esta ubicación.

## <a name="example"></a>Ejemplo
#### <a name="request"></a>Solicitud
El siguiente es un ejemplo de una solicitud.
<!-- {
  "blockType": "ignored",
  "name": "archive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/archive
```
#### <a name="response"></a>Respuesta
El siguiente es un ejemplo de una respuesta.
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```
<!-- uuid: e848414b-4669-4484-ac36-1504c58a3fb8
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Archive team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
