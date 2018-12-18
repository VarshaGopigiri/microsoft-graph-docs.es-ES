---
title: Trabajar con recursos de Azure Active Directory en Microsoft Graph
description: Microsoft Graph para Azure Active Directory (AD Azure) proporciona la API de REST para ayudar a administrar su organización, recursos y activos.
ms.openlocfilehash: 85f44df36057220e4ea26eb8d9342e9fd1df5bb6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305386"
---
# <a name="working-with-azure-active-directory-resources-in-microsoft-graph"></a>Trabajar con recursos de Azure Active Directory en Microsoft Graph

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Con Microsoft Graph, puede tener acceso a recursos de [Azure Active Directory (AD Azure)](https://docs.microsoft.com/azure/active-directory/active-directory-whatis) para habilitar escenarios como la administración de roles de administrador (directorio), invitar a los usuarios externos a una organización, y, si es un [Proveedor de soluciones de la nube (CSP)](https://partner.microsoft.com/cloud-solution-provider), administración de datos de su cliente. Microsoft Graph proporciona también pueden usar métodos aplicaciones, por ejemplo, para detectar información acerca de la pertenencia transitiva grupos y roles de los usuarios. 

> **Nota**: Algunos recursos de Azure AD se documentan en otras secciones de la referencia de la API. Para obtener más información, vea [Usuarios](users.md) y [Grupos](group.md).


## <a name="authorization"></a>Autorización
 
Para llamar a las API de Microsoft Graph en recursos de Azure AD, la aplicación necesitará los permisos adecuados. Muchas de las API expuestas en recursos de Azure AD necesitan uno de los [permisos de _directorio_](/graph/permissions-reference#directory-permissions). Los permisos de directorio tienen privilegios muy elevados y siempre necesitan el consentimiento del administrador. 

Si la aplicación actúa en nombre de un usuario (permisos delegados), puede que este tenga que ser miembro de un [rol de administrador](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) adecuado para que la aplicación pueda llamar correctamente a muchas de las API de Azure AD.

Para obtener más información sobre permisos, incluidos permisos delegados y de aplicación, vea [Permisos](/graph/permissions-reference). 

## <a name="common-use-cases"></a>Casos de uso común 

En la tabla siguiente se muestran algunos de los casos de uso comunes para recursos de Azure AD.

| **Casos de uso**        | **Recursos de REST** | **Ver también** |
|:-----------------|:--------|:----------|
| **Objeto y métodos de directorio** | | |
| `directoryObject` es la clase base de la que heredan muchos de los recursos de directorio (por ejemplo, usuarios y grupos). Microsoft Graph expone varios métodos que puede usar para descubrir información sobre usuarios, grupos y otros objetos de directorio. Por ejemplo, puede comprobar la pertenencia transitiva en una lista de grupos, devolver todos los grupos y roles de directorio de los que es miembro transitivo un objeto de directorio u obtener todos los recursos de un tipo especificado (por ejemplo, usuario o grupo) de una lista de identificadores de recursos genéricos. | [directoryObject](../resources/directoryobject.md) | N/D |
| **Administrar roles de Active directory (Administrador), unidades administrativas, configuración de Active directory y directiva** | | |
| Active roles de directorio en un inquilino de Azure AD y administre las pertenencias de usuario en los roles de directorio. Los roles de directorio también se conocen como roles de administrador. | [directoryRole](../resources/directoryrole.md) <br/>[directoryRoleTemplate](../resources/directoryroletemplate.md) |[Asignar roles de administrador en Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)|
| Administrar unidades administrativas. Roles de Active Directory delegación la autoridad de todo el inquilino a sus miembros. Un administrador puede crear y administrar unidades administrativas para delegar la autoridad administrativa con ámbito de forma más granular a los usuarios. | [administrativeUnit](../resources/administrativeunit.md) | [Administración de unidades administrativas en Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administrative-units-management) |
| Aplicar la configuración de Active directory predefinidos a través de un inquilino o a instancias de recursos individuales. Actualmente, se admite sólo la configuración para los grupos de Office 365. Comportamientos de control de configuración de Active Directory, como las listas de word bloqueados para nombres de grupo para mostrar, si los usuarios invitados pueden ser propietarios del grupo y mucho más. | [Establecer](../resources/directorysetting.md) <br/>[directorySettingTemplate](../resources/directorysettingtemplate.md)| [Cmdlets de Azure Active Directory para configurar configuraciones de grupo](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-groups-settings-cmdlets)|
| Aplicar directivas de Azure AD a aplicaciones, entidades de seguridad de servicio, grupos o toda la organización. Actualmente, se admiten las directivas para la detección de dominio de inicio y la duración del token.  | [Directiva](../resources/policy.md) | N/D |
| **Acceso con privilegios seguro a Azure AD** | | |
| Administrar y supervisar el límite de tiempo de acceso con privilegios a Active directory y recursos de Azure para los administradores y profesionales de TI con la administración de identidad con privilegios (PIM). | [API de administración de identidad con privilegios](../resources/privilegedidentitymanagement-root.md) | [¿Qué es la administración de identidades AD con privilegios de Azure?](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)|
| Supervisar eventos de riesgo de identidad, como los usuarios iniciar sesión desde dispositivos infectados con malware o desde ubicaciones no están familiarizadas. | [API de servicio de protección de identidad](../resources/identityprotection-root.md) | [Protección de identidad de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection)<br/><br/>[Eventos de riesgo de Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-risk-events) |
| **Administrar dispositivos** | | |
| Administre los dispositivos registrados en la organización. Los dispositivos se registran en usuarios e incluyen elementos como portátiles, equipos de escritorio, tabletas y teléfonos móviles. Los dispositivos suelen crearse en la nube con el servicio de registro de dispositivos o Microsoft Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. | [device](../resources/device.md) | [Introducción al registro de dispositivo de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-device-registration-overview)<br/><br/>[¿Qué es Intune?](https://docs.microsoft.com/intune-classic/understand-explore/introduction-to-microsoft-intune)<br/><br/>[Inscribir dispositivos para administrarlos en Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune) |
| **Administración de aplicaciones** | | |
| Administrar la configuración de la aplicación en un inquilino de desarrollador. | [application](../resources/application.md) | [Aplicación y objetos de entidad de seguridad de servicio en Active Directory de Azure](https://docs.microsoft.com/azure/active-directory/develop/active-directory-application-objects) |
| Administrar las aplicaciones que se instalan en un inquilino. | [servicePrinicpal](../resources/serviceprincipal.md) | [Aplicación y objetos de entidad de seguridad de servicio en Active Directory de Azure](https://docs.microsoft.com/azure/active-directory/develop/active-directory-application-objects) |
| Administrar permisos aceptado por los usuarios y administradores en aplicaciones que se instalan en un inquilino. | [oAuth2PermissionGrant](../resources/oauth2permissiongrant.md) | N/D |
| Administrar usuarios, grupos y pertenencias de rol entidad de seguridad de servicio en aplicaciones que se instalan en un inquilino. | [appRoleAssignment](../resources/approleassignment.md) | N/D |
| **Administración de inquilinos asociados** | | |
| Obtenga información sobre las asociaciones con inquilinos de clientes. <br/><br/>**Nota**: Esto solo es válido para inquilinos asociados. Los inquilinos asociados son inquilinos de Azure AD que pertenecen a los socios de Microsoft, que forman parte de los programas [Proveedor de soluciones en la nube de Microsoft](https://partnercenter.microsoft.com/partner/programs), Office 365 Syndication o Microsoft Advisor.| [contract](../resources/contract.md) | [Llamar a Microsoft Graph desde una aplicación del proveedor de soluciones en la nube](/graph/auth-cloudsolutionprovider) |
| Administrar dominios asociados a un inquilino. Las operaciones de dominio permiten a los registradores automatizar la asociación de dominio para servicios como Office 365. | [domain](../resources/domain.md) | [Agregar un nombre de dominio personalizado a Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-domains-add-azure-portal) |
| **Administración de inquilinos** | | |
| Obtenga información sobre una organización, como su dirección comercial, los contactos técnicos y de notificaciones, los planes de servicio a los que está suscrita y los dominios asociados a esta. | [organization](../resources/organization.md) | N/D |
| Obtenga información sobre las SKU de servicio a las que está suscrita una empresa. | [subscribedSku](../resources/subscribedsku.md) | N/D |
| Invite a usuarios externos (invitados) a una organización. | [invitation](../resources/invitation.md) | [¿Qué es la colaboración B2B de Azure AD?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b)|
| **Revisiones de Access** | | |
| Asegúrese de que las pertenencias a grupos y derechos de acceso de la aplicación son correctos con las revisiones de access | [Access revisa API](../resources/accessreviews-root.md) |[Revisa el acceso de Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-access-reviews-overview) |
## <a name="next-steps"></a>Siguientes pasos
Las API y los recursos de directorio pueden proporcionar nuevas formas de comunicarse con los usuarios y administrar sus experiencias con Microsoft Graph. Para obtener más información: 

- Explore en profundidad los métodos y las propiedades de los recursos más útiles para su escenario.
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).

