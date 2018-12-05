---
title: Información general sobre API de Administración de identidad y acceso de Azure AD
description: 'Azure Active Directory (Azure AD) ayuda a centralizar la administración de identidad y acceso (IAM) para permitir el acceso seguro y productivo entre dispositivos, aplicaciones, servicios e infraestructura. Las organizaciones pueden usar Azure AD para administrar las identidades y controlar el acceso en entornos locales, de nube e híbridos.  '
ms.openlocfilehash: f933e47f890f228865968d47040fdb1316607692
ms.sourcegitcommit: 4a46cfd112c8089fc07e4e5ccdccaf415a3a0e7f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2018
ms.locfileid: "27156050"
---
# <a name="azure-ad-identity-and-access-management-api-overview"></a>Información general sobre API de Administración de identidad y acceso de Azure AD

Azure Active Directory (Azure AD) ayuda a centralizar la administración de identidad y acceso (IAM) para permitir el acceso seguro y productivo entre dispositivos, aplicaciones, servicios e infraestructura. Las organizaciones pueden usar Azure AD para administrar las identidades y controlar el acceso en entornos locales, de nube e híbridos.  

Puede usar la API de REST de Azure AD de Microsoft Graph para crear flujos de trabajo únicos entre [recursos](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0) de Azure AD y servicios de terceros.

## <a name="why-use-the-azure-ad-apis"></a>¿Por qué debería usar las API de Azure AD?

Más de 15 millones de organizaciones usan Azure AD al suscribirse a los Servicios en la nube de Microsoft como Office 365, Microsoft Azure, Enterprise Mobility Suite o Microsoft 365.  

Los desarrolladores empresariales utilizan Microsoft Graph para integrar la administración de identidades de Azure AD y otros servicios para automatizar los flujos de trabajo administrativos, como la incorporación (y eliminación) de empleados, el mantenimiento del perfiles, la implementación de licencias y mucho más.

Para muchos desarrolladores empresariales, Microsoft Graph y Azure AD ayudan a migrar mediante lift-and-shift aplicaciones existentes a la nube, lo que acelera la transformación digital de una organización. Puede aprovechar las ventajas de las funciones de Azure AD para agregar mecanismos de control de acceso a aplicaciones, como comprobar la pertenencia de un usuario a un grupo, el rol de directorio o la pertenencia a la unidad administrativa.

Puede usar Microsoft Graph y Azure AD como una forma de llegar rápida y fácilmente a más de 15 millones de organizaciones, incluyendo el 90 % de las empresas del Fortune 500 que ya usan servicios de Azure AD. Las aplicaciones integradas cuentan con experiencias de inicio de sesión directa y pueden usar los datos existentes de la organización para crear experiencias personalizadas.  

Puede usar la API de Azure AD de Microsoft Graph para consultar el perfil de usuario, buscar otros usuarios, administrar relaciones de la organización, realizar un seguimiento de tareas o crear soluciones originales que incorporan datos de la organización existentes. Estas API ofrecen una base sólida para integrar perfectamente aplicaciones empresariales personalizadas en los servicios digitales existentes de una organización.

### <a name="access-users-and-groups"></a>Acceder a usuarios y grupos

Puede usar las API de Azure AD de Microsoft Graph para:

- Buscar y administrar información de los [perfiles de los usuarios](/graph/api/resources/user?view=graph-rest-1.0) de su organización, como el nombre, la foto, la dirección de correo electrónico, el puesto, la ubicación de la oficina y mucho más.
- Crear [grupos](/graph/api/resources/groups-overview?view=graph-rest-1.0) para proyectos y equipos de su organización. Agregar miembros a un grupo y quitarlos para controlar el acceso a los recursos. (Los grupos dinámicos pueden cambiar automáticamente la pertenencia basándose en valores de propiedad de usuario).
- Para controlar el acceso, puede buscar la [pertenencia transitiva](/graph/api/user-checkmembergroups?view=graph-rest-1.0) en una lista de grupos u obtener todos los recursos de un tipo específico (como un usuario o grupo) de una lista de [identificadores de recursos genéricos](/graph/api/directoryobject-getbyids?view=graph-rest-1.0).

### <a name="manage-directory-roles"></a>Administrar roles de directorio

Puede asignar usuarios a [roles de directorio](/graph/api/resources/directoryrole?view=graph-rest-1.0) administrativos de Azure AD predefinidos, que concede permiso para realizar tareas específicas.

### <a name="manage-devices"></a>Administrar dispositivos

