# <a name="intune-devices-and-apps-api-overview"></a>Información general sobre la API de dispositivos y aplicaciones de Intune

Microsoft Intune ayuda a las empresas a administrar dispositivos y aplicaciones de una organización. Puede usar la API de Intune en Microsoft Graph para administrar dispositivos, aplicaciones e incluso configurar Intune usando las herramientas que prefiera. 

Si es un ISV, también puede usar la API de Intune para administrar a los inquilinos de cliente.

## <a name="why-integrate-with-intune"></a>¿Por qué debería realizar la integración con Intune?

Puede usar la API de Intune en Microsoft Graph para acceder a información de dispositivos y aplicaciones de Intune, administrar dispositivos y aplicaciones, y automatizar Intune.

### <a name="manage-devices"></a>Administrar dispositivos

Puede usar la API de Intune para:

- Definir y aplicar directivas de [cumplimiento de dispositivo](../api-reference/v1.0/resources/intune_deviceconfig_devicecomplianceactionitem.md), como la complejidad de la contraseña y su duración, el cifrado, los niveles de protección de amenazas y así sucesivamente.  (Las directivas compatibles varían según el sistema operativo y la versión).
- [Proteger los datos de la compañía](../api-reference/v1.0/resources/intune_mam_windowsinformationprotectionpolicy.md), independientemente de si la plataforma del dispositivo es Windows, Mac, Android o iOS.
- Crear e implementar directivas de [configuración de dispositivo](../api-reference/v1.0/resources/intune_deviceconfig_deviceconfiguration.md), incluyendo la plataforma del sistema operativo y el control de versiones, la pertenencia a un dominio y la administración de las opciones de configuración.
- Crear e implementar directivas de [control de acceso](../api-reference/v1.0/resources/intune_onboarding_onpremisesconditionalaccesssettings.md) a dispositivos, incluyendo descarga restringida, acceso accesorio de red y transferencia de archivos.
- Realizar [acciones remotas](../api-reference/v1.0/resources/intune_devices_manageddevice.md), como buscar el dispositivo, cambiar la contraseña y borrar el dispositivo.

### <a name="manage-apps"></a>Administrar aplicaciones 

Puede usar la API de Intune para realizar las siguientes tareas de administración de la aplicación:

- Implementar [aplicaciones en dispositivos](../api-reference/v1.0/resources/intune_apps_mobileapp.md) o impedir que se implementen aplicaciones.
- Administrar el acceso a [libros electrónicos](../api-reference/v1.0/resources/intune_books_ebookinstallsummary.md) y otros servicios relacionados.
- Definir e implementar opciones de configuración, opciones de protección y directivas de uso de la aplicación.

### <a name="automate-intune"></a>Automatizar Intune

Automatice Intune mediante la API de Intune para:

- Definir y asignar controles de acceso [basados en roles](../api-reference/v1.0/resources/intune_rbac_conceptual.md).
- Auditar y crear informes de cumplimiento, uso y acceso.
- Administrar [gastos de telecomunicaciones](../api-reference/v1.0/resources/intune_tem_conceptual.md).


## <a name="next-steps"></a>Siguientes pasos

- [Usar Azure AD para obtener acceso a la API de Intune](https://docs.microsoft.com/intune/intune-graph-apis).
- Obtenga información sobre cómo realizar tareas comunes con los [ejemplos de Intune de PowerShell](https://github.com/microsoftgraph/powershell-intune-samples).
- Descubra cómo [Usar la API de REST de Intune](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/intune_graph_overview).
- Consulte el [registro de cambios](changelog.md) para obtener información sobre las novedades de la API de Intune.
- Explore los [ejemplos](https://developer.microsoft.com/es-ES/graph/graph/examples) para obtener más ideas sobre cómo usar Microsoft Graph.
