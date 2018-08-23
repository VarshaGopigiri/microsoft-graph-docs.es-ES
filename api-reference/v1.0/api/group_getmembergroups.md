# <a name="group-getmembergroups"></a>grupo: getMemberGroups

Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/group_list_memberof.md), que devuelve solo los grupos de los que el grupo es miembro directo.

Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

| Tipo de permiso                        | Permisos (de menos a más privilegiados)                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| Delegado (cuenta profesional o educativa)     | ~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All |
| Delegado (cuenta personal de Microsoft) | No admitida.                                                                              |
| Aplicación                            | ~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All                             |

> **Nota:** En este momento, esta API requiere el permiso `Directory.Read.All` o superior. El uso del permiso `Group.Read.All` devolverá un error. Se trata de un problema conocido.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/getMemberGroups
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Tipo   | Descripción               |
| :------------ | :----- | :------------------------ |
| Autorización | cadena | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro           | Tipo    | Descripción                                                                           |
| :------------------ | :------ | :------------------------------------------------------------------------------------ |
| securityEnabledOnly | Booleano | Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "group_getmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/groups/{id}/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

> **Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "group: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
