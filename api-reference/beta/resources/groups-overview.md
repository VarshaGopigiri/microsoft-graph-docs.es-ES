# <a name="working-with-groups-in-microsoft-graph"></a>Trabajar con grupos en Microsoft Graph

Los grupos son colecciones de [usuarios](user.md) y otras entidades de seguridad que comparten el acceso a recursos de servicios de Microsoft o de la aplicación. Microsoft Graph proporciona API que se pueden usar para crear y administrar diversos tipos de grupos y funcionalidades de grupo según la situación. Todas las operaciones relacionadas con grupos de Microsoft Graph requieren permisos de administrador.

> **Nota**: Solo se pueden crear grupos mediante cuentas profesionales o educativas. Las cuentas personales de Microsoft no admiten grupos.

| Tipo              | Caso de uso | groupType | Con correo habilitado | Con seguridad habilitada | ¿Se puede crear mediante API? |
|-------------------|----------|-----------|--------------|------------------|--------------------------------|
| [Grupos de Office 365](#office-365-groups) | Facilitar la colaboración de usuarios con recursos compartidos en línea de Microsoft. | `["Unified"]` | `true` | `false` | Sí | [user](user.md) |
| [Grupos de seguridad](#security-groups-and-mail-enabled-security-groups) | Controlar el acceso de los usuarios a recursos de la aplicación. | `[]` | `false` | `true` | Sí |
| [Grupos de seguridad habilitados para correo](#security-groups-and-mail-enabled-security-groups) | Controlar el acceso de los usuarios a recursos de la aplicación, con un buzón de grupo compartido. | `[]` | `true` | `true` | No |
| Grupos de distribución | Distribuir correo a los miembros del grupo. Se recomienda usar Grupos de Office 365 debido al variado conjunto de recursos que proporcionan. | `[]` | `true` | `false` | No |

## <a name="office-365-groups"></a>Grupos de Office 365
La utilidad de Grupos de Office 365 reside en su naturaleza colaborativa, ideal para personas que trabajan juntas en un proyecto o equipo. Se crean con los recursos que comparten los miembros del grupo, incluidos los siguientes:

- Conversaciones de Outlook
- Calendario de Outlook
- Archivos de SharePoint
- Bloc de notas de OneNote
- Sitio de grupo de SharePoint
- Planes de Planner
- Administración de dispositivos de Intune

### <a name="group-in-outlook-example"></a>Ejemplo de grupo de Outlook

Esta es una representación JSON de grupos en Outlook. 

```http

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups/$entity",
    "id": "4c5ee71b-e6a5-4343-9e2c-4244bc7e0938",
    "deletedDateTime": null,
    "classification": "MBI",
    "createdDateTime": "2016-08-23T14:46:56Z",
    "description": "This is a group in Outlook",
    "displayName": "OutlookGroup101",
    "groupTypes": [
        "Unified"
    ],
    "mail": "outlookgroup101@service.microsoft.com",
    "mailEnabled": true,
    "mailNickname": "outlookgroup101",
    "preferredLanguage": null,
    "proxyAddresses": [
        "smtp:outlookgroup101@microsoft.onmicrosoft.com",
        "SMTP:outlookgroup101@service.microsoft.com"
    ],
    "securityEnabled": false,
    "theme": null,
    "visibility": "Public"
}
```
Para más información sobre Grupos de Office 365 y las experiencias de administrador, vea [Obtenga más información sobre los grupos de Office 365](https://support.office.com/es-ES/article/Learn-about-Office-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2).

## <a name="security-groups-and-mail-enabled-security-groups"></a>Grupos de seguridad y grupos de seguridad con correo habilitado

Los grupos de seguridad están diseñados para controlar el acceso de los usuarios a los recursos. Al comprobar si un usuario es miembro de un grupo de seguridad, la aplicación puede tomar decisiones de autorización cuando el usuario intenta obtener acceso a algunos recursos seguros de la aplicación. Los grupos de seguridad pueden tener como miembros usuarios y otros grupos de seguridad.

Los grupos de seguridad con correo habilitado se usan de la misma manera que los grupos de seguridad, pero incluyen la función de buzón compartido para los grupos. No es posible crear grupos de seguridad con correo habilitado mediante la API, pero otras operaciones de grupo seguirán funcionando. Obtenga más información en el artículo [Administrar grupos de seguridad de correo en Exchange](https://technet.microsoft.com/es-ES/library/bb123521%28v=exchg.160%29.aspx).

### <a name="security-group-example"></a>Ejemplo de grupo de seguridad

Esta es una representación JSON de un grupo de seguridad. 

```http
{
    "@odata.type": "#microsoft.graph.group",
    "id": "f87faa71-57a8-4c14-91f0-517f54645106",
    "deletedDateTime": null,
    "classification": null,
    "createdDateTime": "2016-07-20T09:21:23Z",
    "description": "This group is a Security Group",
    "displayName": "SecurityGroup101",
    "groupTypes": [],
    "mail": null,
    "mailEnabled": false,
    "mailNickname": "",
    "preferredLanguage": null,
    "proxyAddresses": [],
    "securityEnabled": true
}
```
## <a name="dynamic-membership"></a>Pertenencia dinámica 

Todos los tipos de grupos pueden tener reglas de pertenencia dinámica que agregan o quitan miembros automáticamente del grupo según las propiedades del usuario. Por ejemplo, el grupo "Empleados de marketing" incluirá a todos los usuarios con la propiedad department establecida en "marketing", de modo que los nuevos empleados de marketing se agreguen automáticamente al grupo y los empleados que dejen el departamento se eliminen automáticamente del grupo. Esta regla se puede especificar en un campo "membershipRule" durante la creación de grupos como `"membershipRule": 'user.department -eq "Marketing"'`. GroupType también debe incluir `"DynamicMembership"`. Mediante la solicitud siguiente se crea un grupo de Office 365 para los empleados de marketing: 

```http
POST https://graph.microsoft.com/beta/groups
{
    "description": "Marketing department folks",
    "displayName": "Marketing department",
    "groupTypes": [
        "Unified",
        "DynamicMembership"
    ],
    "mailEnabled": true,
    "mailNickname": "marketing",
    "securityEnabled": false,
    "membershipRule": 'user.department -eq "Marketing"',
    "membershipRuleProcessingState": "on"
}
```

Para más información sobre la formulación de propiedades membershipRule, vea [Creación de reglas de pertenencia dinámica a grupos basadas en atributos en Azure Active Directory](https://docs.microsoft.com/es-ES/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).

> **Nota**: Las reglas de pertenencia dinámica requieren que el inquilino tenga una licencia de nivel [Azure Active Directory Premium P1](https://azure.microsoft.com/es-ES/pricing/details/active-directory/) o superior.

## <a name="other-types-of-groups"></a>Otros tipos de grupos

Los Grupos de Office 365 en Yammer se usan para facilitar la colaboración de usuarios a través de publicaciones de Yammer. Este tipo de grupo se puede devolver a través de una solicitud de lectura, pero no se puede obtener acceso a sus publicaciones mediante la API. Cuando las publicaciones y las fuentes de conversaciones de Yammer están habilitadas en un grupo, se deshabilitan las conversaciones del grupo de Office 365 predeterminado. Para más información, vea los [documentos de la API para desarrolladores de Yammer](https://developer.yammer.com/docs).

## <a name="common-use-cases"></a>Casos de uso común

Con Microsoft Graph, puede llevar a cabo las siguientes operaciones comunes.

| **Casos de uso**  | **Recursos de REST** | **Ver también** |
|:---------------|:--------|:----------|
| **Métodos de objeto de grupo** | | |
| Crear grupos, obtener grupos existentes, actualizar las propiedades de los grupos y eliminar grupos. Actualmente, solo se pueden crear mediante la API grupos de seguridad y grupos de Outlook. | [group](group.md) | [Crear grupos](../api/group_post_groups.md) <br/> [Enumerar grupos](../api/group_list.md) <br/> [Actualizar grupos](../api/group_update.md) <br/> [Eliminar grupos](../api/group_delete.md) |
| **Métodos de pertenencia a grupos** | | |
| Enumerar los miembros de un grupo y agregar o quitar miembros. | [user](user.md) <br/> [group](group.md)| [Enumerar miembros](../api/group_list_members.md) <br/> [Agregar miembro](../api/group_post_members.md) <br/> [Eliminar miembro](../api/group_delete_members.md)|
| Determinar si un usuario es miembro de un grupo y obtener todos los grupos a los que pertenece el usuario. | [user](user.md) <br/> [group](group.md)| [Comprobar grupos de miembro](../api/group_checkmembergroups.md) <br/> [Obtener grupos de miembro](../api/group_getmembergroups.md)|
| Enumerar los propietarios de un grupo y agregar o quitar propietarios. | [user](user.md) <br/> [group](group.md)| [Enumerar propietarios](../api/group_list_members.md) <br/> [Agregar miembro](../api/group_post_members.md) <br/> [Eliminar miembro](../api/group_delete_members.md)|
