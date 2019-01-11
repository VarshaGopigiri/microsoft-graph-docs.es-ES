---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartir un archivo con un vínculo
localization_priority: Normal
ms.openlocfilehash: 222917a869487f8e0fd893d641436f001354dfb1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871130"
---
# <a name="create-a-sharing-link-for-a-driveitem"></a>Crear un vínculo para compartir para un DriveItem

Puede usar la acción **createLink** para compartir un [DriveItem](../resources/driveitem.md) mediante un vínculo para compartir.

La acción **createLink** creará un nuevo vínculo para compartir si el tipo de vínculo especificado no existe para la aplicación que realiza la llamada. Si ya existe el tipo de vínculo para compartir especificado para la aplicación, se devolverá el vínculo para compartir existente.

Los recursos DriveItem heredan permisos de uso compartido de sus antecesores.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/createLink
POST /groups/{groupId}/drive/items/{itemId}/createLink
POST /me/drive/items/{itemId}/createLink
POST /sites/{siteId}/drive/items/{itemId}/createLink
POST /users/{userId}/drive/items/{itemId}/createLink
```

### <a name="request-body"></a>Cuerpo de la solicitud

El cuerpo de la solicitud define las propiedades del vínculo para compartir que solicita su aplicación.
La solicitud debe ser un objeto JSON con las siguientes propiedades.

|   Nombre    |  Tipo  |                                 Descripción                                  |
| :-------- | :----- | :--------------------------------------------------------------------------- |
| **type**  | string | El tipo de vínculo para compartir que se creará. `view`, `edit` o `embed`.       |
| **ámbito** | string | Opcional. El ámbito del vínculo que se creará. `anonymous` o `organization`. |


### <a name="link-types"></a>Tipos de vínculos

Se pueden usar los siguientes valores para el parámetro de **tipo**.

| Valor del tipo | Descripción                                                                                  |
|:-----------|:---------------------------------------------------------------------------------------------|
| `view`     | Crea un vínculo de solo lectura para el objeto DriveItem.                                                        |
| `edit`     | Crea un vínculo de lectura y escritura para el objeto DriveItem.                                                       |
| `embed`    | Crea un vínculo insertable para el objeto DriveItem. Esta opción solo está disponible para archivos en OneDrive Personal. |

### <a name="scope-types"></a>Tipos de ámbitos

Se permiten los siguientes valores para el parámetro **scope**.
Si el parámetro **scope** no se especifica, se crea el tipo de vínculo predeterminado para la organización.

| Valor          | Description
|:---------------|:------------------------------------------------------------
| `anonymous`    | Cualquier usuario con el vínculo tiene acceso, sin necesidad de iniciar sesión. Esto puede incluir personas fuera de la organización. Compatibilidad con vínculo anónimo puede ser deshabilitado por un administrador.
| `organization` | Cualquier usuario que ha iniciado sesión en su organización (inquilino) puede usar el vínculo para obtener acceso. Sólo está disponible en OneDrive para profesionales y SharePoint.


## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) único en el cuerpo de la respuesta que representa los permiso de uso compartido solicitados.

La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, se solicita un vínculo para compartir que se creará para el objeto DriveItem especificado por {itemId} en el OneDrive del usuario.
El vínculo para compartir está configurado para que sea de solo lectura y lo pueda usar cualquier usuario que tenga el vínculo.

### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "create-link"
}-->

```http
POST /me/drive/items/{item-id}/createLink
Content-type: application/json

{
  "type": "view",
  "scope": "anonymous"
}
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "view",
    "scope": "anonymous",
    "webUrl": "https://1drv.ms/A6913278E564460AA616C71B28AD6EB6",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="creating-company-sharable-links"></a>Crear vínculos de empresa para compartir

OneDrive para la Empresa y SharePoint admiten vínculos de empresa para compartir.
Son similares a los vínculos anónimos, pero solo funcionan para los miembros de la organización propietaria.
Para crear un vínculo de empresa para compartir, utilice el parámetro de **ámbito** con un valor de `organization`.

### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "name": "create-link-scoped", "scopes": "files.readwrite", "tags": "service.sharepoint" } -->

```http
POST /me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "edit",
  "scope": "organization"
}
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "edit",
    "scope": "organization",
    "webUrl": "https://contoso-my.sharepoint.com/personal/ellen_contoso_com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="creating-embeddable-links"></a>Crear vínculos insertables

Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.

**Nota:** La acción de insertar vínculos solo se admite en OneDrive Personal.

### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "name": "create-embedded-link", "scopes": "files.readwrite", "tags": "service.onedrive service.graph" } -->

```http
POST /me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "embed"
}
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["read"],
  "link": {
    "type": "embed",
    "webHtml": "<IFRAME src=\"https://onedrive.live.com/...\"></IFRAME>",
    "webUrl": "https://onedrive.live.com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="remarks"></a>Comentarios

* Los vínculos creados con esta acción no caducan a menos que la organización fuerce una política de caducidad de forma predeterminada.
* Los vínculos se pueden ver en los permisos de uso compartido del elemento y los puede eliminar un propietario del elemento.
* Los vínculos siempre señalan la versión actual de un elemento, a menos que el elemento esté desprotegido (solo en SharePoint).

<!-- {
  "type": "#page.annotation",
  "description": "Create a new sharing link for an item.",
  "keywords": "create,sharing,sharing link",
  "section": "documentation",
  "tocPath": "Sharing/Create link"
} -->
