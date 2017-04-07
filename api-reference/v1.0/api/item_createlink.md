# <a name="create-a-sharing-link-for-a-driveitem"></a>Crear un vínculo para compartir para un DriveItem

Puede usar la acción **createLink** para compartir un [DriveItem](../resources/driveitem.md) mediante un vínculo para compartir.

La acción **createLink** creará un nuevo vínculo para compartir si el tipo de vínculo especificado no existe para la aplicación que realiza la llamada. Si ya existe el tipo de vínculo para compartir especificado para la aplicación, se devolverá el vínculo para compartir existente.

Los recursos DriveItem heredan permisos de sus antecesores.

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

  * Files.ReadWrite

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/items/{item-id}/createLink
POST /me/drive/root:/{item-path}:/createLink
POST /groups/{group-id}/drive/items/{item-id}/createLink
POST /drives/{drive-id}/items/{item-id}/createLink
```

## <a name="request-body"></a>Cuerpo de la solicitud
El cuerpo de la solicitud define el tipo de vínculo para compartir que busca su aplicación. La solicitud debe ser un objeto JSON con esta propiedad.

| Nombre      | Tipo   | Descripción                                                                  |
|:----------|:-------|:-----------------------------------------------------------------------------|
| **type**  | string | El tipo de vínculo para compartir que se creará. `view`, `edit` o `embed`.       |
| **ámbito** | string | El ámbito del vínculo que se creará. `anonymous` o `organization`. Opcional. |

## <a name="link-types"></a>Tipos de vínculos
Se pueden usar los siguientes valores para el parámetro de **tipo**.

| Valor del tipo | Descripción                                                                                  |
|:-----------|:---------------------------------------------------------------------------------------------|
| `view`     | Crea un vínculo de solo lectura para el elemento.                                                        |
| `edit`     | Crea un vínculo de solo escritura para el elemento.                                                       |
| `embed`    | Crea un vínculo insertable para el elemento. Esta opción solo está disponible para OneDrive Personal. |

## <a name="scope-types"></a>Tipos de ámbitos
Se permiten los siguientes valores para el parámetro de **ámbito**. Este parámetro es opcional. Si no se especifica el parámetro de **ámbito**, se creará el vínculo más permisivo que esté disponible.

| Valor del tipo     | Descripción                                                                                                                   |
|:---------------|:------------------------------------------------------------------------------------------------------------------------------|
| `anonymous`    | Crea un vínculo accesible para cualquier usuario para el elemento. El Administrador de inquilinos puede deshabilitar los vínculos anónimos.                 |
| `organization` | Crea un vínculo accesible dentro de una organización para el elemento. El ámbito del vínculo de organizaciones no está disponible para OneDrive Personal. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un recurso de [permiso](../resources/permission.md) único en el cuerpo de la respuesta que representa el permiso solicitado para compartir un vínculo.

El servicio buscará primero en los permisos actuales y comprobará si ya existe uno del mismo **tipo** para la aplicación que realiza la llamada.

La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "item_createlink"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root:/{item-path}:/createLink
Content-type: application/json

{
  "type": "view",
  "scope": "anonymous"
}
```

##### <a name="response"></a>Respuesta

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

OneDrive para la Empresa y SharePoint admiten vínculos de empresa para compartir. Son similares a los vínculos anónimos, pero solo funcionan para los miembros del inquilino propietario. Para crear un vínculo de empresa para compartir, utilice el parámetro de **ámbito** con un valor de `organization`.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "create-link-scoped", "scopes": "files.readwrite service.sharepoint" } -->
```
POST https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "edit",
  "scope": "organization"
}
```

## <a name="http-response"></a>Respuesta HTTP

La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->
```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "view",
    "scope": "organization",
    "webUrl": "https://contoso-my.sharepoint.com/personal/ellen_contoso_com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="embeddable-links"></a>Vínculos insertables

Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.

**Nota:** Los vínculos para insertar solo se admiten en [unidades](../resources/drive.md) donde el **driveType** es `personal`.

## <a name="remarks"></a>Comentarios

* Los vínculos creados con esta acción no caducan a menos que la organización fuerce una política de caducidad de forma predeterminada.
* Los vínculos se pueden ver en los permisos de uso compartido del elemento y los puede eliminar un propietario del elemento.
* Los vínculos siempre señalan la versión actual de un elemento, a menos que el elemento esté desprotegido (solo en SharePoint).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "item: createLink",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Create sharing link"
} -->