[Administre los dispositivos](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction) registrados en la organización. Los dispositivos se registran en usuarios e incluyen elementos como portátiles, equipos de escritorio, tabletas y teléfonos móviles. Los dispositivos suelen crearse en la nube con el servicio de registro de dispositivos o Microsoft Intune. Las directivas de acceso condicional los usan para la autenticación multifactor.

### <a name="partner-tenant-management"></a>Administración de inquilinos de partners

Los partners de Microsoft que distribuyen y administran Microsoft Online Services (como Office 365, Microsoft Azure y CRM Online) pueden ver los [inquilinos organización](/graph/api/resources/contract?view=graph-rest-1.0) que administran actualmente.

También puede [administrar dominios](/graph/api/resources/domain?view=graph-rest-1.0) asociados a un inquilino. Las operaciones de dominio permiten a los partners de Microsoft automatizar el registro de dominios para servicios como Office 365.

### <a name="tenant-management"></a>Administración de inquilinos

Las API de Azure AD para la administración de inquilinos permiten:

- Obtener información sobre una [organización](/graph/api/resources/organization?view=graph-rest-1.0), como su dirección comercial, los contactos técnicos y de notificaciones, las suscripciones de servicio activas y los dominios asociados a esta.
- Obtener información sobre las [SKU de servicio](/graph/api/resources/subscribedsku?view=graph-rest-1.0) a las que está suscrita una empresa.
- [Invitar a usuarios externos](/graph/api/resources/invitation?view=graph-rest-1.0) (invitados) a una organización.

### <a name="monitor-identity-risks-preview"></a>Supervisar los riesgos de identidad (vista previa)

La mayoría de las infracciones de seguridad son el resultado de que los atacantes roben la identidad del usuario, y se han vuelto terriblemente eficaces a la hora de aprovechar las infracciones de terceros y realizar ataques de difusión contraseña y ataques de suplantación sofisticados. Esto significa que debe proteger todas las cuentas de usuario de estos ataques e impedir proactivamente que se aprovechen las identidades en peligro.

Azure AD usa algoritmos de aprendizaje automático adaptable y heurística para detectar anomalías que indican cuentas potencialmente en peligro. Con estos datos, protección de la identidad de Azure AD protege a los usuarios con las directivas de acceso condicional basado en riesgo y genera informes y alertas en sus detecciones.

En la actualidad, Microsoft Graph ofrece acceso fácil a los clientes de Azure AD Premium P2 a [eventos de riesgo de consulta detectados por la protección de la identidad](/graph/api/resources/identityprotection-root?view=graph-rest-beta), incluidos el evento de riesgo tipo, gravedad, fecha, hora, ubicación, usuario afectado y mucho más. Los clientes pueden usar a continuación, los eventos en las aplicaciones de seguridad y sistemas SIEM.

### <a name="activate-users-into-privileged-roles-preview"></a>Activar usuarios con roles con privilegios (versión preliminar)

Puede obtener acceso seguro a los recursos mediante la activación bajo petición de los privilegios administrativos. [Privileged Identity Management](/graph/api/resources/privilegedidentitymanagement-root?view=graph-rest-beta) está incluido en Azure AD Premium P2.

### <a name="manage-user-access-reviews-preview"></a>Administrar las revisiones de acceso de usuario (vista previa)

Puede configurar acceso revisiones de pertenencias a grupos y el acceso de la aplicación. [Access revisa](/graph/api/resources/accessreviews-root?view=graph-rest-beta) es destacados en Azure AD Premium P2.

## <a name="api-reference"></a>Referencia de la API

¿Busca la referencia de API para este servicio?

- [Azure AD acceso a administración de identidades y API en Microsoft Graph v1.0](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0)
- [Azure AD acceso a administración de identidades y API en la versión beta de Microsoft Graph](/graph/api/resources/azure-ad-overview?view=graph-rest-beta)

## <a name="next-steps"></a>Siguientes pasos

- Descubra cómo [Usar la API de REST de Azure AD](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0).
- Usar Azure AD para [autenticar](auth-overview.md) en Microsoft Graph.
- Integrar el [inicio de sesión de Azure AD](https://azure.microsoft.com/en-us/develop/identity/signin/) en su aplicación o sitio web.
- Consulte el [registro de cambios](changelog.md) para obtener información sobre las novedades de la API de Azure AD.
- Explore los [ejemplos](https://developer.microsoft.com/graph/graph/examples) para obtener más ideas sobre cómo usar Microsoft Graph.
