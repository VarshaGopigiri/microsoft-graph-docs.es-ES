# <a name="remove-a-student"></a>Quitar un alumno

Quita un [educationUser](../resources/educationuser.md) de un [educationClass](../resources/educationclass.md)

>**Nota:** Los profesores _y_ los alumnos se encuentran en la colección **members** de la clase. Antes de llamar a esta API, asegúrese de que el **educationUser** que quita no es un profesor.  Obtenga la lista de profesores llamando a [educationclass_list_teachers](educationclass_list_teachers.md) y comprobando que el identificador de usuario del usuario que se va a quitar no se encuentra en la lista de profesores devuelta.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  No admitida.  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | EduRoster.ReadWrite.All | 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/members/{userId}/$ref
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/{class-id}/members/{member-id}
```

##### <a name="response"></a>Respuesta
Este es un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
