# <a name="microsoft-graph-permission-scopes"></a>Ámbitos de permisos de Microsoft Graph

Microsoft Graph expone los ámbitos de permisos de OAuth 2.0 que se usan para controlar el acceso que tiene una aplicación a los recursos. Como desarrollador, deberá especificar los ámbitos de permisos que sean adecuados para el acceso que requiera su aplicación. (Si está usando una autenticación de Azure AD, normalmente realizará esta acción a través del Portal de administración de Azure. Si usa el punto de conexión v2.0 de Azure AD, solicitará los permisos dinámicamente en tiempo de ejecución).

Después del inicio de sesión, a los usuarios o a los administradores se les ofrece la oportunidad de permitir que su aplicación obtenga acceso a sus recursos con los ámbitos de permisos que configuró. Por este motivo, deberá elegir los ámbitos de permisos que proporcionen el menor nivel de privilegios necesarios para su aplicación. Para obtener más detalles acerca de cómo configurar los permisos para la aplicación y en el proceso de consentimiento, consulte <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-integrating-applications/" target="_newtab">Integrar aplicaciones con Azure Active Directory</a>.

>**Nota:** Algunos permisos de Microsoft Graph, como los que pertenecen a los grupos y a las tareas, no se aplican a las cuentas personales.  

##<a name="app-only-vs-delegated-permissions"></a>Permisos solo para la aplicación en comparación con los permisos delegados
Los ámbitos de permiso pueden ser solo para la aplicación o delegados. Los ámbitos solo para la aplicación (también conocidos como roles de la aplicación) conceden a la aplicación el conjunto completo de privilegios ofrecidos por el ámbito. Los ámbitos solo para la aplicación los usan normalmente las aplicaciones que se ejecutan como servicio sin que esté presente un usuario que haya iniciado sesión. 


Los ámbitos de permisos delegados son para las aplicaciones que actúan en nombre de un usuario. Estos ámbitos delegan los privilegios del usuario que ha iniciado sesión a la aplicación para permitirle que actúe como si fuera el usuario. Los privilegios reales concedidos a la aplicación serán la combinación menos privilegiada (la intersección) de los privilegios que conceda el ámbito y los que posea el usuario que haya iniciado sesión. Por ejemplo, si el ámbito de permiso concede privilegios delegados para escribir todos los objetos del directorio, pero el usuario que ha iniciado sesión tiene privilegios solo para actualizar su propio perfil de usuario, la aplicación solo podrá escribir el perfil del usuario que ha iniciado sesión, pero no otros objetos.

