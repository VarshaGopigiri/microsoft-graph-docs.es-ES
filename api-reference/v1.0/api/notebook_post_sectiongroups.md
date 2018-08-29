# <a name="create-sectiongroup"></a>Crear sectionGroup

Crea un [grupo de sección](../resources/sectiongroup.md) nuevo en el bloc de notas especificado.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Notes.Create, Notes.ReadWrite    |
|Aplicación | Notes.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/sectionGroups
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/sectionGroups
POST /groups/{id}/onenote/notebooks/{id}/sectionGroups
POST /sites/{id}/onenote/notebooks/{id}/sectionGroups
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | cadena  | {token} de portador. Obligatorio. |
| Content-Type | string | `application/json` |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, asigne un nombre al grupo de sección.

En el mismo nivel de jerarquía, los nombres de grupo de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?*\/:<>|&#''%~

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [sectionGroup](../resources/sectiongroup.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_sectiongroup_from_notebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sectionGroups
Content-type: application/json
Content-length: 30

{
  "displayName": "Section group name"
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectionGroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

{
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "displayName": "name-value",
  "createdBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  },
  "lastModifiedBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create SectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
