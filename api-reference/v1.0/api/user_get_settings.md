# <a name="get-settings"></a>Obtener la configuración

Leer el objeto de [configuración de](../resources/user_settings.md) usuario y de organización.
Para obtener más información acerca de cómo actualizar las propiedades del objeto de [configuración](../resources/user_settings.md) , consulte [actualización de la configuración de usuario](user_update_settings.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.Read.All, User.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | User.Read.All,User.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

```http
GET /me/settings/
```

Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All. Para obtener más información, vea [permisos](../../../concepts/permissions_reference.md).

```http
GET /users/{id | userPrincipalName}/settings/
```

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` objeto de [configuración de usuario](../resources/user_settings.md) y el código de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

```http
GET https://graph.microsoft.com/v1.0/me/settings
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": false
}
```

