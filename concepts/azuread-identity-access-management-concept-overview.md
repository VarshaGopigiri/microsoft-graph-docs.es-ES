# <a name="azure-ad-identity-and-access-management-api-overview"></a>Información general sobre API de Administración de identidad y acceso de Azure AD

Azure Active Directory (Azure AD) ayuda a centralizar la administración de identidad y acceso (IAM) para permitir el acceso seguro y productivo entre dispositivos, aplicaciones, servicios e infraestructura. Las organizaciones pueden usar Azure AD para administrar las identidades y controlar el acceso en entornos locales, de nube e híbridos.  

Puede usar la API de REST de Azure AD de Microsoft Graph para crear flujos de trabajo únicos entre [recursos](../api-reference/v1.0/resources/azure_ad_overview.md) de Azure AD y servicios de terceros.

## <a name="why-use-the-azure-ad-apis"></a>¿Por qué debería usar las API de Azure AD?

Más de 15 millones de organizaciones usan Azure AD al suscribirse a los Servicios en la nube de Microsoft como Office 365, Microsoft Azure, Enterprise Mobility Suite o Microsoft 365.  

Los desarrolladores empresariales utilizan Microsoft Graph para integrar la administración de identidades de Azure AD y otros servicios para automatizar los flujos de trabajo administrativos, como la incorporación (y eliminación) de empleados, el mantenimiento del perfiles, la implementación de licencias y mucho más.

Para muchos desarrolladores empresariales, Microsoft Graph y Azure AD ayudan a migrar mediante lift-and-shift aplicaciones existentes a la nube, lo que acelera la transformación digital de una organización. Puede aprovechar las ventajas de las funciones de Azure AD para agregar mecanismos de control de acceso a aplicaciones, como comprobar la pertenencia de un usuario a un grupo, el rol de directorio o la pertenencia a la unidad administrativa.

Puede usar Microsoft Graph y Azure AD como una forma de llegar rápida y fácilmente a más de 15 millones de organizaciones, incluyendo el 90 % de las empresas del Fortune 500 que ya usan servicios de Azure AD. Las aplicaciones integradas cuentan con experiencias de inicio de sesión directa y pueden usar los datos existentes de la organización para crear experiencias personalizadas.  

Puede usar la API de Azure AD de Microsoft Graph para consultar el perfil de usuario, buscar otros usuarios, administrar relaciones de la organización, realizar un seguimiento de tareas o crear soluciones originales que incorporan datos de la organización existentes. Estas API ofrecen una base sólida para integrar perfectamente aplicaciones empresariales personalizadas en los servicios digitales existentes de una organización.

### <a name="access-users-and-groups"></a>Acceder a usuarios y grupos

Puede usar las API de Azure AD de Microsoft Graph para:

- Buscar y administrar información de los [perfiles de los usuarios](../api-reference/v1.0/resources/user.md) de su organización, como el nombre, la foto, la dirección de correo electrónico, el puesto, la ubicación de la oficina y mucho más.
- Crear [grupos](../api-reference/v1.0/resources/groups-overview.md) para proyectos y equipos de su organización. Agregar miembros a un grupo y quitarlos para controlar el acceso a los recursos. (Los grupos dinámicos pueden cambiar automáticamente la pertenencia basándose en valores de propiedad de usuario).
- Para controlar el acceso, puede buscar la [pertenencia transitiva](../api-reference/v1.0/api/user_checkmembergroups.md) en una lista de grupos u obtener todos los recursos de un tipo específico (como un usuario o grupo) de una lista de [identificadores de recursos genéricos](../api-reference/v1.0/api/directoryobject_getbyids.md).

### <a name="manage-directory-roles"></a>Administrar roles de directorio

Puede asignar usuarios a [roles de directorio](../api-reference/v1.0/resources/directoryrole.md) administrativos de Azure AD predefinidos, que concede permiso para realizar tareas específicas.

### <a name="manage-devices"></a>Administrar dispositivos

[Administre los dispositivos](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction.md) registrados en la organización. Los dispositivos se registran en usuarios e incluyen elementos como portátiles, equipos de escritorio, tabletas y teléfonos móviles. Los dispositivos suelen crearse en la nube con el servicio de registro de dispositivos o Microsoft Intune. Las directivas de acceso condicional los usan para la autenticación multifactor.

### <a name="partner-tenant-management"></a>Administración de inquilinos de partners

Los partners de Microsoft que distribuyen y administran Microsoft Online Services (como Office 365, Microsoft Azure y CRM Online) pueden ver los [inquilinos organización](../api-reference/v1.0/resources/contract.md) que administran actualmente.

También puede [administrar dominios](../api-reference/v1.0/resources/domain.md) asociados a un inquilino. Las operaciones de dominio permiten a los partners de Microsoft automatizar el registro de dominios para servicios como Office 365.

### <a name="tenant-management"></a>Administración de inquilinos

Las API de Azure AD para la administración de inquilinos permiten:

- Obtener información sobre una [organización](../api-reference/v1.0/resources/organization.md), como su dirección comercial, los contactos técnicos y de notificaciones, las suscripciones de servicio activas y los dominios asociados a esta.
- Obtener información sobre las [SKU de servicio](../api-reference/v1.0/resources/subscribedsku.md) a las que está suscrita una empresa.
- [Invitar a usuarios externos](../api-reference/v1.0/resources/invitation.md) (invitados) a una organización.

### <a name="monitor-identity-protection-risks-preview"></a>Supervisar los riesgos con Identity Protection (versión preliminar)

Puede recuperar eventos de riesgo generados mediante Azure AD [Identity Protection](../api-reference/beta/resources/identityprotection_root.md), incluidos el tipo de evento de riesgo, la gravedad, la fecha, la hora, la ubicación, el usuario afectado y mucho más. Identity Protection está incluido en Azure AD Premium P2.

### <a name="activate-users-into-privileged-roles-preview"></a>Activar usuarios con roles con privilegios (versión preliminar)

Puede obtener acceso seguro a los recursos mediante la activación bajo petición de los privilegios administrativos. [Privileged Identity Management](../api-reference/beta/resources/privilegedidentitymanagement_root.md) está incluido en Azure AD Premium P2.

### <a name="manage-user-access-reviews-preview"></a>Administrar las revisiones de acceso de usuario (vista previa)

Puede configurar revisiones de acceso de pertenencias a grupos y acceso a aplicaciones. Las [revisiones de acceso](../api-reference/beta/resources/accessreviews_root.md) está incluido en Azure AD Premium P2.

## <a name="next-steps"></a>Pasos siguientes

- Descubra cómo [Usar la API de REST de Azure AD](../api-reference/v1.0/resources/azure_ad_overview.md).
- Usar Azure AD para [autenticar](auth_overview.md) en Microsoft Graph. 
- Integrar el [inicio de sesión de Azure AD](https://azure.microsoft.com/en-us/develop/identity/signin/) en su aplicación o sitio web.
- Consulte el [registro de cambios](changelog.md) para obtener información sobre las novedades de la API de Azure AD.
- Explore los [ejemplos](https://developer.microsoft.com/en-us/graph/graph/examples) para obtener más ideas sobre cómo usar Microsoft Graph.
