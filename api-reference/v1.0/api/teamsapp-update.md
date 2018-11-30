---
title: Permissions
description: 'Actualizar una aplicación que se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams. '
ms.openlocfilehash: 38dd5cdbdb64c31d47c6d7e5b0c4bb27da8ad6e7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029244"
---
# <a name="update-apps-published-to-your-organizations-app-catalog"></a>Actualizar aplicaciones publicadas en catálogo de aplicaciones de la organización



Actualización de una [aplicación](../resources/teamsapp.md) se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams. Esta API específicamente actualiza una aplicación publicada en catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino). Para publicar en el catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).

>**Nota:** Sólo los administradores globales pueden llamar a esta API.

| Tipo de permiso                        | Permisos (de menos a más privilegiados)|
|:----------------------------------     |:-------------|
| Delegado (cuenta profesional o educativa)     | AppCatalog.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) | No admitido|
| Aplicación                            | No se admite|

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PUT /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado        | Valor           |
|:--------------|:--------------  |
| Authorization | {token} de portador. Obligatorio.  |
| Content-Type  | aplicación/zip |

## <a name="request-body"></a>Cuerpo de la solicitud

Carga de los equipos Zip manifiesto: Para la aplicación de los equipos zip archivo [consulte Creación de un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)

>**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp-list.md) para hacer referencia a la aplicación que desea actualizar. No use el identificador del manifiesto del paquete de la aplicación de zip.

## <a name="response"></a>Respuesta

```
HTTP/1.1 204 No Content
```

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

```
PUT https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

Para la aplicación de los equipos zip archivo [vea Crear paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)

### <a name="response"></a>Respuesta

```
HTTP/1.1 204 No Content
```
