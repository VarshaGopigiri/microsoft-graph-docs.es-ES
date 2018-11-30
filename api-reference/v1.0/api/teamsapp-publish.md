---
title: Permissions
description: 'Publicar una aplicación en el catálogo de aplicaciones de Microsoft Teams. '
ms.openlocfilehash: c33a1d85673b9f59aade253b2ea5fd237eb5fc83
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029348"
---
# <a name="publish-apps-to-your-organizations-app-catalog"></a>Publicar aplicaciones en el catálogo de aplicaciones de la organización



Publicar una [aplicación](../resources/teamsapp.md) en el catálogo de aplicaciones de Microsoft Teams. En concreto, esta API publica la aplicación al catálogo de su organización (el catálogo de aplicaciones de inquilino); el recurso creado tendrá `distributionMethod`  =  `organization`.

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
POST /appCatalogs/teamsApps
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado        | Valor           |
|:--------------|:--------------  |
| Authorization | {token} de portador. Obligatorio.  |
| Content-Type  | aplicación/zip |

## <a name="request-body"></a>Cuerpo de la solicitud

Carga de manifiesto Zip de los equipos. Para la aplicación de los equipos zip de archivo, [vea Crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package). No se puede crear una aplicación para una organización que tiene el mismo identificador de manifiesto que otra aplicación en esa organización.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [teamsCatalogApp](../resources/teamsapp.md) .

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

```http
POST https://graph.microsoft.com/beta/appCatalogs/teamsApps
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

Para obtener información acerca de cómo crear un archivo zip de aplicación de Microsoft Teams, consulte [crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package). 

### <a name="response"></a>Respuesta

```
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "e3e29acb-8c79-412b-b746-e6c39ff4cd22",
  "externalId": "b5561ec9-8cab-4aa3-8aa2-d8d7172e4311",
  "name": "Test App",
  "version": "1.0.0",
  "distributionMethod": "organization"
}
```