> **Nota**: Para los grupos, solo un subconjunto de la API relativa a la administración de grupos básicos admite permisos solo para la aplicación y permisos delegados. Todos los demás miembros de la API de solo admiten permisos delegados. Vea [problemas conocidos](../overview/release_notes.md#groups) para obtener ejemplos.

## <a name="full-and-basic-profiles-for-users-and-groups"></a>Perfiles completos y básicos de usuarios y grupos

El perfil completo (o perfil) de un usuario o de un grupo incluye todas las propiedades declaradas de la entidad. Ya que el perfil puede contener información del directorio confidencial o información de identificación personal (PII), varios ámbitos limitan el acceso de la aplicación a un conjunto de propiedades limitadas conocidas como perfil básico. En el caso de los usuarios, el perfil básico incluye solo las propiedades siguientes: 

- Nombre para mostrar
- Nombre y apellidos
- Foto
- Dirección de correo electrónico

En el caso de los grupos, el perfil básico contiene solo el nombre para mostrar. 

<!---    <a name="msg_perm_details"> </a>  -->

## <a name="permission-scope-details"></a>Detalles del ámbito de permisos

Debe configurar la aplicación para tener los permisos necesarios para obtener acceso a los recursos de Microsoft Graph. Los permisos se aplican a recursos individuales para los derechos de lectura, escritura o ambos. 

Las tablas siguientes enumeran los ámbitos de permisos de Microsoft Graph y explican el acceso que concede cada uno. 

- La columna **Ámbito** enumera el nombre del ámbito. Los nombres del ámbito adoptan la forma resource.operation.constraint; por ejemplo, Group.ReadWrite.All. Si la restricción es “All”, el ámbito concederá a la aplicación la capacidad de realizar la operación (ReadWrite) en todos los recursos especificados (Group) en el directorio; de lo contrario, el ámbito solo permitirá la operación en el perfil del usuario que haya iniciado sesión. Los ámbitos pueden conceder privilegios limitados para la operación especificada. Consulte la columna **Descripción** para obtener más detalles.
- En la columna **Permiso** se ofrece información acerca de cómo se muestra el ámbito en Azure Portal. 
- En la columna **Descripción** se describe el conjunto completo de privilegios que concede el ámbito. Para ámbitos delegados, el acceso real concedido a la aplicación será la combinación menos privilegiada (la intersección) del acceso concedido por el ámbito y los privilegios del usuario que ha iniciado sesión. 
- Los ámbitos se agrupan en función de si los permisos requieren el consentimiento de un administrador.

  > **Nota**: Consulte [Problemas conocidos](../overview/release_notes.md) para las limitaciones del ámbito de permisos de `v1.0` y de `beta`.
  
###<a name="permissions-requiring-administrators-consent"></a>Permisos que requieren el consentimiento del administrador

|   **Ámbito**                  |  **Permiso**                          |  **Descripción** |
|:-----------------------------|:-----------------------------------------|:-----------------|
| _Directory.AccessAsUser.All_   |     Obtener acceso al directorio como usuario que ha iniciado sesión  | Permite que la aplicación tenga el mismo acceso a la información del directorio que el usuario que inició sesión.|
| _Directory.Read.All_           |     Leer datos del directorio                     | Permite que la aplicación lea los datos del directorio de su organización, como los usuarios, los grupos y las aplicaciones. |
| _Directory.ReadWrite.All_      |     Leer y escribir datos en el directorio           | Permite que la aplicación lea y escriba los datos del directorio de su organización, como los usuarios y los grupos.  No se permite la eliminación de un usuario o un grupo. No permite que la aplicación elimine usuarios o grupos ni que restablezca contraseñas de usuario. |
| _Group.Read.All_ |    Leer todos los grupos | Permite que la aplicación enumere grupos y lea sus propiedades y todas las pertenencias a los grupos en nombre del usuario que ha iniciado sesión.  También permite que la aplicación lea el calendario, las conversaciones, los archivos y otro contenido del grupo de todos los grupos en los que el usuario que ha iniciado sesión tiene acceso. |
| _Group.ReadWrite.All_ |    Leer y escribir en todos los grupos| Permite que la aplicación cree grupos y lea todas las propiedades de los grupos y las pertenencias en nombre del usuario que ha iniciado sesión.  Además, permite a los propietarios del grupo que administren sus grupos y permite a los miembros del grupo que actualicen su contenido del grupo. |
| _User.Read.All_                |     Leer todos los perfiles completos del usuario           | Igual que User.ReadBasic.All, excepto que permite que la aplicación lea el perfil completo de todos los usuarios de la organización y cuando lee las propiedades de navegación como el administrador y los subordinados. El perfil completo incluye todas las propiedades declaradas de la entidad **Usuario**. Para leer los grupos de los que es miembro un usuario, la aplicación requerirá también Group.Read.All o Group.ReadWrite.All. |
| _User.ReadWrite.All_           |     Leer todos los perfiles completos del usuario y escribir en ellos | Permite que la aplicación lea y escriba el conjunto completo de las propiedades del perfil, los informes y los administradores de otros usuarios de su organización, en nombre del usuario que ha iniciado sesión. |


###<a name="permissions-not-requiring-administrators-consent"></a>Permisos que no requieren el consentimiento del administrador

|   **Ámbito**    |  **Permiso**   |  **Descripción** |
|:-----------------------------|:-----------------------------------------|:-----------------|
| _Calendars.Read_ |    Leer los calendarios del usuario  | Permite que la aplicación lea los eventos en los calendarios del usuario.|
| _Calendars.Read.Shared_ |    Leer los calendarios del usuario y los calendarios compartidos | Permite que la aplicación lea los eventos en todos los calendarios a los que tiene acceso el usuario, incluidos los calendarios de delegado y compartidos. |
| _Calendars.ReadWrite_ |    Obtener acceso completo a los calendarios del usuario  | Permite que la aplicación cree, lea, actualice y elimine eventos de los calendarios del usuario. |
| _Calendars.ReadWrite.Shared_ |    Leer y escribir los calendarios del usuario y los calendarios compartidos | Permite que la aplicación cree, lea, actualice y elimine eventos en todos los calendarios para los que el usuario tiene permisos de acceso. Esto incluye los calendarios de delegado y los calendarios compartidos.|
| _Contacts.Read_ |    Leer los contactos del usuario  | Permite que la aplicación lea los contactos del usuario. |
| _Contacts.Read.Shared_ |    Leer los contactos del usuario y los contactos compartidos | Permite que la aplicación lea los contactos para los que el usuario tiene permisos de acceso, incluidos los contactos propios y compartidos del usuario. |
| _Contacts.ReadWrite_ |    Obtener acceso completo a los contactos del usuario  | Permite que la aplicación cree, lea, actualice y elimine los contactos del usuario. |
| _Contacts.ReadWrite.Shared_ |    Leer y escribir los contactos del usuario y los contactos compartidos | Permite que la aplicación cree, lea, actualice y elimine los contactos para los que el usuario tiene permisos de acceso, incluidos los contactos propios y compartidos del usuario.|
| _Files.Read_ |    Leer los archivos del usuario y los que se han compartido con él | Permite que la aplicación lea los archivos del usuario que inició sesión y los archivos compartidos con este.| 
| _Files.Read.All_ | Leer todos los archivos a  los que el usuario puede tener acceso | Permite que la aplicación lea todos archivos a los que el puede tener acceso el usuario que inició sesión. |
| _Files.Read.Selected_ |    Leer los archivos que el usuario selecciona  | Permite que la aplicación lea los archivos que el usuario selecciona. La aplicación tiene acceso durante varias horas después de que el usuario seleccione un archivo. |
| _Files.ReadWrite_ |   Obtener acceso completo a los archivos del usuario y a los que se han compartido con él | Permite que la aplicación lea, cree, actualice y elimine los archivos del usuario que inició sesión y los archivos compartidos con el usuario. |
| _Files.ReadWrite.All_ | Tener acceso completo a todos los archivos a los que puede tener acceso el usuario | Permite que la aplicación lea, cree, actualice y elimine todos los archivos a los que puede tener acceso el usuario que inició sesión. |
| _Files.ReadWrite.AppFolder_ | Tener acceso completo a la carpeta de la aplicación | Permite que la aplicación lea, cree, actualice y elimine archivos de la carpeta de la aplicación. |
| _Files.ReadWrite.Selected_ |    Leer los archivos que el usuario selecciona y escribir en ellos | Permite que la aplicación lea y escriba archivos que el usuario selecciona. La aplicación tiene acceso durante varias horas después de que el usuario seleccione un archivo. |
| _Mail.Read_ |    Leer el correo del usuario | Permite que la aplicación lea el correo electrónico de los buzones del usuario. |
| _Mail.Read.Shared_ |    Leer el correo del usuario y el correo compartido | Permite que la aplicación lea el correo al que tiene acceso el usuario, incluido el correo propio y el compartido del usuario. |
| _Mail.ReadWrite_ |    Acceso al correo del usuario para la lectura y la escritura  | Permite que la aplicación cree, lea, actualice y elimine correos electrónicos en los buzones del usuario. No incluye el permiso para enviar correos.|
| _Mail.ReadWrite.Shared_ |    Leer y escribir el correo del usuario y el correo compartido | Permite que la aplicación cree, lea, actualice y elimine el correo para el que el usuario tiene permiso de acceso, incluido el correo propio y compartido del usuario. No incluye el permiso para enviar correos. |
| _Mail.Send_ |    Enviar correo como usuario | Permite que la aplicación envíe correos como si fueran usuarios de la organización. |
| _Mail.Send.Shared_ |    Enviar correo en nombre de otros | Permite que la aplicación envíe correos como el usuario que ha iniciado sesión, incluidos envíos de parte de terceros. |
| _MailboxSettings.ReadWrite_ |  Leer y escribir la configuración del buzón del usuario | Permite que la aplicación cree, lea, actualice y elimine la configuración del buzón del usuario. No incluye el permiso para enviar correos.|
| _offline_access_ |    Acceso a los datos de usuario en cualquier momento (versión preliminar) | Permite que la aplicación lea y actualice los datos del usuario, incluso cuando no están usando en ese momento la aplicación.|
| _openid_ |    Iniciar la sesión de los usuarios (versión preliminar) | Permite que los usuarios inicien sesión en la aplicación con sus cuentas profesionales o educativas y permite que la aplicación vea la información básica del perfil del usuario.|
| _User.Read_       |    Iniciar sesión y leer el perfil del usuario | Permite a los usuarios iniciar sesión en la aplicación y permite a la aplicación leer el perfil de los usuarios que han iniciado sesión. El perfil completo incluye todas las propiedades declaradas de la entidad usuario. La aplicación no puede leer las propiedades de navegación, como el administrador o los subordinados. También permite que la aplicación lea la siguiente información básica de la empresa del usuario que ha iniciado sesión (a través del objeto **TenantDetail**): id. de inquilino, nombre para mostrar del inquilino y dominios comprobados.|
| _User.ReadWrite_ |    Acceso al perfil del usuario para la lectura y la escritura  | Permite que la aplicación lea su perfil. También permite que la aplicación actualice su información de perfil en su nombre. |
| _User.ReadBasic.All_ |    Leer el perfil básico de todos los usuarios | Permite que la aplicación lea el perfil básico de todos los usuarios de la organización en nombre del usuario que ha iniciado sesión. Las siguientes propiedades comprenden el perfil básico del usuario: nombre para mostrar, nombre y apellidos, foto y dirección de correo electrónico. Para leer los grupos de los que es miembro un usuario, la aplicación requerirá también Group.Read.All o Group.ReadWrite.All.| 

###<a name="app-only-permissions-requiring-administrators-consent"></a>Los permisos solo para la aplicación requieren el consentimiento del administrador

|   **Ámbito**    |  **Permiso**   |  **Descripción** |
|:---------------|:------------------|:-----------------|
| _Calendars.Read_ |    Leer los calendarios de todos los buzones | Permite que la aplicación lea los eventos de todos los calendarios sin la necesidad de que un usuario haya iniciado sesión. |
| _Calendars.ReadWrite_ |    Leer los calendarios de todos los buzones y escribir en ellos | Permite que la aplicación cree, lea, actualice y elimine eventos en todos los calendarios sin la necesidad de que un usuario haya iniciado sesión.|
| _Contacts.Read_ |    Leer los contactos de todos los buzones | Permite que la aplicación lea todos los contactos de todos los buzones sin la necesidad de que un usuario haya iniciado sesión. |
| _Contacts.ReadWrite_ |    Leer y escribir contactos en todos los buzones  |Permite que la aplicación cree, lea, actualice y elimine todos los contactos en todos los buzones sin la necesidad de que un usuario haya iniciado sesión.|
| _Device.ReadWrite.All_ | Leer y escribir dispositivos | Permite que la aplicación lea y escriba todas las propiedades del dispositivo sin iniciar sesión con ningún usuario. No permite la creación de dispositivos, su eliminación o la actualización de identificadores de seguridad alternativos de dispositivos. |
| _Directory.Read.All_ | Leer datos del directorio | Permite que la aplicación lea los datos del directorio de su organización, como los usuarios, los grupos y las aplicaciones sin iniciar sesión con ningún usuario. |
| _Directory.ReadWrite.All_ | Leer y escribir datos en el directorio | Permite que la aplicación lea y escriba los datos del directorio de su organización, como los usuarios y los grupos sin iniciar sesión con ningún usuario. No se permite la eliminación de un usuario o un grupo. |
| _Files.Read.All_ | Leer todos los archivos a  los que el usuario puede tener acceso | Permite que la aplicación lea todos los archivos de todas las colecciones de sitios sin la necesidad de que un usuario haya iniciado sesión. |
| _Files.ReadWrite.All_ | Tener acceso completo a todos los archivos a los que puede tener acceso el usuario | Permite que la aplicación lea, escriba, actualice y elimine todos los archivos de todas las colecciones de sitios sin la necesidad de que un usuario haya iniciado sesión. |
| _Group.Read.All_ | Leer todos los grupos | Permite que la aplicación lea suscripciones para todos los grupos sin la necesidad de que un usuario haya iniciado sesión. Tenga en cuenta que no todas las API de grupo admiten el acceso mediante permisos solo de aplicación. Consulte los [problemas conocidos](../overview/release_notes.md#groups) para obtener ejemplos. |
| _Group.ReadWrite.All_ | Leer y escribir en todos los grupos | Permite que la aplicación cree y elimine grupos y lea y actualice pertenencias a grupos. La aplicación puede realizar todas esas operaciones sin que un usuario haya iniciado sesión. Tenga en cuenta que no todas las API de grupo admiten el acceso mediante permisos solo de aplicación. Consulte los [problemas conocidos](../overview/release_notes.md#groups) para obtener ejemplos.|
| _Mail.Read_       |    Leer el correo de todos los buzones | Permite que la aplicación lea el correo de todos los buzones sin la necesidad de que un usuario haya iniciado sesión.|
| _Mail.ReadWrite_ |    Leer y escribir correos en todos los buzones | Permite que la aplicación cree, lea, actualice y elimine correos en todos los buzones sin un usuario que ha iniciado sesión. No incluye el permiso para enviar correos. |
| _Mail.Send_ |    Enviar correo como cualquier usuario | Permite que la aplicación envíe correos como cualquier usuario sin la necesidad de que un usuario haya iniciado sesión. | 
| _MailboxSettings.ReadWrite_ | Leer y escribir toda la configuración del buzón del usuario.  | Permite que la aplicación cree, lea, actualice y elimine la configuración del buzón del usuario sin que un usuario haya iniciado sesión. No incluye el permiso para enviar correos. |
| _Member.Read.Hidden_ | Leer todas las pertenencias ocultas | Permite que la aplicación lea las pertenencias de grupos ocultos y unidades administrativas sin la necesidad de que un usuario haya iniciado sesión. |
| _Reports.Read.All_ | Leer todos los informes de uso | Permite a una aplicación leer todos los informes de uso de servicio sin necesidad de que un usuario haya iniciado sesión. Los servicios que proporcionan informes de uso incluyen Office 365 y Azure Active Directory. |
| _User.Read.All_ |    Leer los perfiles completos de todos los usuarios | Permite que la aplicación lea el conjunto completo de las propiedades del perfil, las pertenencias del grupo, los informes y los administradores de otros usuarios de su organización, sin un usuario que ha iniciado sesión.| 
| _User.ReadWrite.All_ |   Leer los perfiles completos de todos los usuarios y escribir en ellos | Permite que la aplicación lea y escriba el conjunto completo de las propiedades del perfil, las pertenencias del grupo, los informes y los administradores de otros usuarios de su organización, sin un usuario que ha iniciado sesión.|


##<a name="permission-scopes-in-preview"></a>Ámbitos de permisos en la versión preliminar

###<a name="permissions-requiring-administrators-consent-preview"></a>Permisos que requieren el consentimiento del administrador (versión preliminar)

|   **Ámbito**    |  **Permiso**   |  **Descripción** |
|:---------------|:------------------|:-----------------|
| _IdentityRiskEvent.Read.All_ |   Leer información de eventos de riesgo de identidad (vista previa) | Permite que la aplicación lea información de eventos de riesgo de identidad para todos los usuarios de la organización de parte del usuario que ha iniciado sesión. |
| _DeviceManagementServiceConfiguration.Read.All_ | Leer configuración de Microsoft Intune (vista previa) | Permite que la aplicación lea las propiedades de servicio de Microsoft Intune, incluidas la inscripción del dispositivo y la configuración de conexión del servicio de terceros. |
| _DeviceManagementServiceConfiguration.ReadWrite.All_ | Leer y escribir la configuración de Microsoft Intune (vista previa) | Permite que la aplicación lea y escriba las propiedades de servicio de Microsoft Intune, incluidas la inscripción del dispositivo y la configuración de conexión del servicio de terceros. |
| _DeviceManagementConfiguration.Read.All_ | Leer las directivas y configuración de dispositivo de Microsoft Intune (vista previa) | Permite que la aplicación lea las propiedades de una configuración de dispositivo administrada por Microsoft Intune y las directivas de cumplimiento de dispositivos y su asignación a grupos. |
| _DeviceManagementConfiguration.ReadWrite.All_ | Leer y escribir las directivas y configuración de dispositivo de Microsoft Intune (vista previa) | Permite que la aplicación lea y escriba las propiedades de una configuración de dispositivo administrada por Microsoft Intune y las directivas de cumplimiento de dispositivos y su asignación a grupos. |
| _DeviceManagementApps.Read.All_ | Leer aplicaciones de Microsoft Intune (vista previa) | Permite que la aplicación lea las propiedades, asignaciones de grupos y estados de aplicaciones, configuraciones de aplicaciones y directivas de protección de aplicaciones administradas por Microsoft Intune. |
| _DeviceManagementApps.ReadWrite.All_ | Leer y escribir aplicaciones de Microsoft Intune (vista previa) | Permite que la aplicación lea y escriba las propiedades, asignaciones de grupos y estados de aplicaciones, configuraciones de aplicaciones y directivas de protección de aplicaciones administradas por Microsoft Intune. |
| _DeviceManagementRBAC.Read.All_ | Leer la configuración de RBAC de Microsoft Intune (vista previa) | Permite que la aplicación lea las propiedades relacionadas con la configuración del control de acceso basado en roles (RBAC) de Microsoft Intune. |
| _DeviceManagementRBAC.ReadWrite.All_ | Leer y escribir la configuración de RBAC de Microsoft Intune (vista previa) | Permite que la aplicación lea y escriba las propiedades relacionadas con la configuración del control de acceso basado en roles (RBAC) de Microsoft Intune. |
| _DeviceManagementManagedDevices.Read.All_ | Leer dispositivos de Microsoft Intune (vista previa) | Permite que la aplicación lea las propiedades de dispositivos administrados por Microsoft Intune. |
| _DeviceManagementManagedDevices.ReadWrite.All_ | Leer y escribir dispositivos de Microsoft Intune (vista previa) | Permite que la aplicación lea y escriba las propiedades de dispositivos administrados por Microsoft Intune. No permite operaciones de alto impacto como la eliminación remota y el restablecimiento de contraseña del propietario del dispositivo. |
| _DeviceManagementManagedDevices.PrivilegedOperations.All_ | Realizar acciones remotas que repercutan en el usuario en dispositivos de Microsoft Intune (vista previa) | Permite que la aplicación realice acciones de alto impacto remotas como la eliminación remota de datos del dispositivo o restablecer la contraseña en dispositivos administrados por Microsoft Intune. |

###<a name="permissions-not-requiring-administrators-consent-preview"></a>Permisos que no requieren el consentimiento del administrador (versión preliminar)

|   **Ámbito**    |  **Permiso**   |  **Descripción** |
|:---------------|:------------------|:-----------------|
| _Notes.Create_ |    Crear páginas en los blocs de notas de los usuarios (versión preliminar) | Permite que la aplicación lea los títulos de los blocs de notas y las secciones y cree páginas nuevas, blocs de notas y secciones en nombre del usuario que ha iniciado sesión.|
| _Notes.Read_ |    Leer blocs de notas del usuario (versión preliminar) | Permite que la aplicación ver los títulos de los blocs de notas de OneNote y las secciones y lea todas las páginas en nombre del usuario que ha iniciado sesión. No puede ver las secciones protegidas con contraseña. |
| _Notes.Read.All_ |    Leer todos los blocs de notas a los que el usuario pueda obtener acceso (versión preliminar) | Permite que la aplicación lea los contenidos de todos los blocs de notas y las secciones a las que el usuario que ha iniciado sesión tiene acceso.   No puede leer las secciones protegidas con contraseña. |
| _Notes.ReadWrite_ |    Leer blocs de notas del usuario y escribir en ellos (versión preliminar) | Permite que la aplicación lea los títulos de los blocs de notas y las secciones, lea todas las páginas, escriba todas las páginas y cree nuevas páginas en nombre del usuario que ha iniciado sesión.  No puede acceder a las secciones protegidas con contraseña. |
| _Notes.ReadWrite.All_ |    Leer todos los blocs de notas a los que el usuario pueda obtener acceso y escribir en ellos (versión preliminar) | Permite que la aplicación lea y escriba los contenidos de todos los blocs de notas y las secciones a las que el usuario que ha iniciado sesión tiene acceso.  No puede acceder a las secciones protegidas con contraseña.|
| _Notes.ReadWrite.CreatedByApp_ |    Acceso limitado al bloc de notas (versión preliminar) | Permite que la aplicación lea los títulos de los blocs de notas y las secciones y cree páginas nuevas en nombre del usuario que ha iniciado sesión. También permite que la aplicación lea y actualice las páginas creadas por la aplicación. |
| _People.Read_ |    Leer las listas de contactos relevantes de los usuarios (versión preliminar) | Permite que la aplicación lea un listado ordenado de los contactos relevantes del usuario que ha iniciado sesión. La lista incluye los contactos locales, los contactos de las redes sociales, el directorio de su organización y los contactos de comunicaciones recientes (como el correo electrónico y Skype).|
| _Sites.Read.All_ |    Leer los elementos de todas las colecciones de sitios | Permite que la aplicación lea los documentos y enumere los elementos de todas las colecciones de sitios en nombre del usuario que ha iniciado sesión. |
| _Sites.ReadWrite.All_ |    Leer y escribir elementos en todas las colecciones de sitios. | Permite que la aplicación edite o lea los documentos y enumere los elementos de todas las colecciones de sitios en nombre del usuario que ha iniciado sesión. |
| _Tasks.Read_ | Leer tareas del usuario | Permite que la aplicación lea las tareas del usuario. |
| _Tasks.Read.Shared_ | Leer tareas del usuario y tareas compartidas | Permite que la aplicación lea las tareas para las que el usuario tiene permisos de acceso, incluidas las tareas propias y compartidas del usuario. |
| _Tasks.ReadWrite_ |    Crear, leer, actualizar y eliminar tareas y planes del usuario (versión preliminar) | Permite que la aplicación cree, lea, actualice y elimine tareas y planes (y las tareas en ellos), que se han asignado o que se han compartido con el usuario que ha iniciado sesión.|
| _Tasks.ReadWrite.Shared_ | Leer y escribir las tareas del usuario y tareas compartidas | Permite que la aplicación cree, lea, actualice y elimine las tareas para las que el usuario tiene permisos, incluidas las tareas propias y compartidas. |



##<a name="permission-scope-scenarios"></a>Escenarios de ámbito de permiso
Los siguientes son algunos escenarios de la aplicación que usan los recursos `User` y `Group` y sus correspondientes ámbitos requeridos. La siguiente tabla muestra los ámbitos de permiso necesarios para que una aplicación pueda realizar operaciones específicas. Tenga en cuenta que en algunos casos, capacidad de la aplicación para realizar algunas operaciones dependerá de si el ámbito del permiso es solo para la aplicación o delegado, y, en el caso de ámbitos de permiso delegados, en los privilegios del usuario que ha iniciado sesión. 

###<a name="access-scenarios-using-the-user-resource-and-the-required-scopes"></a>Obtener acceso a los escenarios usando el recurso User y los ámbitos requeridos

| **Tareas de la aplicación que implican el uso del recurso User**     |  **Ámbitos requeridos** | **Permisos** |
|:-------------------------------|:---------------------|:---------------|
| La aplicación desea leer más información básica de los usuarios (solo el nombre para mostrar y la imagen), por ejemplo, para mostrar en una experiencia de selección de usuarios     | _User.ReadBasic.All_  |  Leer todo el perfil básico del usuario |
| La aplicación desea leer el perfil de usuario completo del usuario que ha iniciado sesión (ver los subordinados directos y el administrador, etc.)     | _User.Read_ | Habilitar el inicio de sesión y leer el perfil del usuario|
| La aplicación desea leer el perfil de usuario completo de todos los usuarios     | _User.Read.All_ |  Leer todos los perfiles completos del usuario   |
| La aplicación desea leer archivos, información del calendario y el correo del usuario que ha iniciado sesión     | _User.Read_, _Files.Read_, _Mail.Read_, _Calendars.Read_ | Habilitar el inicio de sesión y leer el perfil del usuario, Leer los archivos de los usuarios, Leer el correo del usuario, Leer los calendarios del usuario |
| La aplicación desea leer los archivos del usuario que ha iniciado sesión (los míos) y los archivos que otros usuarios han compartido con el usuario que ha iniciado sesión (el mío). | _User.Read_, _Files.Read_, _Sites.Read.All_ | Habilitar el inicio de sesión y leer el perfil del usuario, Leer los archivos de los usuarios, Leer los elementos de todas las colecciones de sitios |
| La aplicación desea leer y escribir en el perfil completo del usuario que ha iniciado sesión     | _User.ReadWrite_ | Acceso al perfil del usuario para la lectura y la escritura  |
| La aplicación desea leer y escribir en el perfil de usuario completo de todos los usuarios     | _User.ReadWrite.All_ | Leer todos los perfiles completos del usuario y escribir en ellos |
| La aplicación desea leer los archivos, el correo y la información del calendario del usuario que ha iniciado sesión y escribir en ellos     | _User.ReadWrite_, _Files.ReadWrite_, _Mail.ReadWrite_, _Calendars.ReadWrite_  |  Acceso de lectura y escritura al perfil del usuario, Acceso de lectura y escritura al perfil del usuario, Acceso de lectura y escritura al correo del usuario, Tener acceso completo a los calendarios del usuario |
   

###<a name="access-scenarios-using-the-group-resource-and-the-required-scopes"></a>Escenarios de acceso mediante el recurso Group y los ámbitos requeridos
    
| **Tareas de la aplicación que implican el uso del recurso Group**     |  **Ámbitos requeridos** |  **Permisos** |
|:-------------------------------|:---------------------|:---------------|
| La aplicación desea leer la información básica del grupo (solo el nombre para mostrar y la imagen), por ejemplo, para mostrarla en una experiencia de selección de grupos     | _Group.Read.All_  | Leer todos los grupos|
| La aplicación quiere leer todo el contenido de todos los grupos de Office 365, incluidos los archivos y las conversaciones.  También necesita mostrar las pertenencias a grupos, ser capaz de actualizar las pertenencias a grupos (si es el propietario).  |  _Group.Read.All_ | Leer los elementos de todas las colecciones de sitios, Leer todos los grupos|
| La aplicación quiere leer y escribir todo el contenido de todos los grupos de Office 365, incluidos los archivos y las conversaciones.  También necesita mostrar las pertenencias a grupos, ser capaz de actualizar las pertenencias a grupos (si es el propietario).  |     _Group.ReadWrite.All_, _Sites.ReadWrite.All_ |  Leer y escribir en todos los grupos, Editar o eliminar elementos en todas las colecciones de sitios |
| La aplicación quiere descubrir (buscar) un grupo de Office 365. Permite al usuario buscar un determinado grupo y elegir uno desde la lista enumerada para permitir que el usuario se una al grupo.     | _Group.ReadWrite.All_ | Leer y escribir en todos los grupos|
| La aplicación desea crear un grupo a través de AAD Graph |     _Group.ReadWrite.All_ | Leer y escribir en todos los grupos|
 


