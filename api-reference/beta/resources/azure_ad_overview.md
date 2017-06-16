# <a name="working-with-azure-active-directory-resources-in-microsoft-graph"></a>Trabajar con recursos de Azure Active Directory en Microsoft Graph

Con Microsoft Graph, puede obtener acceso a recursos de [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/active-directory-whatis) que puede usar para habilitar diferentes escenarios. Esto incluye la posibilidad de administrar roles de administrador (directorio), invitar a usuarios externos a una organización y, si es [proveedor de soluciones en la nube (CSP)](https://partner.microsoft.com/cloud-solution-provider), administrar los datos de los clientes. Microsoft Graph también proporciona varios métodos que pueden usar muchos tipos de aplicaciones; por ejemplo, para descubrir información sobre las pertenencias a grupos y roles transitivas de los usuarios. 

> **Nota**: Algunos recursos de Azure AD se documentan en otras secciones de la referencia de la API. Para obtener más información, consulte [usuarios](users.md) y [grupos](group.md).


## <a name="authorization"></a>Autorización
 
Para llamar a las API de Microsoft Graph en recursos de Azure AD, la aplicación necesitará los permisos adecuados.  Muchas de las API expuestas en recursos de Azure AD requieren uno de los [permisos _Directory_](../../../concepts/permissions_reference.md#directory-permissions).  Los permisos _Directory_ tienen privilegios elevados y requieren siempre el consentimiento del administrador. 

Hay dos tipos de permisos: delegados y de aplicación. Si la aplicación llama a una API en nombre de un usuario, necesitará permisos delegados. Si llama a una API como ella misma sin un usuario que haya iniciado sesión, necesitará permisos de aplicación. Este último escenario suele producirse en el caso de demonios o servicios back-end. Para obtener más información sobre los permisos delegados y de aplicación, consulte [Permisos](../../../concepts/permissions_reference.md). 

Por último, si su aplicación está actuando en nombre de un usuario, es probable que este tenga que ser miembro de un [rol de administrador](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) adecuado para que la aplicación llame correctamente a muchas de las API de Azure AD.

## <a name="common-use-cases"></a>Casos de uso común 

En la tabla siguiente, se muestran algunos escenarios comunes para los que se pueden usar recursos de Azure AD.

| Casos de uso        | Recursos de REST | Vea también |
|:---------------|:--------|:----------|
| **Objeto y métodos de directorio** | | |
| `directoryObject` es la clase base de la que heredan muchos de los recursos de directorio (por ejemplo, usuarios y grupos). Microsoft Graph expone varios métodos que puede usar para descubrir información sobre usuarios, grupos y otros objetos de directorio. Por ejemplo, puede comprobar la pertenencia transitiva en una lista de grupos, devolver todos los grupos y roles de directorio de los que es miembro transitivo un objeto de directorio u obtener todos los recursos de un tipo especificado (por ejemplo, usuario o grupo) de una lista de identificadores de recursos genéricos. | [directoryObject](../resources/directoryobject.md) | N/D |
| **Administrar roles de directorio (administrador)** | | |
| Active roles de directorio en un inquilino de Azure AD y administre las pertenencias de usuario en los roles de directorio. Los roles de directorio también se conocen como roles de administrador. | [directoryRole](../resources/directoryrole.md) <br/>[directoryRoleTemplate](../resources/directoryroletemplate.md) | Para obtener más información sobre los roles de directorio (administrador), consulte [Asignación de roles de administrador en Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles). |
| **Administrar dispositivos** | | |
| Administre los dispositivos registrados en la organización. Los dispositivos se registran en usuarios e incluyen elementos como portátiles, equipos de escritorio, tabletas y teléfonos móviles. Los dispositivos se crean normalmente en la nube con el servicio de registro de dispositivos o Microsoft Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. | [device](../resources/device.md) | Para obtener más información sobre el servicio de registro de dispositivos, consulte [Introducción al Registro de dispositivos de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-device-registration-overview).<br/><br/> Para obtener más información sobre Microsoft Intune, consulte [What is Intune?](https://docs.microsoft.com/intune-classic/understand-explore/introduction-to-microsoft-intune) (¿Qué es Intune?) e [Inscribir dispositivos para administrarlos en InTune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune). |
| **Administración de inquilinos asociados** | | |
| Obtenga información sobre las asociaciones con inquilinos de clientes. | [contract](../resources/contract.md) | Solo existe en los inquilinos asociados. Los inquilinos asociados son inquilinos de Azure AD que pertenecen a los socios de Microsoft que forman parte de los programas [Proveedor de soluciones en la nube de Microsoft](https://partnercenter.microsoft.com/partner/programs), Office 365 Syndication o Microsoft Advisor. <br/><br/>Para obtener más información sobre cómo administrar los datos de los clientes a través de Microsoft Graph como un proveedor de soluciones en la nube, consulte [Llamar a Microsoft Graph desde una aplicación del proveedor de soluciones en la nube](../../../concepts/auth_cloudsolutionprovider.md). |
| Administrar dominios asociados a un inquilino. Las operaciones de dominio permiten a los registradores automatizar la asociación de dominio para servicios como Office 365. | [domain](../resources/domain.md) | Para obtener más información, consulte [Adición de un nombre de dominio personalizado a la versión preliminar de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-domains-add-azure-portal). |
| **Administración de inquilinos** | | |
| Obtenga información sobre una organización; por ejemplo, su dirección comercial, los contactos técnicos y de notificación, los planes de servicio a los que está suscrita y los dominios asociados a ella. | [organization](../resources/organization.md) | N/D |
| Obtenga información sobre las SKU de servicio a las que está suscrita una empresa. | [subscribedSku](../resources/subscribedsku.md) | N/D |
| Invite a usuarios externos (invitados) a una organización. | [invitation](../resources/invitation.md) | Para obtener más información, consulte [¿Qué es la colaboración B2B de Azure AD?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b). |



## <a name="next-steps"></a>Pasos siguientes
Las API y los recursos de directorio pueden proporcionar nuevas formas de comunicarse con los usuarios y administrar sus experiencias con Microsoft Graph: 

- Explore en profundidad los métodos y las propiedades de los recursos más útiles para su escenario.
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).


