# <a name="section-copytonotebook"></a>sección: copyToNotebook
Copia una sección a un bloc de notas específico.

En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:   

Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/copyToNotebook
POST /users/{id | userPrincipalName}/onenote/sections/{id}/copyToNotebook
POST /groups/{id}/onenote/sections/{id}/copyToNotebook
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | cadena  | `Bearer <token>` Un token válido de OAuth facilitado a la aplicación en función de las credenciales de usuario y de si este tiene autorizado el acceso. |
| Content-Type | cadena | `application/json` |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.

| Parámetro       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|groupId|Cadena|El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.|
|id|Cadena|Obligatorio. El id. del bloc de notas de destino. |
|renameAs|Cadena|El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente. |

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "section_copytonotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/copyToNotebook
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "section: copyToNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->