# <a name="use-the-onenote-rest-api"></a>Usar la API de REST de OneNote

Microsoft Graph permite a su aplicación obtener autorización de acceso a blocs de notas OneNote de un usuario, a secciones y páginas en una cuenta personal u organizativa. Con los [permisos adecuados delegados o de la aplicación](../../../concepts/permissions_reference.md#notes-permissions), la aplicación puede tener acceso a los datos de OneNote del usuario que haya iniciado sesión o cualquier usuario en una cuenta empresarial.

## <a name="root-url"></a>Dirección URL raíz
La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote.
```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```
El segmento `version` de la URL representa la versión de Microsoft Graph que quiere utilizar:

- `v1.0` corresponde al código de producción estable.
- `beta` corresponde a la prueba de una característica que se encuentra en desarrollo. Pueden cambiar las características y la funcionalidad en el extremo de la versión beta; no se recomienda usarlos en el código de producción.

La ubicación puede ser el bloc de notas del usuario en Office 365 o OneDrive para consumidores, los blocs de notas de grupo o blocs de notas de grupo hospedados en un sitio de SharePoint en Office 365. 

![Pila de desarrollo de la API de OneNote](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/onenote-dev-diagram.png)

### <a name="user-notebooks"></a>Blocs de notas de usuario
Para obtener acceso a los blocs de notas personales en OneDrive para consumidores o para la empresa, utilice una de las siguientes direcciones URL:

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

- `me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).
- `users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual. Use la API de los [usuarios](users.md).
> **Nota:** Puede obtener identificadores de usuario realizando una solicitud GET en `https://graph.microsoft.com/v1.0/users`.

### <a name="group-notebooks"></a>Blocs de notas de grupo
Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
### <a name="sharepoint-site-notebooks"></a>Blocs de notas del sitio de SharePoint

Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

