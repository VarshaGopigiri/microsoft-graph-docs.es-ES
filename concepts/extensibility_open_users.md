# <a name="add-custom-data-to-users-using-open-extensions-preview"></a>Agregar datos personalizados a usuarios mediante extensiones abiertas (vista previa)
Vamos a guiarle a través de un ejemplo para demostrarle cómo usar las *extensiones abiertas*. 

Imagine que está creando una aplicación que está disponible en muchas plataformas cliente distintas, como equipos de sobremesa y móviles.  Quiere que los usuarios puedan configurar su experiencia de interfaz para que sea coherente sin importar en qué dispositivo inicien sesión en su aplicación. Se trata de un requisito común para la mayoría de las aplicaciones. 

En este escenario, vamos a mostrarle cómo:

1. Agregar una extensión abierta que represente cierta información móvil acerca del usuario.
2. Realizar una consulta al usuario y devolver el perfil móvil.
3. Cambiar la información del perfil móvil del usuario (el valor de extensión abierta).
4. Eliminar la información de perfil móvil del usuario.

>**Nota:** Este tema muestra cómo agregar, leer, actualizar y eliminar extensiones abiertas en un recurso *usuario*.  Estos métodos también se admiten para los tipos de recurso *administrativeUnit*, *póngase en contacto con*, *dispositivo*, *evento*, *grupo*, *evento de grupo*, *publicación de grupo* y *organización*.  Solo tiene que actualizar las solicitudes de ejemplo mostradas a continuación usando cualquiera de estos tipos de recurso. Las respuestas mostradas en los ejemplos siguientes pueden aparecer truncadas para abreviar. 

## <a name="1-add-roaming-profile-information"></a>1. Agregar información de perfil móvil
El usuario inicia sesión en la aplicación y configura su apariencia.  La configuración de la aplicación debe ser móvil para que el usuario reciba la misma experiencia en cualquier dispositivo desde el que inicie sesión en la aplicación.  Aquí veremos cómo agregar la información del perfil móvil a un recurso de usuario.

##### <a name="request"></a>Solicitud
```http
POST https://graph.microsoft.com/beta/me/extensions
Content-type: application/json
{
    "@odata.type":"microsoft.graph.openTypeExtension",
    "extensionName":"com.contoso.roamingSettings",
    "theme":"dark",
    "color":"purple",
    "lang":"Japanese"
}
```
##### <a name="response"></a>Respuesta
```http
HTTP/1.1 201 Created
Content-Type: application/json
Content-length: 420

{
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "extensionName": "com.contoso.roamingSettings",
    "id": "com.contoso.roamingSettings",
    "theme": "dark",
    "color": "purple",
    "lang": "Japanese"
}
```

## <a name="2-retrieve-roaming-profile-information"></a>2. Recuperar información de perfil móvil
Cuando el usuario inicia sesión en la aplicación desde otro dispositivo, esta puede recuperar los detalles del perfil de usuario, además de su configuración móvil. Esto puede hacerse obteniendo el recurso de usuario y expandiendo la propiedad de navegación de extensión.

##### <a name="request"></a>Solicitud
```http
GET https://graph.microsoft.com/beta/me?$select=id,displayName,mail,mobilePhone&$expand=extensions
```
##### <a name="response"></a>Respuesta
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-length: 420

{
    "id": "84b80893-8749-40a3-97b7-68513b600544",
    "displayName": "John Smith",
    "mail": "john@contoso.com",
    "mobilePhone": "1-555-6589",
    "extensions": [
        {
            "@odata.type": "#microsoft.graph.openTypeExtension",
            "extensionName": "com.contoso.roamingSettings",
            "id": "com.contoso.roamingSettings",
            "theme": "dark",
            "color": "purple",
            "lang": "Japanese"
        }
    ]
}
```
>**Nota:** Si tiene varias extensiones, puede filtrar por la *id* para obtener aquella que le interese.

## <a name="3-change-roaming-profile-information"></a>3. Cambiar información de perfil móvil
El usuario puede cambiar la información de su perfil móvil.  Esta actualización puede realizarse con un ```PATCH``` en el valor de extensión abierta. 

##### <a name="request"></a>Solicitud
```http
PATCH https://graph.microsoft.com/beta/me/extensions/com.contoso.roamingSettings
Content-type: application/json
{
    "theme":"light",
    "color":"yellow",
    "lang":"Swahili"
}
```

##### <a name="response"></a>Respuesta
```
HTTP/1.1 204 No content
```

## <a name="4-delete-a-users-roaming-profile"></a>4. Eliminar un perfil de usuario móvil
El usuario decide que ya no desea tener un perfil móvil y lo elimina. Esto puede realizarse con una solicitud ```DELETE``` en el valor de extensión abierta.

##### <a name="request"></a>Solicitud
```http
DELETE https://graph.microsoft.com/beta/me/extensions/com.contoso.roamingSettings
```

##### <a name="response"></a>Respuesta
```
HTTP/1.1 204 No content
```

## <a name="see-also"></a>Recursos adicionales

- [Agregar datos personalizados a los recursos mediante extensiones](extensibility_overview.md)
- [Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)](extensibility_schema_groups.md)