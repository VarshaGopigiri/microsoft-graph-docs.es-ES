# <a name="microsoft-graph-permissions-reference"></a>Referencia de permisos de Microsoft Graph 
Microsoft Graph expone permisos pormenorizados que controlan el acceso que las aplicaciones tienen a recursos como usuarios, grupos y correo. Como desarrollador, usted decide qué permisos de Microsoft Graph solicita la aplicación. Cuando un usuario inicia sesión en su aplicación, se le ofrece la opción (o, en algunos casos, a un administrador) de dar su consentimiento a estos permisos. Si el usuario consiente, la aplicación tiene acceso a los recursos y las API que ha solicitado. En el caso de las aplicaciones que no requieren que un usuario haya iniciado sesión, un administrador puede dar su consentimiento previo a los permisos al instalar la aplicación o durante el registro. 

## <a name="delegated-permissions-application-permissions-and-effective-permissions"></a>Permisos delegados, permisos de la aplicación y permisos efectivos
Microsoft Graph tiene dos tipos de permisos: **permisos delegados** y **permisos de la aplicación**. 

- Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión. En estas aplicaciones, el usuario o un administrador dan su consentimiento a los permisos que solicita la aplicación, y se delega permiso a la aplicación para que actúe como usuario que ha iniciado sesión cuando se hacen llamadas a Microsoft Graph. En ocasiones, los usuarios no administrativos pueden recibir permisos delegados, pero existen permisos con privilegios mayores que requieren el [consentimiento del administrador](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-scopes#admin-restricted-scopes).  

- Los **permisos de la aplicación** son los que usan las aplicaciones que se ejecutan sin que un usuario haya iniciado sesión, como las aplicaciones que se ejecutan como servicios en segundo plano o demonios.  Solo un administrador puede dar su [consentimiento a los permisos de la aplicación](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-scopes#requesting-consent-for-an-entire-tenant). 

Los _permisos efectivos_ son los permisos que tendrá la aplicación al realizar solicitudes a Microsoft Graph. Es importante comprender la diferencia entre los permisos delegados y de aplicación concedidos a la aplicación y sus permisos efectivos al realizar llamadas a Microsoft Graph.

- En el caso de los permisos delegados, los _permisos efectivos_ de la aplicación serán la intersección menos privilegiada de los permisos delegados concedidos a la aplicación (a través del consentimiento) y los privilegios del usuario que ha iniciado sesión. La aplicación nunca puede tener más privilegios que el usuario que ha iniciado sesión. Dentro de las organizaciones, los privilegios del usuario que ha iniciado sesión se pueden determinar mediante directiva o mediante la pertenencia a uno o más roles de administrador. Para obtener más información sobre los roles de administrador, vea [Asignación de roles de administrador en Azure Active Directory]((https://docs.microsoft.com/es-ES/azure/active-directory/active-directory-assign-admin-roles)).<br/><br/>Por ejemplo, supongamos que se le ha concedido a la aplicación el permiso delegado _User.ReadWrite.All_. En teoría, este permiso concede a la aplicación el permiso de leer y actualizar el perfil de todos los usuarios de una organización. Si el usuario que ha iniciado sesión es un administrador global, la aplicación podrá actualizar el perfil de cada usuario de la organización. Pero si el usuario que ha iniciado sesión no está incluido en un rol de administrador, la aplicación solo podrá actualizar el perfil del usuario que ha iniciado sesión. No podrá actualizar los perfiles de otros usuarios de la organización, ya que el usuario en cuyo nombre tiene permiso para actuar no cuenta con esos privilegios.
  
- En el caso de los permisos de aplicación, los _permisos efectivos_ de la aplicación serán el nivel completo de privilegios que conlleva el permiso. Por ejemplo, una aplicación que tiene el permiso de aplicación _User.ReadWrite.All_ puede actualizar el perfil de todos los usuarios de la organización. 

### <a name="microsoft-graph-permission-names"></a>Nombres de permisos de Microsoft Graph
Los nombres de permisos de Microsoft Graph siguen un patrón sencillo: _recurso.operación.restricción_. Por ejemplo, _User.Read_ concede el permiso de leer el perfil del usuario que ha iniciado sesión, _User.ReadWrite_ concede el permiso de leer y modificar el perfil del usuario que ha iniciado sesión, y _Mail.Send_ concede el permiso de enviar correo en nombre del usuario que ha iniciado sesión. 

El elemento _restricción_ del nombre determina el posible alcance del acceso que tendrá la aplicación dentro del directorio. Actualmente, Microsoft Graph admite las siguientes restricciones: 

* **All** concede permiso a la aplicación para realizar las operaciones en todos los recursos del tipo especificado en un directorio. Por ejemplo, _User.Read.All_ concede potencialmente a la aplicación privilegios para leer los perfiles de todos los usuarios de un directorio. 
* **Shared** concede permiso a la aplicación para realizar las operaciones en los recursos que otros usuarios han compartido con el usuario que ha iniciado sesión. Esta restricción se usa principalmente con recursos de Outlook, como correo, calendarios y contactos. Por ejemplo, _Mail.Read.Shared_ concede privilegios para leer el correo del buzón del usuario que ha iniciado sesión y el correo de los buzones que otros usuarios de la organización han compartido con el usuario que ha iniciado sesión.
* **AppFolder** concede permiso a la aplicación para leer y escribir archivos en una carpeta dedicada en OneDrive. Esta restricción solo se expone en [Permisos de archivos](#files-permissions) y solo es válida para cuentas de Microsoft.
* Si no se especifica **ninguna restricción**, la aplicación se limita a realizar las operaciones en los recursos que posee el usuario que ha iniciado sesión. Por ejemplo, _User.Read_ concede privilegios para leer el perfil únicamente del usuario que ha iniciado sesión, y _Mail.Read_ concede permiso para leer únicamente el correo del buzón del usuario que ha iniciado sesión.

> **Nota**: En escenarios delegados, los permisos efectivos concedidos a la aplicación pueden verse limitados por los privilegios en la organización del usuario que ha iniciado sesión.

### <a name="microsoft-accounts-and-work-or-school-accounts"></a>Cuentas de Microsoft y cuentas profesionales o educativas

No todos los permisos son válidos para las cuentas de Microsoft y para las cuentas profesionales o educativas. Consulte los **comentarios** de cada grupo de permisos para determinar si un permiso concreto es válido para las cuentas de Microsoft, para las cuentas profesionales o educativas, o para ambas. 

### <a name="user-and-group-search-limitations-for-guest-users-in-organizations"></a>Limitaciones de búsqueda de usuarios y grupos para usuarios invitados en las organizaciones

Las funciones de búsqueda de grupos y usuarios permiten que la aplicación busque cualquier usuario o grupo en un directorio de la organización mediante la realización de consultas en el conjunto de recursos `/users` o `/groups` (por ejemplo, `https://graph.microsoft.com/v1.0/users`). Los administradores y los usuarios puede realizar esta función, pero los usuarios invitados no. 

Si el usuario que ha iniciado sesión es un usuario invitado, en función de los permisos que se hayan concedido a una aplicación, puede leer el perfil de un usuario o grupo específico (por ejemplo, `https://graph.microsoft.com/v1.0/users/241f22af-f634-44c0-9a15-c8cd2cea5531`), pero no puede realizar consultas en el conjunto de recursos `/users` o `/groups` que devuelvan potencialmente más de un solo recurso. 

Con los permisos adecuados, la aplicación puede leer los perfiles de usuarios o grupos que obtiene al seguir los vínculos de las propiedades de navegación, como `/users/{id}/directReports` o `/groups/{id}/members`.


## <a name="calendars-permissions"></a>Permisos de calendarios

#### <a name="delegated-permissions"></a>Permisos delegados

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Calendars.Read_ |Leer los calendarios del usuario |Permite que la aplicación lea los eventos en los calendarios del usuario. |No |
| _Calendars.Read.Shared_ |Leer los calendarios del usuario y los calendarios compartidos |Permite que la aplicación lea los eventos en todos los calendarios a los que tiene acceso el usuario, incluidos los calendarios delegados y compartidos. |No |
| _Calendars.ReadWrite_ |Obtener acceso completo a los calendarios del usuario |Permite que la aplicación cree, lea, actualice y elimine eventos de los calendarios del usuario. |No |
| _Calendars.ReadWrite.Shared_ |Leer y escribir los calendarios del usuario y los calendarios compartidos |Permite que la aplicación cree, lea, actualice y elimine eventos en todos los calendarios para los que el usuario tiene permisos de acceso. Esto incluye los calendarios de delegado y los calendarios compartidos.|No |

<br/>

#### <a name="application-permissions"></a>Permisos de la aplicación

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
|_Calendars.Read_ |Leer los calendarios de todos los buzones |Permite que la aplicación lea los eventos de todos los calendarios sin la necesidad de que un usuario haya iniciado sesión. |Sí |
|_Calendars.ReadWrite_ |Leer los calendarios de todos los buzones y escribir en ellos |Permite que la aplicación cree, lea, actualice y elimine eventos en todos los calendarios sin la necesidad de que un usuario haya iniciado sesión. |Sí |

<br/>

### <a name="remarks"></a>Comentarios

_Calendars.Read.Shared_ y _Calendars.ReadWrite.Shared_ solo son válidos para las cuentas profesionales o educativas. Todos los demás permisos son válidos para las cuentas de Microsoft y para las cuentas profesionales o educativas.

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _Calendars.Read_: obtener los eventos del calendario del usuario entre el 23 de abril de 2017 y el 29 de abril de 2017 (`GET /me/calendarView?startDateTime=2017-04-23T00:00:00&endDateTime=2017-04-29T00:00:00`).
* _Calendars.Read.Shared_: buscar horas de reunión en las que todos los asistentes estén disponibles (`POST /users/{id|userPrincipalName}/findMeetingTimes`).
* _Calendars.ReadWrite_: agregar un evento al calendario del usuario (`POST /me/events`).

#### <a name="application"></a>Aplicación

* _Calendars.Read_: buscar eventos en el calendario de una sala de conferencias organizados por bob@contoso.com (`GET /users/{id | userPrincipalName}/events?$filter=organizer/emailAddress/address eq 'bob@contoso.com'`).
* _Calendars.Read_: mostrar todos los eventos del calendario de un usuario para el mes de mayo (`GET /users/{id | userPrincipalName}/calendarView?startDateTime=2017-05-01T00:00:00&endDateTime=2017-06-01T00:00:00`).
* _Calendars.ReadWrite_: agregar un evento al calendario de un usuario para una baja aprobada (`POST /users/{id | userPrincipalName}/events`).
* _Calendars.Send_: enviar un mensaje (`POST /users/{id | userPrincipalName}/sendCalendars`).


Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="contacts-permissions"></a>Permisos de contactos

#### <a name="delegated-permissions"></a>Permisos delegados

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
|_Contacts.Read_ |Leer los contactos del usuario  |Permite que la aplicación lea los contactos del usuario. |No |
|_Contacts.Read.Shared_ |Leer los contactos del usuario y los contactos compartidos |Permite que la aplicación lea los contactos para los que el usuario tiene permisos de acceso, incluidos los contactos propios y compartidos del usuario. |No |
|_Contacts.ReadWrite_ |Obtener acceso completo a los contactos del usuario |Permite que la aplicación cree, lea, actualice y elimine los contactos del usuario. |No |
|_Contacts.ReadWrite.Shared_ |Leer y escribir los contactos del usuario y los contactos compartidos |Permite que la aplicación cree, lea, actualice y elimine los contactos para los que el usuario tiene permisos, incluidos los contactos propios y compartidos del usuario. |No |

#### <a name="application-permissions"></a>Permisos de la aplicación

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
|_Contacts.Read_ |Leer los contactos de todos los buzones |Permite que la aplicación lea todos los contactos de todos los buzones sin la necesidad de que un usuario haya iniciado sesión. |Sí |
|_Contacts.ReadWrite_ |Leer y escribir contactos en todos los buzones |Permite que la aplicación cree, lea, actualice y elimine todos los contactos en todos los buzones sin la necesidad de que un usuario haya iniciado sesión. |Sí |

### <a name="remarks"></a>Comentarios
Para las cuentas de Microsoft, solo son válidos los permisos delegados _Contacts.Read_ y _Contacts.ReadWrite_. 

### <a name="example-usage"></a>Ejemplos de uso
#### <a name="delegated"></a>Delegado

* _Contacts.Read_: leer un contacto de una de las carpetas de nivel superior de contactos del usuario que ha iniciado sesión (`GET /me/contactfolders/{Id}/contacts/{id}`).
* _Contacts.ReadWrite_: actualizar la fotografía de contacto de uno de los contactos del usuario que ha iniciado sesión (`PUT /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value`). 
* _Contacts.ReadWrite_: agregar contactos a la carpeta raíz del usuario que ha iniciado sesión (`POST /me/contacts`).

#### <a name="application"></a>Aplicación

* _Contacts.Read_: leer contactos de una de las carpetas de contactos de nivel superior de cualquier usuario de la organización (`GET /users/{id | userPrincipalName}/contactfolders/{Id}/contacts/{id}`). 
* _Contacts.ReadWrite_: actualizar la fotografía de cualquier contacto de cualquier usuario de una organización (`PUT /user/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value`). 
* _Contacts.ReadWrite_: agregar contactos a la carpeta raíz de cualquier usuario de la organización (`POST /users/{id | userPrincipalName}/contacts`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="device-permissions"></a>Permisos de dispositivo

#### <a name="delegated-permissions"></a>Permisos delegados

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
|_Device.Read_ |Leer los dispositivos del usuario |Permite a la aplicación leer la lista de dispositivos de un usuario en nombre del usuario que inició sesión. |No |
|_Device.Command_ |Comunicarse con los dispositivos del usuario |Permite a la aplicación iniciar otra aplicación o comunicarse con otra aplicación del dispositivo de un usuario en nombre del usuario que inició sesión. |No |


#### <a name="application-permissions"></a>Permisos de la aplicación

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
|_Device.ReadWrite.All_ |Leer y escribir dispositivos |Permite que la aplicación lea y escriba todas las propiedades del dispositivo sin la necesidad de que un usuario haya iniciado sesión. No permite la creación de dispositivos, su eliminación o la actualización de identificadores de seguridad alternativos de dispositivos. |Sí |

### <a name="remarks"></a>Comentarios

Los permisos delegados _Device.Read_ y _Device.Command_ solo son válidos para las cuentas personales de Microsoft.

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="application"></a>Aplicación

* _Device.ReadWrite.All_: leer todos los dispositivos registrados de la organización (`GET /devices`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="intune-device-management-permissions"></a>Permisos de la administración de dispositivos de Intune

#### <a name="delegated-permissions"></a>Permisos delegados

|Permiso    |Cadena para mostrar   |Descripción |Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
|_DeviceManagementApps.Read.All_ | Leer aplicaciones de Microsoft Intune | Permite que la aplicación lea las propiedades, asignaciones de grupos y estados de aplicaciones, configuraciones de aplicaciones y directivas de protección de aplicaciones administradas por Microsoft Intune. | Sí |
|_DeviceManagementApps.ReadWrite.All_ | Leer y escribir aplicaciones de Microsoft Intune | Permite que la aplicación lea y escriba las propiedades, asignaciones de grupos y estados de aplicaciones, configuraciones de aplicaciones y directivas de protección de aplicaciones administradas por Microsoft Intune. | Sí |
|_DeviceManagementConfiguration.Read.All_ | Leer las directivas y configuración de dispositivo de Microsoft Intune | Permite que la aplicación lea las propiedades de una configuración de dispositivo administrada por Microsoft Intune y las directivas de cumplimiento de dispositivos y su asignación a grupos. | Sí |
|_DeviceManagementConfiguration.ReadWrite.All_ | Leer y escribir las directivas y configuración de dispositivo de Microsoft Intune  | Permite que la aplicación lea y escriba las propiedades de una configuración de dispositivo administrada por Microsoft Intune y las directivas de cumplimiento de dispositivos y su asignación a grupos. | Sí |
|_DeviceManagementManagedDevices.PrivilegedOperations.All_ | Realizar acciones remotas que repercutan en el usuario en dispositivos de Microsoft Intune | Permite que la aplicación realice acciones de alto impacto remotas como la eliminación remota de datos del dispositivo o restablecer la contraseña en dispositivos administrados por Microsoft Intune. | Sí |
|_DeviceManagementManagedDevices.Read.All_ | Leer dispositivos de Microsoft Intune | Permite que la aplicación lea las propiedades de dispositivos administrados por Microsoft Intune. | Sí |
|_DeviceManagementManagedDevices.ReadWrite.All_ | Leer y escribir dispositivos de Microsoft Intune | Permite que la aplicación lea y escriba las propiedades de dispositivos administrados por Microsoft Intune. No permite operaciones de alto impacto como la eliminación remota y el restablecimiento de contraseña del propietario del dispositivo. | Sí |
|_DeviceManagementRBAC.Read.All_ | Leer la configuración de RBAC de Microsoft Intune | Permite que la aplicación lea las propiedades relacionadas con la configuración del control de acceso basado en roles (RBAC) de Microsoft Intune. | Sí |
|_DeviceManagementRBAC.ReadWrite.All_ | Leer y escribir la configuración de RBAC de Microsoft Intune | Permite que la aplicación lea y escriba las propiedades relacionadas con la configuración del control de acceso basado en roles (RBAC) de Microsoft Intune. | Sí |
|_DeviceManagementServiceConfig.Read.All_ | Leer la configuración de Microsoft Intune | Permite que la aplicación lea las propiedades de servicio de Intune, incluidas la inscripción del dispositivo y la configuración de conexión del servicio de terceros. | Sí |
|_DeviceManagementServiceConfig.ReadWrite.All_ | Leer y escribir la configuración de Microsoft Intune | Permite que la aplicación lea y escriba las propiedades de servicio de Microsoft Intune, incluidas la inscripción del dispositivo y la configuración de conexión del servicio de terceros. | Sí |

#### <a name="application-permissions"></a>Permisos de la aplicación

Ninguno.

### <a name="remarks"></a>Comentarios

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estos permisos solo son válidos para las cuentas profesionales o educativas.

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="application"></a>Aplicación

* _DeviceManagementServiceConfiguration.Read.All_: comprobar el estado actual de la suscripción de Intune (`GET /deviceManagement/subscriptionState`).
* _DeviceManagementServiceConfiguration.ReadWrite.All_: crear términos y condiciones (`POST /deviceManagement/termsAndConditions`).
* _DeviceManagementConfiguration.Read.All_: encontrar el estado de una configuración de dispositivo (`GET /deviceManagement/deviceConfigurations/{id}/deviceStatuses`).
* _DeviceManagementConfiguration.ReadWrite.All_: asignar una directiva de cumplimiento de dispositivos a un grupo (`POST deviceCompliancePolicies/{id}/assign`).
* _DeviceManagementApps.Read.All_: buscar todas las aplicaciones de la Tienda Windows publicadas en Intune (`GET /deviceAppManagement/mobileApps?$filter=isOf('microsoft.graph.windowsStoreApp')`).
* _DeviceManagementApps.ReadWrite.All_: publicar una aplicación nueva (`POST /deviceAppManagement/mobileApps`).
* _DeviceManagementRBAC.Read.All_: buscar una asignación de roles por nombre (`GET /deviceManagement/roleAssignments?$filter=displayName eq 'My Role Assignment'`).
* _DeviceManagementRBAC.ReadWrite.All_: crear un rol personalizado (`POST /deviceManagement/roleDefinitions`).
* _DeviceManagementManagedDevices.Read.All_: buscar un dispositivo administrado por nombre (`GET /managedDevices/?$filter=deviceName eq 'My Device'`).
* _DeviceManagementManagedDevices.ReadWrite.All_: eliminar un dispositivo administrado (`DELETE /managedDevices/{id}`).
* _DeviceManagementManagedDevices.PrivilegedOperations.All_: restablecer el código de acceso del dispositivo administrado de un usuario (`POST /managedDevices/{id}/resetPasscode`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="directory-permissions"></a>Permisos de directorio

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Directory.Read.All_ |Leer datos del directorio | Permite que la aplicación lea los datos del directorio de su organización, como los usuarios, los grupos y las aplicaciones. | Sí |
| _Directory.ReadWrite.All_ |Leer y escribir datos en el directorio | Permite que la aplicación lea y escriba los datos del directorio de su organización, como los usuarios y los grupos. No permite que la aplicación elimine usuarios o grupos ni que restablezca contraseñas de usuario. | Sí |
| _Directory.AccessAsUser.All_ |Obtener acceso al directorio como usuario que ha iniciado sesión  | Permite que la aplicación tenga el mismo acceso a la información del directorio que el usuario que ha iniciado sesión. | Sí |

<br/>

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Directory.Read.All_ | Leer datos del directorio | Permite que la aplicación lea los datos del directorio de su organización, como los usuarios, los grupos y las aplicaciones sin iniciar sesión con ningún usuario. | Sí |
| _Directory.ReadWrite.All_ | Leer y escribir datos en el directorio | Permite que la aplicación lea y escriba los datos del directorio de su organización, como los usuarios y los grupos sin iniciar sesión con ningún usuario. No se permite la eliminación de un usuario o un grupo. | Sí |

### <a name="remarks"></a>Comentarios
No se admiten permisos de directorio en las cuentas de Microsoft. 

Los permisos de directorio proporcionan el mayor nivel de privilegio para obtener acceso a los recursos del directorio, como el [usuario](../api-reference/v1.0/resources/user.md), el [grupo](../api-reference/v1.0/resources/group.md) y el [dispositivo](../api-reference/v1.0/resources/device.md) de una organización. 

También controlan de manera exclusiva el acceso a otros recursos del directorio, como los [contactos de la organización](../api-reference/beta/resources/orgcontact.md), las [API de extensión de esquema](../api-reference/beta/resources/schemaextension.md) y las [API de Privileged Identity Management (PIM)](../api-reference/beta/resources/privilegedidentitymanagement_root.md), así como muchos de los recursos y API indicados en el nodo **Azure Active Directory** en la documentación de referencia de la API v1.0 y beta. Entre estos se incluyen las unidades administrativas, los roles de directorio, las configuraciones de directorio, las directivas y mucho más. 

El permiso _Directory.ReadWrite.All_ concede los privilegios siguientes:

- Acceso completo de lectura a todos los recursos del directorio (propiedades declaradas y propiedades de navegación)
- Crear y actualizar usuarios
- Deshabilitar y habilitar usuarios (pero no el administrador de la compañía)
- Establecer un identificador de seguridad alternativo para el usuario (pero no para los administradores)
- Crear y actualizar grupos
- Administrar pertenencias de grupo
- Actualizar el propietario del grupo
- Administrar asignaciones de licencias
- Definir extensiones de esquema en aplicaciones
- **Nota**: No hay permisos para restablecer contraseñas de usuario.
- **Nota**: No hay permisos para eliminar recursos (incluidos usuarios o grupos).
- **Nota**: Se excluye específicamente la posibilidad de crear o actualizar los recursos que no se han enumerado anteriormente. Esto incluye: aplicación, oAauth2Permissiongrant, appRoleAssignment, dispositivo, servicePrincipal, organización, dominios, etc.
 

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado
* _Directory.Read.All_: enumerar todas las unidades administrativas de una organización (`GET /beta/administrativeUnits`).
* _Directory.ReadWrite.All_: agregar miembros a un rol de directorio (`POST /directoryRoles/{id}/members/$ref`).

#### <a name="application"></a>Aplicación
* _Directory.Read.All_: enumerar todas las pertenencias de un usuario, incluidos los roles de directorio y las unidades administrativas (`GET /beta/users/{id}/memberOf`).
* _Directory.Read.All_: enumerar todos los miembros del grupo, incluidas las entidades de servicio (`GET /beta/groups/{id}/members`).
* _Directory.ReadWrite.All_: agregar un propietario a un grupo (`POST /groups/{id}/owners/$ref`).


Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="education-permissions"></a>Permisos para el ámbito educativo

#### <a name="delegated-permissions"></a>Permisos delegados

|Permiso |Cadena para mostrar |Descripción | Se requiere el consentimiento del administrador |
|:--------- |:------------- |:---------- | :--------------------- |
|EduAdministration.Read | Leer configuración de aplicación educativa |  Permite a la aplicación leer la configuración de la aplicación educativa en nombre del usuario. | Sí |
|EduAdministration.ReadWrite | Administrar configuración de aplicación educativa | Permite a la aplicación administrar la configuración de la aplicación educativa en nombre del usuario. | Sí |
|EduAssignments.ReadBasic | Leer las tareas de clase de los usuarios sin calificaciones | Permite a la aplicación leer las tareas sin calificaciones en nombre del usuario | Sí |
|EduAssignments.ReadWriteBasic | Leer y escribir las tareas de clase de los usuarios sin calificaciones | Permite a la aplicación leer y escribir las tareas sin calificaciones en nombre del usuario | Sí |
|EduAssignments.Read | Leer la vista de los usuarios de las tareas de clase y sus calificaciones | Permite a la aplicación leer las tareas y sus calificaciones en nombre del usuario| Sí |
|EduAssignments.ReadWrite | Leer y escribir la vista de los usuarios de las tareas de clase y sus calificaciones | Permite a la aplicación leer y escribir las tareas y sus calificaciones en nombre del usuario|Sí |
|EduRostering.ReadBasic| Leer un subconjunto limitado de la vista de los usuarios de la lista | Permite a la aplicación leer un subconjunto limitado de los datos de la estructura de escuelas y clases en una lista de organización, y leer la información específica de educación sobre los usuarios en nombre del usuario.  | Sí  |


#### <a name="application-permissions"></a>Permisos de la aplicación

| Permiso | Cadena para mostrar | Descripción | Se requiere el consentimiento del administrador |
| :--------- | :------------- | :---------- | :--------------------- |
|EduAssignments.ReadBasic.All| Leer las tareas de clase sin calificaciones|Permite a la aplicación leer las tareas sin calificaciones para todos los usuarios| Sí |
|EduAssignments.ReadWriteBasic.All | Leer y escribir las tareas de clase sin calificaciones | Permite a la aplicación leer y escribir las tareas sin calificaciones para todos los usuarios| Sí |
|EduAssignments.Read.All| Leer las tareas de clase con calificaciones | Permite a la aplicación leer las tareas y sus calificaciones para todos los usuarios | Sí |
|EduAssignments.ReadWrite.All | Leer y escribir las tareas de clase con calificaciones | Permite a la aplicación leer y escribir las tareas y sus calificaciones para todos los usuarios | Sí |
|EduRostering.ReadBasic.All | Leer un subconjunto limitado de la lista de la organización. | Permite a la aplicación leer un subconjunto limitado de los datos de la estructura de escuelas y de clases en una lista de organización, y leer la información específica de educación sobre los usuarios. | Sí |
|EduRostering.Read.All | Lea la lista de la organización. | Permite a la aplicación leer la estructura de escuelas y de clases en una lista de organización, y leer la información específica de educación sobre los usuarios. | Sí |
|EduRostering.ReadWrite.All| Leer y escribir la lista de la organización. | Permite a la aplicación leer y escribir la estructura de escuelas y de clases en una lista de organización, y leer y escribir la información específica de educación sobre los usuarios.  | Sí |

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _EduAssignments.Read_: Obtener información de las tareas del alumno que haya iniciado sesión (`GET /education/classes/<id>/assignments/<id>`)
* _EduAssignments.ReadWriteBasic_: Enviar la tarea del alumno que haya iniciado sesión (`GET /education/classes/<id>/assignments/<id>submit`)
* _EduRoster.ReadBasic_: Clases a las que asiste o en las que enseña un alumno que haya iniciado sesión (`GET /education/classes/<id>/members`)

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

## <a name="files-permissions"></a>Permisos de archivos

#### <a name="delegated-permissions"></a>Permisos delegados

|Permiso |Cadena para mostrar |Descripción | Se requiere el consentimiento del administrador |
|:--------- |:------------- |:---------- | :--------------------- |
| _Files.Read_ | Leer archivos de usuario | Permite a la aplicación leer los archivos del usuario que inició la sesión. | No |
| _Files.Read.All_ | Leer todos los archivos a  los que el usuario puede tener acceso | Permite que la aplicación lea todos archivos a los que puede tener acceso el usuario que ha iniciado sesión. | No |
| _Files.ReadWrite_  | Obtener acceso total a los archivos de usuario | Permite a la aplicación leer, crear, actualizar y eliminar los archivos del usuario que inició la sesión. | No|
| _Files.ReadWrite.All_ | Obtener acceso total a todos los archivos a los que puede tener acceso el usuario | Permite que la aplicación lea, cree, actualice y elimine todos los archivos a los que puede obtener acceso el usuario que inició la sesión. | No |
| _Files.ReadWrite.AppFolder_ | Obtener acceso total a la carpeta de la aplicación (versión preliminar) | (Versión preliminar) Permite que la aplicación lea, cree, actualice y elimine archivos de la carpeta de la aplicación. | No |
| _Files.Read.Selected_  | Leer los archivos que el usuario selecciona | **Compatibilidad limitada en Microsoft Graph (vea los comentarios)** <br/> (Versión preliminar) Permite que la aplicación lea los archivos que el usuario selecciona. La aplicación puede obtener acceso a un archivo durante varias horas después de que el usuario lo haya seleccionado.  | No |
| _Files.ReadWrite.Selected_ | Leer los archivos que el usuario selecciona y escribir en ellos | **Compatibilidad limitada en Microsoft Graph (vea los comentarios)** <br/> (Versión preliminar) Permite que la aplicación lea y escriba archivos que el usuario selecciona. La aplicación puede obtener acceso a un archivo durante varias horas después de que el usuario lo haya seleccionado. | No |

#### <a name="application-permissions"></a>Permisos de la aplicación

| Permiso | Cadena para mostrar | Descripción | Se requiere el consentimiento del administrador |
| :--------- | :------------- | :---------- | :--------------------- |
| _Files.Read.All_ | Leer archivos en todas las colecciones de sitios | Permite que la aplicación lea todos los archivos de todas las colecciones de sitios sin la necesidad de que un usuario haya iniciado sesión.  | Sí |
| _Files.ReadWrite.All_ | Leer y escribir archivos en todas las colecciones de sitios | Permite que la aplicación lea, cree, actualice y elimine todos los archivos de todas las colecciones de sitios sin la necesidad de que un usuario haya iniciado sesión. | Sí |

### <a name="remarks"></a>Comentarios

Los permisos delegados Files.Read, Files.ReadWrite, Files.Read.All y Files.ReadWrite.All son válidos tanto para cuentas Microsoft personales como para cuentas profesionales o educativas. Tenga en cuenta que, para las cuentas personales, Files.Read y Files.ReadWrite también conceden acceso a archivos compartidos con el usuario que inició la sesión. 

Los permisos delegados Files.Read.Selected y Files.ReadWrite.Selected solo son válidos en cuentas profesionales o educativas, y solo se exponen para trabajar con [controladores de archivos de Office 365 (v1.0)]((https://msdn.microsoft.com/office/office365/howto/using-cross-suite-apps)). No tienen que usarse para llamar directamente a las API de Microsoft Graph. 

El permiso delegado Files.ReadWrite.AppFolder solo es válido para cuentas personales y se usa para obtener acceso a la [carpeta especial del directorio raíz de la aplicación]((https://dev.onedrive.com/misc/appfolder.htm)) con la API de Microsoft Graph [Obtener carpeta especial](../api-reference/v1.0/api/drive_get_specialfolder.md) de OneDrive.


### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _Files.Read_: leer archivos almacenados en el OneDrive del usuario que ha iniciado sesión (`GET /me/drive/root/children`).
* _Files.Read.All_: leer archivos compartidos con el usuario que ha iniciado sesión (`GET /me/drive/root/sharedWithMe`).
* _Files.ReadWrite_: escribir un archivo en el OneDrive del usuario que ha iniciado sesión (`PUT /me/drive/root/children/filename.txt/content`).
* _Files.ReadWrite.All_: escribir un archivo compartido con el usuario (`PUT /users/rgregg@contoso.com/drive/root/children/file.txt/content`).
* _Files.ReadWrite.AppFolder_: escribir archivos en la carpeta de la aplicación en OneDrive (`PUT /me/drive/special/approot/children/file.txt/content`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="group-permissions"></a>Permisos de grupo

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Group.Read.All_ |    Leer todos los grupos | Permite que la aplicación enumere grupos y lea sus propiedades y todas las pertenencias a los grupos en nombre del usuario que ha iniciado sesión.  También permite que la aplicación lea el calendario, las conversaciones, los archivos y otro contenido del grupo de todos los grupos en los que el usuario que ha iniciado sesión tiene acceso. | Sí |
| _Group.ReadWrite.All_ |    Leer y escribir en todos los grupos| Permite que la aplicación cree grupos y lea todas las propiedades de los grupos y las pertenencias en nombre del usuario que ha iniciado sesión.  Además, permite a los propietarios del grupo que administren sus grupos y permite a los miembros del grupo que actualicen su contenido del grupo. | Sí |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Group.Read.All_ | Leer todos los grupos | Permite que la aplicación lea suscripciones para todos los grupos sin la necesidad de que un usuario haya iniciado sesión. Tenga en cuenta que no todas las API de grupo admiten el acceso mediante permisos solo de aplicación. Consulte los [problemas conocidos](../concepts/known_issues.md) para obtener ejemplos. | Sí |
| _Group.ReadWrite.All_ | Leer y escribir en todos los grupos | Permite que la aplicación cree y elimine grupos y lea y actualice pertenencias a grupos. La aplicación puede realizar todas esas operaciones sin que un usuario haya iniciado sesión. Tenga en cuenta que no todas las API de grupo admiten el acceso mediante permisos solo de aplicación. Consulte los [problemas conocidos](../concepts/known_issues.md) para obtener ejemplos.| Sí |


### <a name="remarks"></a>Comentarios

No se admite la funcionalidad de grupo en cuentas personales de Microsoft. 

En el caso de los grupos de Office 365, los permisos de grupo conceden a la aplicación acceso al contenido del grupo, como conversaciones, archivos, notas, etc. 

En el caso de los permisos de la aplicación, se admiten algunas limitaciones para las API. Para obtener más información, vea los [problemas conocidos](../concepts/known_issues.md).

En algunos casos, una aplicación podría necesitar [permisos de directorio](#directory-permissions) para leer algunas propiedades de grupo, como `member` y `memberOf`. Por ejemplo, si un grupo tiene una o más entidades de servicio [servicePrincipals](../api-reference/beta/resources/serviceprincipal.md) como miembros, la aplicación necesitará permisos efectivos para leer las entidades de servicio mediante la concesión de uno de los permisos _Directory.\*_. De lo contrario, Microsoft Graph devolverá un error. (En el caso de los permisos delegados, el usuario que ha iniciado sesión también deberá tener privilegios suficientes en la organización para leer entidades de servicio). Lo mismo se aplica a la propiedad `memberOf`, que puede devolver [administrativeUnits](../api-reference/beta/resources/administrativeunit.md).

Los permisos de grupo también se usan para controlar el acceso a los recursos y las API de [Microsoft Planner](../api-reference/beta/resources/planner_overview.md). Solo se admiten los permisos delegados para las API de Microsoft Planner; no se admiten los permisos de aplicación. No se admiten las cuentas personales de Microsoft.


### <a name="example-usage"></a>Ejemplos de uso
#### <a name="delegated"></a>Delegado

* _Group.Read.All_: leer todos los Grupos de Office 365 de los que es miembro el usuario que ha iniciado sesión (`GET /me/memberOf/$/microsoft.graph.group?$filter=groupTypes/any(a:a%20eq%20'unified')`).
* _Group.Read.All_: leer todo el contenido del Grupo de Office 365, como conversaciones (`GET /groups/{id}/conversations`).
* _Group.ReadWrite.All_: actualizar propiedades del grupo, como la fotografía (`PUT /groups/{id}/photo/$value`).
* _Group.ReadWrite.All_: actualizar miembros del grupo (`POST /groups/{id}/members/$ref`). NOTA: Esto también requiere _User.ReadBasic.All_ para leer el usuario que se va a agregar como miembro.

#### <a name="application"></a>Aplicación

* _Group.Read.All_: buscar todos los grupos cuyo nombre empieza por "Sales" (`GET /groups?$filter=startswith(displayName,'Sales')`).
* _Group.ReadWrite.All_: el servicio de demonio crea eventos en el calendario de un Grupo de Office 365 (`POST /groups/{id}/events`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="identity-risk-event-permissions"></a>Permisos de eventos de riesgo de identidad

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _IdentityRiskEvent.Read.All_ |   Leer información de eventos de riesgo de identidad  | Permite que la aplicación lea información de eventos de riesgo de identidad para todos los usuarios de la organización de parte del usuario que ha iniciado sesión. | Sí |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _IdentityRiskEvent.Read.All_ |   Leer información de eventos de riesgo de identidad | Permite que la aplicación lea información de eventos de riesgo de identidad para todos los usuarios de la organización sin que un usuario haya iniciado sesión. | Sí |


### <a name="remarks"></a>Comentarios

_IdentityRiskEvent.Read.All_ solo es válido para las cuentas profesionales o educativas. Para que una aplicación con permisos delegados pueda leer información de identidad de riesgo, el usuario que ha iniciado sesión debe ser miembro de uno de los siguientes roles de administrador: Administrador global, Administrador de seguridad o Lector de seguridad. Para obtener más información sobre los roles de administrador, vea [Asignación de roles de administrador en Azure Active Directory]((https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)).

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated-and-application"></a>Permisos delegados y de la aplicación

Los siguientes usos son válidos para los permisos delegados y de la aplicación:

* Leer todos los eventos de riesgo generados para todos los usuarios del inquilino (`GET /beta/identityRiskEvents`).
* Leer eventos de riesgo de malware generados por la red de robots (botnet) de Dorkbot (`GET /beta/malwareRiskEvents?$filter=malwareName eq 'Dorkbot'`).
* Leer los 50 eventos de riesgo más recientes (`GET /beta/identityRiskEvents?$orderBy=riskEventDateTime desc&top=50`).
 
Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="identity-provider-permissions"></a>Permisos del proveedor de identidades

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _IdentityProvider.Read.All_ |   Leer la información del proveedor de identidades  | Permite que la aplicación lea los proveedores de identidades configurados en el inquilino de Azure AD o Azure AD B2C en nombre del usuario que ha iniciado sesión. | Sí |
| _IdentityProvider.ReadWrite.All_ |   Leer y escribir información del proveedor de identidades  |  Permite que la aplicación lea o escriba los proveedores de identidades configurados en el inquilino de Azure AD o Azure AD B2C en nombre del usuario que ha iniciado sesión. | Sí |

### <a name="remarks"></a>Comentarios

_IdentityProvider.Read.All_ y _IdentityProvider.ReadWrite.All_ solo son válidos para las cuentas profesionales o educativas. Para que una aplicación lea o escriba proveedores de identidades con permisos delegados, el usuario que ha iniciado sesión debe tener el rol de administrador global. Para más información sobre los roles de administrador, vea [Asignación de roles de administrador en Azure Active Directory]((https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)).

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado
Los siguientes usos son válidos para los permisos delegados:

* _IdentityProvider.Read.All_: leer todos los proveedores de identidades configurados en el inquilino (`GET /beta/identityProviders`).
* _IdentityProvider.Read.All_: leer un proveedor de identidades existente (`GET /beta/identityProviders/{id}`).
* _IdentityProvider.ReadWrite.All_: crear un proveedor de identidades (`POST /beta/identityProviders`).
* _IdentityProvider.ReadWrite.All_: actualizar un proveedor de identidades existente (`PATCH /beta/identityProviders/{id}`).
* _IdentityProvider.ReadWrite.All_: eliminar un proveedor de identidades existente (`DELETE /beta/identityProviders/{id}`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---
## <a name="mail-permissions"></a>Permisos de correo

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Mail.Read_ |    Leer el correo del usuario | Permite que la aplicación lea el correo electrónico de los buzones del usuario. | No |
| _Mail.ReadWrite_ |    Acceso al correo del usuario para la lectura y la escritura  | Permite que la aplicación cree, lea, actualice y elimine correos electrónicos en los buzones del usuario. No incluye el permiso para enviar correos.| No |
| _Mail.Read.Shared_ |    Leer el correo del usuario y el correo compartido | Permite que la aplicación lea el correo al que tiene acceso el usuario, incluido el correo propio y el compartido del usuario. | No |
| _Mail.ReadWrite.Shared_ |    Leer y escribir el correo del usuario y el correo compartido | Permite que la aplicación cree, lea, actualice y elimine el correo para el que el usuario tiene permiso de acceso, incluido el correo propio y compartido del usuario. No incluye el permiso para enviar correos. | No |
| _Mail.Send_ |    Enviar correo como usuario | Permite que la aplicación envíe correos como si fueran usuarios de la organización. | No |
| _Mail.Send.Shared_ |    Enviar correo en nombre de otros | Permite que la aplicación envíe correos como el usuario que ha iniciado sesión, incluidos envíos de parte de terceros. | No |
| _MailboxSettings.Read_ |  Leer la configuración del buzón del usuario | Permite que la aplicación lea la configuración del buzón del usuario. No incluye el permiso para enviar correos. | No |
| _MailboxSettings.ReadWrite_ |  Leer y escribir la configuración del buzón del usuario | Permite que la aplicación cree, lea, actualice y elimine la configuración del buzón del usuario. No incluye el permiso para enviar correos. | No |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _Mail.Read_       |    Leer el correo de todos los buzones | Permite que la aplicación lea el correo de todos los buzones sin la necesidad de que un usuario haya iniciado sesión.| Sí |
| _Mail.ReadWrite_ |    Leer y escribir correos en todos los buzones | Permite que la aplicación cree, lea, actualice y elimine correos en todos los buzones sin un usuario que ha iniciado sesión. No incluye el permiso para enviar correos. | Sí |
| _Mail.Send_ |    Enviar correo como cualquier usuario | Permite que la aplicación envíe correos como cualquier usuario sin la necesidad de que un usuario haya iniciado sesión. | Sí | 
| _MailboxSettings.Read_ |  Leer toda la configuración del buzón del usuario | Permite que la aplicación lea la configuración del buzón del usuario sin la necesidad de que un usuario haya iniciado sesión. No incluye el permiso para enviar correos. | No |
| _MailboxSettings.ReadWrite_ | Leer y escribir toda la configuración del buzón del usuario.  | Permite que la aplicación cree, lea, actualice y elimine la configuración del buzón del usuario sin que un usuario haya iniciado sesión. No incluye el permiso para enviar correos. | Sí |

### <a name="remarks"></a>Comentarios

_Mail.Read.Shared_, _Mail.ReadWrite.Shared_ y _Mail.Send.Shared_ solo son válidos para las cuentas profesionales o educativas. Todos los demás permisos son válidos para las cuentas de Microsoft y para las cuentas profesionales o educativas.

Con el permiso _Mail.Send_ o _Mail.Send.Shared_, una aplicación puede enviar un correo y guardar una copia en la carpeta Elementos enviados del usuario, incluso si la aplicación no usa un permiso _Mail.ReadWrite_ o _Mail.ReadWrite.Shared_ correspondiente.

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _Mail.Read_: enumera los mensajes de la Bandeja de entrada del usuario, ordenados por `receivedDateTime` (`GET /me/mailfolders/inbox/messages?$orderby=receivedDateTime DESC`).
* _Mail.Read.Shared_: buscar todos los mensajes con datos adjuntos en la Bandeja de entrada de un usuario que ha compartido su Bandeja de entrada con el usuario que ha iniciado sesión (`GET /users{id | userPrincipalName}/mailfolders/inbox/messages?$filter=hasAttachments eq true`).
* _Mail.ReadWrite_: marcar un mensaje como leído (`PATCH /me/messages/{id}`).
* _Mail.Send_: enviar un mensaje (`POST /me/sendmail`).
* _MailboxSettings.ReadWrite_: actualizar la respuesta automática del usuario (`PATCH /me/mailboxSettings`).

#### <a name="application"></a>Aplicación

* _Mail.Read_: buscar mensajes de bob@contoso.com (`GET /users/{id | userPrincipalName}/messages?$filter=from/emailAddress/address eq 'bob@contoso.com'`).
* _Mail.ReadWrite_: crear una carpeta en la Bandeja de entrada denominada `Expense Reports` (`POST /users/{id | userPrincipalName}/mailfolders`).
* _Mail.Send_: enviar un mensaje (`POST /users/{id | userPrincipalName}/sendmail`).
* _MailboxSettings.Read_: obtener la zona horaria predeterminada del buzón del usuario (`GET /users/{id | userPrincipalName}/mailboxSettings/timeZone`).


Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="member-permissions"></a>Permisos de miembro

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Member.Read.Hidden_ | Leer todas las pertenencias ocultas | Permite a la aplicación leer las pertenencias a grupos ocultos y unidades administrativas en nombre del usuario que inició sesión, para esos grupos ocultos y unidades administrativas a los que dicho usuario tiene acceso. | Sí |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Member.Read.Hidden_ | Leer todas las pertenencias ocultas | Permite que la aplicación lea las pertenencias de grupos ocultos y unidades administrativas sin la necesidad de que un usuario haya iniciado sesión. | Sí |

### <a name="remarks"></a>Comentarios
_Member.Read.Hidden_ solo es válido en las cuentas profesionales o educativas.

Es posible ocultar la pertenencia a algunos Grupos de Office 365. Esto significa que solo los miembros del grupo pueden ver a los demás miembros. Puede usar esta característica para ayudar a cumplir los reglamentos que exigen que una organización oculte la pertenencia a grupos a usuarios externos (por ejemplo, un Grupo de Office 365 que representa a los alumnos inscritos en una clase).

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _Member.Read.Hidden_: leer los miembros de una unidad administrativa con pertenencia oculta en nombre del usuario que ha iniciado sesión (`GET /administrativeUnits/{id}/members`).
* _Member.Read.Hidden_: leer los miembros de un grupo con pertenencia oculta en nombre del usuario que ha iniciado sesión (`GET /groups/{id}/members`).

#### <a name="application"></a>Aplicación

* _Member.Read.Hidden_: leer los miembros de una unidad administrativa con pertenencia oculta (`GET /administrativeUnits/{id}/members`).
* _Member.Read.Hidden_: leer los miembros de un grupo con pertenencia oculta (`GET /groups/{id}/members`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="notes-permissions"></a>Permisos de notas

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Notes.Read_ |    Leer blocs de notas de usuario de OneNote | Permite que la aplicación lea los títulos de los blocs de notas y las secciones de OneNote y cree páginas, blocs de notas y secciones en nombre del usuario que ha iniciado sesión. | No |
| _Notes.Create_ |    Crear blocs de notas de usuario de OneNote | Permite que la aplicación lea los títulos de los blocs de notas y las secciones de OneNote y cree páginas, blocs de notas y secciones en nombre del usuario que ha iniciado sesión.| No |
| _Notes.ReadWrite_ |    Leer y escribir blocs de notas de usuario de OneNote | Permite que la aplicación lea, comparta y modifique blocs de notas de OneNote en nombre del usuario que ha iniciado sesión. | No |
| _Notes.Read.All_ |    Leer todos los blocs de notas de OneNote a los que el usuario puede tener acceso | Permite que la aplicación lea blocs de notas de OneNote a los que tiene acceso en la organización el usuario que ha iniciado sesión. | No |
| _Notes.ReadWrite.All_ |    Leer y escribir todos los blocs de notas de OneNote a los que el usuario puede tener acceso | Permite que la aplicación lea, comparta y modifique blocs de notas de OneNote a los que tiene acceso en la organización el usuario que ha iniciado sesión.| No |
| _Notes.ReadWrite.CreatedByApp_ |    Acceso limitado al bloc de notas (en desuso) | **En desuso** <br/>No usar. Este permiso no concede privilegios. | No |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Notes.Read.All_ |    Leer todos los blocs de notas de OneNote | Permite que la aplicación lea todos los blocs de notas de OneNote de la organización, sin la necesidad de que un usuario haya iniciado sesión. | Sí |
| _Notes.ReadWrite.All_ |    Leer y escribir todos los blocs de notas de OneNote | Permite que la aplicación lea, comparta y modifique todos los blocs de notas de OneNote de la organización, sin la necesidad de que un usuario haya iniciado sesión.| Sí |


### <a name="remarks"></a>Comentarios
_Notes.Read.All_ y _Notes.ReadWrite.All_ solo son válidos para las cuentas profesionales o educativas. Todos los demás permisos son válidos para las cuentas de Microsoft y para las cuentas profesionales o educativas.

Con el permiso _Notes.Create_, una aplicación puede ver la jerarquía de blocs de notas de OneNote del usuario que ha iniciado sesión y crear contenido de OneNote (blocs de notas, grupos de secciones, secciones, páginas, etc.).

_Notes.ReadWrite_ y _Notes.ReadWrite.All_ también permiten que la aplicación modifique los permisos para el contenido de OneNote al que puede tener acceso el usuario que ha iniciado sesión. 

En el caso de las cuentas profesionales o educativas, _Notes.Read.All_ y _Notes.ReadWrite.All_ permiten que la aplicación tenga acceso al contenido de OneNote de otros usuarios al que tiene permiso de acceso dentro de la organización el usuario que ha iniciado sesión.

### <a name="example-usage"></a>Ejemplos de uso
#### <a name="delegated"></a>Delegado

* _Notes.Create_: crear un bloc de notas para el usuario que ha iniciado sesión (`POST /me/onenote/notebooks`).
* _Notes.Read_: leer el bloc de notas del usuario que ha iniciado sesión (`GET /me/onenote/notebooks`).
* _Notes.Read.All_: obtener todos los blocs de notas a los que tiene acceso en la organización el usuario que ha iniciado sesión (`GET /me/onenote/notebooks?includesharednotebooks=true`).
* _Notes.ReadWrite_: actualizar la página del usuario que ha iniciado sesión (`PATCH /me/onenote/pages/{id}/$value`).
* _Notes.ReadWrite.All_: crear una página en el bloc de notas de otro usuario al que el usuario que ha iniciado sesión tiene acceso dentro de la organización (`POST /users/{id}/onenote/pages`).

#### <a name="application"></a>Aplicación

* _Notes.Read.All_: leer todos los blocs de notas de los usuarios de un grupo (`GET /groups/{id}/onenote/notebooks`).
* _Notes.ReadWrite.All_: actualizar la página de un bloc de notas de cualquier usuario de la organización (`PATCH /users/{id}/onenote/pages/{id}/$value`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).


## <a name="openid-permissions"></a>Permisos de OpenID

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _email_ |    Ver la dirección de correo electrónico de los usuarios | Permite que la aplicación lea la dirección de correo electrónico principal de los usuarios. | No |
| _offline_access_ |    Acceso a los datos de usuario en cualquier momento | Permite que la aplicación lea y actualice los datos del usuario, incluso cuando no están usando en ese momento la aplicación.| No |
| _openid_ |    Inicio de sesión de los usuarios | Permite que los usuarios inicien sesión en la aplicación con sus cuentas profesionales o educativas y permite que la aplicación vea la información básica del perfil del usuario.| No |
| _profile_ |    Ver el perfil básico de los usuarios | Permite que la aplicación vea el perfil básico de los usuarios (nombre, imagen, nombre de usuario).| No |

#### <a name="application-permissions"></a>Permisos de la aplicación

Ninguno.

### <a name="remarks"></a>Comentarios
Puede usar estos permisos para especificar artefactos que quiera que se devuelvan en solicitudes de token y autorización de Azure AD. Los puntos de conexión de Azure AD v1.0 y v2.0 los admiten de forma diferente.

Con el punto de conexión de Azure AD (v1.0), solo se usa el permiso _openid_. Lo tiene que especificar en el parámetro *scope* en una solicitud de autorización para devolver un token de identificador al usar el protocolo OpenID Connect para que un usuario inicie sesión en su aplicación. Para obtener más información, consulte [Autorización del acceso a aplicaciones web con OpenID Connect y Azure Active Directory]((https://docs.microsoft.com/azure/active-directory/develop/active-directory-protocols-openid-connect-code)). Para devolver correctamente un token de identificador, también debe asegurarse de que se configura el permiso _User.Read_ al registrar la aplicación. 

Con el punto de conexión de Azure AD v2.0, se especifica el permiso _offline\_access_ en el parámetro _scope_ para solicitar de forma explícita un token de actualización al usar los protocolos OAuth 2.0 u OpenID Connect. Con OpenID Connect, debe especificar el permiso _openid_ para solicitar un token de identificador. También puede especificar los permisos _email_ y _profile_, o ambos, para devolver notificaciones adicionales en el token de identificador. No es necesario especificar _User.Read_ para devolver un token de identificador con el punto de conexión v2.0. Para obtener más información, consulte [Ámbitos de OpenID Connect](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes#openid-connect-scopes).

> **Importante** Actualmente, la biblioteca de autenticación de Microsoft (MSAL) especifica _offline\_access_, _openid_, _profile_ y _email_ de forma predeterminada en las solicitudes de token y autorización. Esto significa que, para el caso predeterminado, si se especifican estos permisos de forma explícita, es posible que Azure AD devuelva un error. 

---

## <a name="people-permissions"></a>Permisos de personas

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _People.Read_ |    Leer las listas de personas relevantes de los usuarios | Permite que la aplicación lea una lista con puntuación de los contactos relevantes del usuario que ha iniciado sesión. La lista puede incluir contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype). | No |
| _People.Read.All_ | Leer las listas de personas relevantes de todos los usuarios | Permite leer una lista con puntuación de los contactos relevantes para el usuario que ha iniciado sesión o para otros usuarios de la organización del usuario que ha iniciado sesión. La lista puede incluir contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype). También permite que la aplicación busque en todo el directorio de la organización del usuario que ha iniciado sesión. | Sí |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:-----------------------------|:-----------------------------------------|:-----------------|:-----------------|
| _People.Read.All_ | Leer las listas de personas relevantes de todos los usuarios | Permite leer una lista con puntuación de los contactos relevantes para el usuario que ha iniciado sesión o para otros usuarios de la organización del usuario que ha iniciado sesión. <br/><br/>La lista puede incluir contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype). También permite que la aplicación busque en todo el directorio de la organización del usuario que ha iniciado sesión. | Sí |

### <a name="remarks"></a>Comentarios

El permiso People.Read.All solo es válido para las cuentas profesionales y educativas. 

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado
* _People.Read_: leer una lista de los contactos relevantes (`GET /me/people`)
* _People.Read.All_: leer una lista de los contactos relevantes para otro usuario de la misma organización (`GET /users('{id})/people`)

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="reports-permissions"></a>Permisos de informes

#### <a name="delegated-permissions"></a>Permisos delegados

Ninguno.

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Reports.Read.All_ | Leer todos los informes de uso | Permite a una aplicación leer todos los informes de uso de servicio sin necesidad de que un usuario haya iniciado sesión. Los servicios que proporcionan informes de uso incluyen Office 365 y Azure Active Directory. | Sí |

### <a name="remarks"></a>Comentarios
Los permisos de informes solo son válidos para las cuentas profesionales o educativas. 

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="application"></a>Aplicación

* _Reports.Read.All_: leer el informe de detalles de uso de las aplicaciones de correo electrónico durante un período de siete días (`GET /reports/EmailAppUsage(view='Detail',period='D7')/content`).
* _Reports.Read.All_: leer el informe de detalles de actividad de correo electrónico con fecha de 01-01-2017 (`GET /reports/EmailActivity(view='Detail',data='2017-01-01')/content`).
* _Reports.Read.All_: leer el informe de detalles de activaciones de Office 365 (`GET /reports/Office365Activations(view='Detail')/content`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="sites-permissions"></a>Permisos de sitios

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Sites.Read.All_        | Leer los elementos de todas las colecciones de sitios | Permite que la aplicación lea los documentos y enumere los elementos en todas las colecciones de sitios en nombre del usuario que ha iniciado sesión. | No  |
| _Sites.ReadWrite.All_   | Leer y escribir elementos en todas las colecciones de sitios. | Permite que la aplicación edite o elimine los documentos y enumere los elementos en todas las colecciones de sitios en nombre del usuario que ha iniciado sesión. | No  |
| _Sites.Manage.All_      | Leer, editar y eliminar elementos y listas en todas las colecciones de sitios | Permite que la aplicación administre y cree listas, documentos y elementos de listas en todas las colecciones de sitios en nombre del usuario que ha iniciado sesión. | No |
| _Sites.FullControl.All_ | Tomar el control total de todas las colecciones de sitios | Permite que la aplicación tenga control total de los sitios de SharePoint en todas las colecciones de sitios en nombre del usuario que ha iniciado sesión.  | Sí  |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Sites.Read.All_        | Leer los elementos de todas las colecciones de sitios | Permite que la aplicación lea todos los documentos y elementos de lista de todas las colecciones de sitios sin necesidad de que un usuario haya iniciado sesión. | Sí |
| _Sites.ReadWrite.All_   | Leer y escribir elementos en todas las colecciones de sitios. | Permite que la aplicación cree, lea, actualice y elimine documentos y elementos de lista de todas las colecciones de sitios sin necesidad de que un usuario haya iniciado sesión. | Sí |
| _Sites.Manage.All_      | Tomar el control total de todas las colecciones de sitios | Permite que la aplicación administre y cree listas, documentos y elementos de listas en todas las colecciones de sitios sin necesidad de que un usuario haya iniciado sesión.  | Sí  |
| _Sites.FullControl.All_ | Leer, editar y eliminar elementos y listas en todas las colecciones de sitios | Permite que la aplicación tenga control total de los sitios de SharePoint en todas las colecciones de sitios sin necesidad de que un usuario haya iniciado sesión.  | Sí  |


### <a name="remarks"></a>Comentarios

Los permisos de sitios solo son válidos en las cuentas profesionales o educativas.

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _Sites.Read.All_: leer las listas del sitio raíz de SharePoint (`GET /v1.0/sites/root/lists`).
* _Sites.ReadWrite.All_: crear elementos de lista en una lista de SharePoint (`POST /v1.0/sites/root/lists/123/items`).
* _Sites.Manage.All_: agregar una nueva lista a un sitio de SharePoint (`POST /v1.0/sites/root/lists`).
* _Sites.FullControl.All_: acceso completo a listas y sitios de SharePoint.

---

## <a name="tasks-permissions"></a>Permisos de tareas

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _Tasks.Read_ | Leer tareas del usuario | Permite que la aplicación lea las tareas del usuario. | No |
| _Tasks.Read.Shared_ | Leer tareas del usuario y tareas compartidas | Permite que la aplicación lea las tareas para las que el usuario tiene permisos de acceso, incluidas las tareas propias y compartidas del usuario. | No |
| _Tasks.ReadWrite_ |    Crear, leer, actualizar y eliminar tareas y contenedores del usuario | Permite que la aplicación cree, lea, actualice y elimine tareas y contenedores (y las tareas en ellos), que se han asignado o que se han compartido con el usuario que ha iniciado sesión.| No |
| _Tasks.ReadWrite.Shared_ | Leer y escribir las tareas del usuario y tareas compartidas | Permite que la aplicación cree, lea, actualice y elimine las tareas para las que el usuario tiene permisos, incluidas las tareas propias y compartidas. | No |

#### <a name="application-permissions"></a>Permisos de la aplicación

Ninguno.

### <a name="remarks"></a>Comentarios
Los permisos _Tasks_ se usan para controlar el acceso a las tareas de Outlook. El acceso a las tareas de Microsoft Planner se controla mediante [permisos de _grupo_](#group-permissions).

Los permisos _Shared_ actualmente solo se admiten para las cuentas profesionales o educativas. Incluso con permisos _Shared_, puede producirse un error en las lecturas y las escrituras si el usuario que posee el contenido compartido no ha concedido al usuario que tiene acceso los permisos necesarios para modificar el contenido de la carpeta.

### <a name="example-usage"></a>Ejemplos de uso
#### <a name="delegated"></a>Delegado

* _Tasks.Read_: obtener todas las tareas del buzón de un usuario (`GET /me/outlook/tasks`).
* _Tasks.Read.Shared_: tener acceso a las tareas de una carpeta que otro usuario de la organización ha compartido con usted (`Get /users{id|userPrincipalName}/outlook/taskfolders/{id}/tasks`).
* _Tasks.ReadWrite_: agregar un evento a la carpeta de tareas predeterminada del usuario (`POST /me/outook/tasks`).
* _Tasks.Read_: obtener todas las tareas sin completar del buzón de un usuario (`GET /users/{id | userPrincipalName}/outlook/tasks?$filter=status ne 'completed'`).
* _Tasks.ReadWrite_: actualizar una tarea del buzón de un usuario (`PATCH /users/{id | userPrincipalName}/outlook/tasks/id`).
* _Tasks.ReadWrite.Shared_: completar una tarea en nombre de otro usuario (`POST /users/{id | userPrincipalName}/outlook/tasks/id/complete`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="user-permissions"></a>Permisos de usuario

#### <a name="delegated-permissions"></a>Permisos delegados

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _User.Read_       |    Iniciar sesión y leer el perfil del usuario | Permite a los usuarios iniciar sesión en la aplicación y permite a la aplicación leer el perfil de los usuarios que han iniciado sesión. También permite que la aplicación lea la información empresarial básica de los usuarios que han iniciado sesión.| No |
| _User.ReadWrite_ |    Acceso al perfil del usuario para la lectura y la escritura  | Permite que la aplicación lea su perfil. También permite que la aplicación actualice su información de perfil en su nombre. | No |
| _User.ReadBasic.All_ |    Leer perfiles básicos de todos los usuarios | Permite que la aplicación lea un conjunto de propiedades básicas del perfil de otros usuarios de su organización en nombre del usuario que ha iniciado sesión. Esto incluye el nombre para mostrar, el nombre y los apellidos, la dirección de correo electrónico y la fotografía. | No |
| _User.Read.All_  |     Leer los perfiles completos de todos los usuarios           | Permite que la aplicación lea el conjunto completo de las propiedades del perfil, los informes y los administradores de otros usuarios de su organización, en nombre del usuario que ha iniciado sesión. | Sí |
| _User.ReadWrite.All_ |     Leer los perfiles completos de todos los usuarios y escribir en ellos | Permite que la aplicación lea y escriba el conjunto completo de las propiedades del perfil, los informes y los administradores de otros usuarios de su organización, en nombre del usuario que ha iniciado sesión. También permite que la aplicación cree y elimine usuarios, así como restablecer contraseñas de usuario en nombre del usuario que ha iniciado sesión. | Sí |
| _User.Invite.All_  |     Invitar a usuarios a la organización | Permite que la aplicación invite a usuarios a la organización en nombre del usuario que ha iniciado sesión. | Sí |

#### <a name="application-permissions"></a>Permisos de la aplicación

|   Permiso    |  Cadena para mostrar   |  Descripción | Se requiere el consentimiento del administrador |
|:----------------|:------------------|:-------------|:-----------------------|
| _User.Read.All_ |    Leer los perfiles completos de todos los usuarios | Permite que la aplicación lea el conjunto completo de las propiedades del perfil, las pertenencias del grupo, los informes y los administradores de otros usuarios de su organización, sin un usuario que ha iniciado sesión.| Sí |
| _User.ReadWrite.All_ |   Leer los perfiles completos de todos los usuarios y escribir en ellos | Permite que la aplicación lea y escriba el conjunto completo de las propiedades del perfil, las pertenencias del grupo, los informes y los administradores de otros usuarios de su organización sin la necesidad de que un usuario haya iniciado sesión.  También permite que la aplicación cree y elimine usuarios no administrativos. No permite el restablecimiento de contraseñas de usuario. | Sí |
| _User.Invite.All_  |     Invitar a usuarios a la organización | Permite que la aplicación invite a usuarios a la organización sin la necesidad de que un usuario haya iniciado sesión. | Sí |

### <a name="remarks"></a>Comentarios

Los únicos permisos válidos para las cuentas de Microsoft son _User.Read_ y _User.ReadWrite_. En el caso de las cuentas profesionales o educativas, son válidos todos los permisos.

Con el permiso _User.Read_, una aplicación también puede leer información empresarial básica del usuario que ha iniciado sesión para una cuenta profesional o educativa en el recurso de [organización](../api-reference/v1.0/resources/organization.md). Están disponibles las propiedades siguientes: id, displayName y verifiedDomains.

En el caso de las cuentas profesionales o educativas, el perfil completo incluye todas las propiedades declaradas del recurso [usuario](../api-reference/v1.0/resources/user.md). En las lecturas, solo se devuelve de forma predeterminada un número limitado de propiedades. Para leer las propiedades que no están incluidas en el conjunto predeterminado, use `$select`. Las propiedades predeterminadas son:

- displayName
- givenName
- jobTitle
- mail
- mobilePhone
- officeLocation
- preferredLanguage
- surname
- userPrincipalName

 Los permisos delegados _User.ReadWrite_ y _User.Readwrite.All_ permiten que la aplicación actualice las siguientes propiedades de perfil para las cuentas profesionales o educativas:

- aboutMe
- birthday
- hireDate
- interests
- mobilePhone
- mySite
- pastProjects
- photo
- preferredName
- responsibilities
- schools
- skills

Con el permiso de la aplicación _User.ReadWrite.All_, la aplicación puede actualizar todas las propiedades declaradas de las cuentas profesionales o educativas, excepto la contraseña.

Para leer o escribir subordinados directos (`directReports`) o el administrador (`manager`) de una cuenta profesional o educativa, la aplicación debe tener el permiso _User.Read.All_ (solo lectura) o _User.ReadWrite.All_.

El permiso _User.ReadBasic.All_ restringe el acceso de la aplicación a un conjunto limitado de propiedades conocidas como perfil básico. Esto se debe a que el perfil completo podría contener información confidencial del directorio. El perfil básico incluye solo las propiedades siguientes: 

- displayName
- givenName
- mail
- photo
- surname
- userPrincipalName

Para leer las pertenencias a grupos de un usuario (`memberOf`), la aplicación debe tener el permiso [_Group.Read.All_](#group-permissions) o [_Group.ReadWrite.All_](#group-permissions). Pero si el usuario es también miembro de [directoryRole](../api-reference/v1.0/resources/directoryrole.md) o [administrativeUnit](../api-reference/beta/resources/administrativeunit.md), la aplicación necesitará permisos efectivos para leer esos recursos. De lo contrario, Microsoft Graph devolverá un error. Esto significa que la aplicación también necesitará [permisos de directorio](#directory-permissions) y, para los permisos delegados, el usuario que ha iniciado sesión también necesitará privilegios suficientes en la organización para obtener acceso a los roles del directorio y las unidades administrativas. 

### <a name="example-usage"></a>Ejemplos de uso

#### <a name="delegated"></a>Delegado

* _User.Read_: leer el perfil completo del usuario que ha iniciado sesión (`GET /me`).
* _User.ReadWrite_: actualizar la fotografía del usuario que ha iniciado sesión (`PUT /me/photo/$value`).
* _User.ReadBasic.All_: buscar todos los usuarios cuyo nombre empieza por "David" (`GET /users?$filter=startswith(displayName,'David')`).
* _User.Read.All_: leer el administrador de un usuario (`GET /user/{id | userPrincipalName}/manager`).


#### <a name="application"></a>Aplicación

* _User.Read.All_: leer todos los usuarios y las relaciones mediante una consulta delta (`GET /beta/users/delta?$select=displayName,givenName,surname`).
* _User.ReadWrite.All_: actualizar la fotografía de cualquier usuario de la organización (`PUT /user/{id | userPrincipalName}/photo/$value`).

Para obtener información sobre escenarios más complejos que implican varios permisos, vea [Escenarios de permisos](#permission-scenarios).

---

## <a name="permission-scenarios"></a>Escenarios de permisos

En esta sección se muestran algunos escenarios comunes destinados a los recursos de [usuario](../api-reference/v1.0/resources/user.md) y [grupo](../api-reference/v1.0/resources/group.md) de una organización. En las tablas se muestran los permisos que una aplicación necesita para poder realizar operaciones específicas requeridas por el escenario. Tenga en cuenta que, en algunos casos, la capacidad de la aplicación de realizar operaciones específicas dependerá de si un permiso es un permiso delegado o un permiso de la aplicación. En el caso de los permisos delegados, los permisos efectivos de la aplicación también dependerán de los privilegios del usuario que ha iniciado sesión en la organización. Para obtener más información, vea [Permisos delegados, permisos de la aplicación y permisos efectivos](#delegated-permissions-application-permissions-and-effective-permissions).

### <a name="access-scenarios-on-the-user-resource"></a>Escenarios de acceso en el recurso User

| **Tareas de la aplicación que implican el uso del recurso User**   |  **Permisos necesarios** | **Cadenas de permiso** |
|:-------------------------------|:---------------------|:---------------|
| La aplicación quiere leer más información básica de los usuarios (solo el nombre para mostrar y la imagen), por ejemplo, para mostrarla en una experiencia de selección de contactos   | _User.ReadBasic.All_  |  Leer todos los perfiles básicos de usuario |
| La aplicación quiere leer el perfil de usuario completo del usuario que ha iniciado sesión (ver los subordinados directos y el administrador, etc.)     | _User.Read_ | Habilitar el inicio de sesión y leer el perfil del usuario|
| La aplicación desea leer el perfil de usuario completo de todos los usuarios  | _User.Read.All_ |  Leer todos los perfiles completos del usuario   |
| La aplicación desea leer archivos, información del calendario y el correo del usuario que ha iniciado sesión  | _User.Read_, _Files.Read_, _Mail.Read_, _Calendars.Read_ | Habilitar el inicio de sesión y leer el perfil del usuario, Leer los archivos de los usuarios, Leer el correo del usuario, Leer los calendarios del usuario |
| La aplicación desea leer los archivos del usuario que ha iniciado sesión (los míos) y los archivos que otros usuarios han compartido con el usuario que ha iniciado sesión (el mío). | _User.Read_, _Files.Read_, _Sites.Read.All_ | Habilitar el inicio de sesión y leer el perfil del usuario, Leer los archivos de los usuarios, Leer los elementos de todas las colecciones de sitios |
| La aplicación desea leer y escribir en el perfil completo del usuario que ha iniciado sesión   | _User.ReadWrite_ | Acceso al perfil del usuario para la lectura y la escritura  |
| La aplicación desea leer y escribir en el perfil de usuario completo de todos los usuarios    | _User.ReadWrite.All_ | Leer todos los perfiles completos del usuario y escribir en ellos |
| La aplicación desea leer los archivos, el correo y la información del calendario del usuario que ha iniciado sesión y escribir en ellos    | _User.ReadWrite_, _Files.ReadWrite_, _Mail.ReadWrite_, _Calendars.ReadWrite_  |  Acceso de lectura y escritura al perfil del usuario, Acceso de lectura y escritura al perfil del usuario, Acceso de lectura y escritura al correo del usuario, Tener acceso completo a los calendarios del usuario |
   

### <a name="access-scenarios-on-the-group-resource"></a>Escenarios de acceso en el recurso Group
    
| **Tareas de la aplicación que implican el uso del recurso Group**  |  **Permisos necesarios** |  **Cadenas de permiso** |
|:-------------------------------|:---------------------|:---------------|
| La aplicación quiere leer la información básica del grupo (solo el nombre para mostrar y la imagen), por ejemplo, para mostrarla en una experiencia de selección de grupos  | _Group.Read.All_  | Leer todos los grupos|
| La aplicación quiere leer todo el contenido de todos los grupos de Office 365, incluidos los archivos y las conversaciones.  También necesita mostrar las pertenencias a grupos, ser capaz de actualizar las pertenencias a grupos (si es el propietario).  |  _Group.Read.All_ | Leer los elementos de todas las colecciones de sitios, Leer todos los grupos|
| La aplicación quiere leer y escribir todo el contenido de todos los grupos de Office 365, incluidos los archivos y las conversaciones.  También necesita mostrar las pertenencias a grupos, ser capaz de actualizar las pertenencias a grupos (si es el propietario).  |   _Group.ReadWrite.All_, _Sites.ReadWrite.All_ |  Leer y escribir en todos los grupos, Editar o eliminar elementos en todas las colecciones de sitios |
| La aplicación quiere descubrir (buscar) un grupo de Office 365. Permite al usuario buscar un determinado grupo y elegir uno desde la lista enumerada para permitir que el usuario se una al grupo.     | _Group.ReadWrite.All_ | Leer y escribir en todos los grupos|
| La aplicación desea crear un grupo a través de AAD Graph |   _Group.ReadWrite.All_ | Leer y escribir en todos los grupos|
