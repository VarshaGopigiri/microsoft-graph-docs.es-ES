# <a name="working-with-azure-active-directory-resources-in-microsoft-graph"></a>Trabajar con recursos de Azure Active Directory en Microsoft Graph

Con Microsoft Graph, puede obtener acceso a recursos de [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/active-directory-whatis) para habilitar escenarios, como administrar roles de administrador (directorio), invitar a usuarios externos a una organización y, si es un [Proveedor de soluciones en la nube (CSP)](https://partner.microsoft.com/cloud-solution-provider), administrar los datos de sus clientes. Microsoft Graph también ofrece métodos que las aplicaciones pueden usar para, por ejemplo, descubrir información sobre las pertenencias a roles y grupos transitivos de los usuarios. 

> **Nota**: Algunos recursos de Azure AD se documentan en otras secciones de la referencia de la API. Para obtener más información, vea [Usuarios](users.md) y [Grupos](group.md).


## <a name="authorization"></a>Authorization
 
Para llamar a las API de Microsoft Graph en recursos de Azure AD, la aplicación necesitará los permisos adecuados. Muchas de las API expuestas en recursos de Azure AD necesitan uno de los [permisos de _directorio_](../../../concepts/permissions_reference.md#directory-permissions). Los permisos de directorio tienen privilegios muy elevados y siempre necesitan el consentimiento del administrador. 

Si la aplicación actúa en nombre de un usuario (permisos delegados), puede que este tenga que ser miembro de un [rol de administrador](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) adecuado para que la aplicación pueda llamar correctamente a muchas de las API de Azure AD.

Para obtener más información sobre permisos, incluidos permisos delegados y de aplicación, vea [Permisos](../../../concepts/permissions_reference.md). 

## <a name="common-use-cases"></a>Casos de uso común 

En la tabla siguiente se muestran algunos de los casos de uso comunes para recursos de Azure AD.

| **Casos de uso**        | **Recursos de REST** | **Ver también** |
|:---------------|:--------|:----------|
| **Objeto y métodos de directorio** | | |
| `directoryObject` es la clase base de la que heredan muchos de los recursos de directorio (por ejemplo, usuarios y grupos). Microsoft Graph expone varios métodos que puede usar para descubrir información sobre usuarios, grupos y otros objetos de directorio. Por ejemplo, puede comprobar la pertenencia transitiva en una lista de grupos, devolver todos los grupos y roles de directorio de los que es miembro transitivo un objeto de directorio u obtener todos los recursos de un tipo especificado (por ejemplo, usuario o grupo) de una lista de identificadores de recursos genéricos. | [directoryObject](../resources/directoryobject.md) | N/D |
| **Administrar roles de directorio (administrador)** | | |
| Active roles de directorio en un inquilino de Azure AD y administre las pertenencias de usuario en los roles de directorio. Los roles de directorio también se conocen como roles de administrador. | [directoryRole](../resources/directoryrole.md) <br/>[directoryRoleTemplate](../resources/directoryroletemplate.md) | [Asignar roles de administrador en Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) |
| Aplique configuraciones de grupo predefinidas en un inquilino o a instancias de recursos individuales. La configuración de grupo controla los comportamientos como las listas de palabras bloqueadas para los nombres para mostrar de grupos o si los usuarios invitados pueden ser propietarios de grupos, entre otros. | [groupSetting](../resources/groupsetting.md) <br/>[groupSettingTemplate](../resources/groupsettingtemplate.md)| [Cmdlets de Azure Active Directory para configurar configuraciones de grupo](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-groups-settings-cmdlets)|
| **Administrar dispositivos** | | |
| Administre los dispositivos registrados en la organización. Los dispositivos se registran en usuarios e incluyen elementos como portátiles, equipos de escritorio, tabletas y teléfonos móviles. Los dispositivos suelen crearse en la nube con el servicio de registro de dispositivos o Microsoft Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. | [device](../resources/device.md) | [Introducción al registro de dispositivos de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-device-registration-overview).<br/><br/>[¿Qué es Intune?](https://docs.microsoft.com/intune-classic/understand-explore/introduction-to-microsoft-intune)<br/><br/>[Inscribir dispositivos para administrarlos en Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune) |
| **Administración de inquilinos asociados** | | |
| Obtenga información sobre las asociaciones con inquilinos de clientes.<br/><br/>**Nota**: Esto solo es válido para inquilinos asociados. Los inquilinos asociados son inquilinos de Azure AD que pertenecen a los socios de Microsoft, que forman parte de los programas [Proveedor de soluciones en la nube de Microsoft](https://partnercenter.microsoft.com/partner/programs), Office 365 Syndication o Microsoft Advisor. | [contract](../resources/contract.md) | [Llamar a Microsoft Graph desde una aplicación del proveedor de soluciones en la nube](../../../concepts/auth_cloudsolutionprovider.md) |
| Administrar dominios asociados a un inquilino. Las operaciones de dominio permiten a los registradores automatizar la asociación de dominio para servicios como Office 365. | [domain](../resources/domain.md) | [Agregar un nombre de dominio personalizado a Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-domains-add-azure-portal) |
| **Administración de inquilinos** | | |
| Obtenga información sobre una organización, como su dirección comercial, los contactos técnicos y de notificaciones, los planes de servicio a los que está suscrita y los dominios asociados a esta. | [organization](../resources/organization.md) | N/D |
| Obtenga información sobre las SKU de servicio a las que está suscrita una empresa. | [subscribedSku](../resources/subscribedsku.md) | N/D |
| Invite a usuarios externos (invitados) a una organización. | [invitation](../resources/invitation.md) | [¿Qué es la colaboración B2B de Azure AD?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b) |



## <a name="next-steps"></a>Siguientes pasos
Las API y los recursos de directorio pueden proporcionar nuevas formas de comunicarse con los usuarios y administrar sus experiencias con Microsoft Graph. Para obtener más información: 

- Explore en profundidad los métodos y las propiedades de los recursos más útiles para su escenario.
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).


