---
title: Actualizar windows10GeneralConfiguration
description: Actualice las propiedades de un objeto windows10GeneralConfiguration.
author: tfitzmac
ms.openlocfilehash: c135256fa93c202537729048caeac12ec169ba17
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322739"
---
# <a name="update-windows10generalconfiguration"></a>Actualizar windows10GeneralConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Boolean|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|windows10AppsForceUpdateSchedule|[windows10AppsForceUpdateSchedule](../resources/intune-deviceconfig-windows10appsforceupdateschedule.md)|Programación de actualización de Windows 10 force para las aplicaciones.|
|enableAutomaticRedeployment|Boolean|Permitir a los usuarios con derechos administrativos para eliminar todos los datos de usuario y la configuración con CTRL + Win + R en la pantalla de bloqueo de dispositivo para que pueda volver a configurar automáticamente el dispositivo y reinscrito en administración.|
|assignedAccessSingleModeUserName|String|Esta configuración de directiva permite que para definir la cuenta de usuario que se bloqueará al único modo de quiosco de aplicación.|
|assignedAccessSingleModeAppUserModelId|String|Esta configuración de directiva permite que para definir el identificador de modelo de usuario aplicación (AUMID) que se bloqueará al único modo de quiosco de aplicación.|
|microsoftAccountSignInAssistantSettings|[signInAssistantOptions](../resources/intune-deviceconfig-signinassistantoptions.md)|Controla el servicio NT de cuenta de inicio de sesión Ayudante de Microsoft (wlidsvc). Los valores posibles son: `notConfigured` y `disabled`.|
|authenticationAllowSecondaryDevice|Boolean|Permite que los dispositivos de autenticación secundario para que funcione con Windows.|
|authenticationAllowFIDODevice|Boolean|Indica si se va a permitir la autenticación mediante BOBI dispositivo (o nohttps://fidoalliance.org/)|
|cryptographyAllowFipsAlgorithmPolicy|Boolean|Especifique si desea permitir o no permitir la directiva de Federal Information Processing Standard (FIPS).|
|displayAppListWithGdiDPIScalingTurnedOn|Colección String|Lista de aplicaciones heredadas que tienen GDI activado de escala de PPP.|
|displayAppListWithGdiDPIScalingTurnedOff|Colección String|Lista de aplicaciones heredadas que tienen GDI desactivado de escala de PPP.|
|enterpriseCloudPrintDiscoveryEndPoint|String|Punto de conexión para la detección de impresoras en la nube.|
|enterpriseCloudPrintOAuthAuthority|String|Punto de conexión de autenticación para la adquisición de tokens de OAuth.|
|enterpriseCloudPrintOAuthClientIdentifier|String|GUID de una aplicación cliente autorizado a recuperar los tokens de OAuth de la autoridad OAuth.|
|enterpriseCloudPrintResourceIdentifier|String|URI del recurso de OAuth para el servicio de impresión, tal y como está configurado en el portal de Azure.|
|enterpriseCloudPrintDiscoveryMaxLimit|Int32|Número máximo de impresoras que se deben consultar desde un punto de conexión de detección. Se trata de una configuración solo para móviles. Valores válidos de 1 a 65535|
|enterpriseCloudPrintMopriaDiscoveryResourceIdentifier|String|URI del recurso de OAuth para la detección de impresoras, tal y como está configurado en el portal de Azure.|
|messagingBlockSync|Boolean|Indica si se deben bloquear el mensaje de texto copia de seguridad y restauración y mensajería en cualquier lugar.|
|messagingBlockMMS|Boolean|Indica si se va a bloquear o no el envío o recepción el MMS funcionalidad en el dispositivo.|
|messagingBlockRichCommunicationServices|Boolean|Indica si se va a bloquear o no el envío o recepción del conmutador funcionalidad en el dispositivo.|
|printerNames|Colección String|Aprovisionar automáticamente las impresoras en función de sus nombres (nombres de host de red).|
|printerDefaultName|String|Nombre (nombre de host de red) de una impresora instalada.|
|printerBlockAddition|Boolean|Impedir la instalación de usuario de impresoras adicionales de configuración de las impresoras.|
|searchBlockDiacritics|Boolean|Especifica si la búsqueda puede usar diacríticos.|
|searchDisableAutoLanguageDetection|Boolean|Especifica si se va a utilizar la detección automática de idioma al crear índices de contenido y propiedades.|
|searchDisableIndexingEncryptedItems|Boolean|Indica si se va a bloquear la indexación de los elementos protegidos mediante WIP para impedir que aparezcan en los resultados de búsqueda de Cortana o Explorer.|
|searchEnableRemoteQueries|Booleano|Indica si se van a bloquear las consultas remotas del índice de este equipo.|
|searchDisableUseLocation|Boolean|Especifica si búsqueda puede usar la información de ubicación.|
|searchDisableLocation|Boolean|Especifica si búsqueda puede usar la información de ubicación.|
|searchDisableIndexerBackoff|Boolean|Indica si se va a deshabilitar la característica que reduce la velocidad del indexador de búsqueda.|
|searchDisableIndexingRemovableDrive|Booleano|Indica si se va a permitir que los usuarios agreguen ubicaciones existentes en unidades extraíbles a las bibliotecas e indexarlas.|
|searchEnableAutomaticIndexSizeManangement|Boolean|Especifica la cantidad mínima de espacio en disco duro en la misma unidad que la ubicación del índice antes de detener la indexación.|
|searchBlockWebResults|Boolean|Indica si se deben bloquear la búsqueda en Internet.|
|securityBlockAzureADJoinedDevicesAutoEncryption|Boolean|Especifique si desea permitir el cifrado de automáticas de dispositivos durante OOBE cuando el dispositivo está Azure AD Unido (sólo escritorio).|
|diagnosticsDataSubmissionMode|[diagnosticDataSubmissionMode](../resources/intune-deviceconfig-diagnosticdatasubmissionmode.md)|Obtiene o establece un valor que permite que el dispositivo envíe datos de diagnóstico y telemetría de uso, como Watson. Los valores posibles son: `userDefined`, `none`, `basic`, `enhanced` y `full`.|
|oneDriveDisableFileSync|Booleano|Obtiene o establece un valor que permite que los administradores de TI impidan que las aplicaciones y características funcionen con archivos en OneDrive.|
|systemTelemetryProxyServer|String|Obtiene o establece el nombre de dominio completo (FQDN) o la dirección IP de un servidor proxy para reenviar solicitudes de telemetría y experiencias de usuario conectado.|
|inkWorkspaceAccess|[inkAccessSetting](../resources/intune-deviceconfig-inkaccesssetting.md)|Controla el acceso de usuarios al área de trabajo de entrada de lápiz, desde el escritorio y desde encima de la pantalla de bloqueo. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|inkWorkspaceAccessState|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Controla el acceso de usuarios al área de trabajo de entrada de lápiz, desde el escritorio y desde encima de la pantalla de bloqueo. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|inkWorkspaceBlockSuggestedApps|Boolean|Especifique si desea mostrar sugerencias de aplicación recomendada en el área de trabajo de entrada de lápiz.|
|smartScreenEnableAppInstallControl|Boolean|Permite que los administradores de TI controlen si los usuarios pueden instalar aplicaciones desde lugares que no sean la Tienda.|
|personalizationDesktopImageUrl|String|Dirección URL http o https a una imagen jpg, jpeg o png que debe descargarse y usarse como la imagen de escritorio, o dirección URL de archivo a una imagen local en el sistema de archivos que debe usarse como la imagen de escritorio.|
|personalizationLockScreenImageUrl|String|Dirección URL http o https a una imagen jpg, jpeg o png que debe descargarse y usarse como la imagen de pantalla de bloqueo, o dirección URL de archivo a una imagen local en el sistema de archivos que debe usarse como la imagen de pantalla de bloqueo.|
|bluetoothAllowedServices|Colección String|Especificar una lista de servicios y perfiles Bluetooth permitidos en cadenas de formato hexadecimal.|
|bluetoothBlockAdvertising|Boolean|Indica si se va a impedir que el usuario utilice anuncios de Bluetooth.|
|bluetoothBlockDiscoverableMode|Boolean|Indica si se va a impedir que el usuario utilice el modo visible de Bluetooth.|
|bluetoothBlockPrePairing|Boolean|Indica si se va a impedir que determinados periféricos Bluetooth agrupados se emparejen automáticamente con el dispositivo host.|
|edgeBlockAutofill|Boolean|Indica si se va a bloquear el autorrelleno.|
|edgeBlocked|Boolean|Indica si se va a impedir que el usuario utilice el explorador Edge.|
|edgeCookiePolicy|[edgeCookiePolicy](../resources/intune-deviceconfig-edgecookiepolicy.md)|Indica las cookies que se van a bloquear en el explorador Edge. Los valores posibles son: `userDefined`, `allow`, `blockThirdParty` y `blockAll`.|
|edgeBlockDeveloperTools|Boolean|Indica si se van a bloquear las herramientas de desarrollador en el explorador Edge.|
|edgeBlockSendingDoNotTrackHeader|Boolean|Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.|
|edgeBlockExtensions|Boolean|Indica si se van a bloquear las extensiones en el explorador Edge.|
|edgeBlockInPrivateBrowsing|Boolean|Indica si se va a bloquear la exploración de InPrivate en redes corporativas, en el explorador Edge.|
|edgeBlockJavaScript|Boolean|Indica si se va a impedir que el usuario utilice JavaScript.|
|edgeBlockPasswordManager|Boolean|Indica si se va a bloquear el administrador de contraseñas.|
|edgeBlockAddressBarDropdown|Boolean|Bloquear la funcionalidad de lista desplegable de la barra de direcciones en Microsoft Edge. Deshabilite esta opción para minimizar las conexiones de red de Microsoft Edge con servicios de Microsoft.|
|edgeBlockCompatibilityList|Boolean|Bloquear la lista de compatibilidad de Microsoft en Microsoft Edge. Esta lista de Microsoft ayuda a que Edge muestre correctamente los sitios con problemas de compatibilidad conocidos.|
|edgeClearBrowsingDataOnExit|Boolean|Borrar los datos de navegación al salir de Microsoft Edge.|
|edgeAllowStartPagesModification|Booleano|Permitir que los usuarios cambien las páginas de inicio en Edge. Use la propiedad EdgeHomepageUrls para especificar las páginas de inicio que vería el usuario de forma predeterminada al abrir Edge.|
|edgeDisableFirstRunPage|Boolean|Bloquear la página web de Microsoft que se abre la primera vez que se usa Microsoft Edge. Esta directiva permite que las empresas (por ejemplo, las inscritas en configuraciones de cero emisiones) bloqueen esta página.|
|edgeBlockLiveTileDataCollection|Booleano|Bloquear la recopilación de información por parte de Microsoft para la creación de iconos dinámicos cuando los usuarios anclan un sitio a la pantalla Inicio desde Microsoft Edge.|
|edgeSyncFavoritesWithInternetExplorer|Boolean|Habilitar la sincronización de favoritos entre Internet Explorer y Microsoft Edge. Las adiciones, los cambios de orden, las eliminaciones y las modificaciones de favoritos se comparten entre los dos exploradores.|
|edgeFavoritesListLocation|String|La ubicación de la lista de favoritos para aprovisionar. Puede ser un archivo local, la red local o la ubicación http.|
|edgeBlockEditFavorites|Boolean|Indica si se deben bloquear al usuario de hacer cambios en los favoritos.|
|cellularBlockDataWhenRoaming|Boolean|Indica si se va a impedir que el usuario utilice los datos móviles en itinerancia.|
|cellularBlockVpn|Boolean|Indica si se va a impedir que el usuario utilice VPN en redes de telefonía móvil.|
|cellularBlockVpnWhenRoaming|Boolean|Indica si se va a impedir que el usuario utilice VPN en redes de telefonía móvil en itinerancia.|
|cellularData|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Si desea permitir que el canal de conexión de datos en el dispositivo. Si no configurado, se permite el canal de conexión de datos y el usuario puede desactivarla. Los valores posibles son: `blocked`, `required` y `allowed`.|
|defenderBlockEndUserAccess|Boolean|Indica si se va a impedir que el usuario final tenga acceso a Defender.|
|defenderDaysBeforeDeletingQuarantinedMalware|Int32|Número de días antes de que se elimine el malware en cuarentena. Valores válidos de 0 a 90.|
|defenderDetectedMalwareActions|[defenderDetectedMalwareActions](../resources/intune-deviceconfig-defenderdetectedmalwareactions.md)|Obtiene o especifica las acciones de Defender para el malware detectado por nivel de amenaza.|
|defenderSystemScanSchedule|[weeklySchedule](../resources/intune-deviceconfig-weeklyschedule.md)|Día de la semana para el análisis del sistema de Defender. Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.|
|defenderFilesAndFoldersToExclude|Colección String|Archivos y carpetas que se van a excluir de los análisis y la protección en tiempo real.|
|defenderFileExtensionsToExclude|Colección String|Extensiones de archivo que se van a excluir de los análisis y la protección en tiempo real.|
|defenderScanMaxCpu|Int32|Porcentaje máximo de uso de CPU durante el análisis. Valores válidos de 0 a 100.|
|defenderMonitorFileActivity|[defenderMonitorFileActivity](../resources/intune-deviceconfig-defendermonitorfileactivity.md)|Valor para supervisar la actividad de archivo. Los valores posibles son: `userDefined`, `disable`, `monitorAllFiles`, `monitorIncomingFilesOnly` y `monitorOutgoingFilesOnly`.|
|defenderPotentiallyUnwantedAppAction|[defenderPotentiallyUnwantedAppAction](../resources/intune-deviceconfig-defenderpotentiallyunwantedappaction.md)|Obtiene o establece la acción de Defender que se realizará en potencialmente no deseados aplicación (PUA), que incluye el software con comportamientos de inserción de ad, solicitud de agrupación y persistentes de software de pago o suscripción, etcetera. Usuario de alertas de Defender cuando PUA se está descargando o intenta instalar propio. Agregado en 10 de Windows para escritorio. Los valores posibles son: `deviceDefault`, `block` y `audit`.|
|defenderPotentiallyUnwantedAppActionSetting|[defenderProtectionType](../resources/intune-deviceconfig-defenderprotectiontype.md)|Obtiene o establece la acción de Defender que se realizará en potencialmente no deseados aplicación (PUA), que incluye el software con comportamientos de inserción de ad, solicitud de agrupación y persistentes de software de pago o suscripción, etcetera. Usuario de alertas de Defender cuando PUA se está descargando o intenta instalar propio. Agregado en 10 de Windows para escritorio. Los valores posibles son: `userDefined`, `enable` y `auditMode`.|
|defenderProcessesToExclude|Colección String|Procesos que se van a excluir de los análisis y la protección en tiempo real.|
|defenderPromptForSampleSubmission|[defenderPromptForSampleSubmission](../resources/intune-deviceconfig-defenderpromptforsamplesubmission.md)|Configuración de cómo solicitar al usuario el envío de muestras. Los valores posibles son: `userDefined`, `alwaysPrompt`, `promptBeforeSendingPersonalData`, `neverSendData` y `sendAllDataWithoutPrompting`.|
|defenderRequireBehaviorMonitoring|Boolean|Indica si se va a requerir la supervisión de comportamiento.|
|defenderRequireCloudProtection|Boolean|Indica si se va a requerir la protección en la nube.|
|defenderRequireNetworkInspectionSystem|Boolean|Indica si se va a requerir el sistema de inspección de red.|
|defenderRequireRealTimeMonitoring|Booleano|Indica si se va a requerir la supervisión en tiempo real.|
|defenderScanArchiveFiles|Boolean|Indica si se van a examinar archivos de almacenamiento.|
|defenderScanDownloads|Booleano|Indica si se van a examinar las descargas.|
|defenderScanNetworkFiles|Booleano|Indica si se van a examinar los archivos abiertos desde una carpeta de red.|
|defenderScanIncomingMail|Boolean|Indica si se van a examinar los mensajes de correo entrante.|
|defenderScanMappedNetworkDrivesDuringFullScan|Boolean|Indica si se van a analizar las unidades de red asignadas durante el análisis completo.|
|defenderScanRemovableDrivesDuringFullScan|Boolean|Indica si se van a analizar las unidades extraíbles durante el análisis completo.|
|defenderScanScriptsLoadedInInternetExplorer|Boolean|Indica si se van a analizar scripts cargados en el explorador Internet Explorer.|
|defenderSignatureUpdateIntervalInHours|Int32|Intervalo de actualización de la firma en horas. Especifique 0 para no comprobarla. Valores válidos de 0 a 24|
|defenderScanType|[defenderScanType](../resources/intune-deviceconfig-defenderscantype.md)|Tipo de análisis del sistema de Defender. Los valores posibles son: `userDefined`, `disabled`, `quick` y `full`.|
|defenderScheduledScanTime|TimeOfDay|Hora de Defender para el análisis del sistema.|
|defenderScheduledQuickScanTime|TimeOfDay|Hora en la que se realiza un análisis rápido diariamente.|
|defenderCloudBlockLevel|[defenderCloudBlockLevelType](../resources/intune-deviceconfig-defendercloudblockleveltype.md)|Especifica el nivel de protección que proporciona la nube. Los valores posibles son: `notConfigured`, `high`, `highPlus` y `zeroTolerance`.|
|defenderCloudExtendedTimeout|Int32|Extensión de tiempo de espera para el archivo de examen de la nube. Valores válidos de 0 a 50.|
|defenderCloudExtendedTimeoutInSeconds|Int32|Extensión de tiempo de espera para el archivo de examen de la nube. Valores válidos de 0 a 50.|
|defenderBlockOnAccessProtection|Boolean|Permiten o impiden la funcionalidad de Windows Defender en protección de acceso.|
|defenderScheduleScanDay|[defenderScheduleScanDay](../resources/intune-deviceconfig-defenderschedulescanday.md)|Selecciona el día en que se debe ejecutar el examen de Windows Defender. Los valores posibles son: `everyday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday` y `noScheduledScan`.|
|defenderSubmitSamplesConsentType|[defenderSubmitSamplesConsentType](../resources/intune-deviceconfig-defendersubmitsamplesconsenttype.md)|Comprueba si el usuario da su consentimiento nivel en Windows Defender para enviar datos. Los valores posibles son: `sendSafeSamplesAutomatically`, `alwaysPrompt`, `neverSend` y `sendAllSamplesAutomatically`.|
|lockScreenAllowTimeoutConfiguration|Boolean|Especifica si se mostrará una opción configurable por el usuario para controlar el tiempo de espera de la pantalla mientras se está en la pantalla de bloqueo de dispositivos Windows 10 Mobile. Si esta directiva está establecida en Permitir, se ignora el valor establecido por lockScreenTimeoutInSeconds.|
|lockScreenBlockActionCenterNotifications|Boolean|Indica si se van a bloquear las notificaciones del centro de acciones en la pantalla de bloqueo.|
|lockScreenBlockCortana|Booleano|Indica si el usuario puede interactuar con Cortana mediante la voz mientras el sistema está bloqueado.|
|lockScreenBlockToastNotifications|Boolean|Indica si se permiten las notificaciones del sistema por encima de la pantalla de bloqueo del dispositivo.|
|lockScreenTimeoutInSeconds|Int32|Establecer la duración (en segundos) entre el bloqueo de la pantalla y su desactivación en dispositivos Windows 10 Mobile. Los valores admitidos son de 11 a 1800. Valores válidos de 11 a 1800|
|passwordBlockSimple|Boolean|Especifique si se permiten números PIN o contraseñas, como "1111" o "1234". En equipos de escritorio Windows 10, también controla el uso de contraseñas de imagen.|
|passwordExpirationDays|Int32|La expiración de la contraseña en días. Valores válidos de 0 a 730.|
|passwordMinimumLength|Int32|La longitud mínima de contraseña. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordMinimumCharacterSetCount|Int32|Número de juegos de caracteres necesarios en la contraseña.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que impiden su reutilización. Valores válidos de 0 a 50.|
|passwordRequired|Boolean|Indica si se va a requerir que el usuario tenga una contraseña.|
|passwordRequireWhenResumeFromIdleState|Booleano|Indica si se va a requerir una contraseña al reanudar desde un estado inactivo.|
|passwordRequiredType|[requiredPasswordType](../resources/intune-deviceconfig-requiredpasswordtype.md)|Tipo de contraseña necesaria. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica. Valores válidos de 0 a 999.|
|passwordMinimumAgeInDays|Int32|Esta configuración de seguridad determina el período de tiempo (en días) que debe ser una contraseña utilizada antes de que el usuario puede cambiarla. Valores válidos de 0 a 998|
|privacyAdvertisingId|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Habilita o deshabilita el uso del identificador de publicidad. Se agregó en Windows 10, versión 1607. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|privacyAutoAcceptPairingAndConsentPrompts|Boolean|Indica si se va a permitir la aceptación automática de los cuadros de diálogo de consentimiento del usuario de emparejamiento y privacidad al iniciar aplicaciones.|
|privacyBlockInputPersonalization|Booleano|Indica si se va a bloquear el uso de servicios de voz basados en la nube de Cortana, el dictado o las aplicaciones de la tienda.|
|privacyBlockPublishUserActivities|Boolean|Bloquea la detección/experiencias compartida de recursos usados recientemente en el conmutador de tareas de etcetera.|
|privacyBlockActivityFeed|Boolean|Bloquea el uso de servicios de nube en función de voz para Cortana, Dictation o almacén de aplicaciones.|
|startBlockUnpinningAppsFromTaskbar|Boolean|Indica si se va a impedir que el usuario desancle aplicaciones de la barra de tareas.|
|startMenuAppListVisibility|[windowsStartMenuAppListVisibilityType](../resources/intune-deviceconfig-windowsstartmenuapplistvisibilitytype.md)|Al configurar este valor, se contrae la lista de aplicaciones, se quita la lista de aplicaciones por completo o se deshabilita la alternancia correspondiente en la aplicación Configuración. Los valores posibles son: `userDefined`, `collapse`, `remove` y `disableSettingsApp`.|
|startMenuHideChangeAccountSettings|Boolean|Al habilitar esta directiva, se impide que la opción Cambiar configuración de cuenta aparezca en el icono de usuario del menú Inicio.|
|startMenuHideFrequentlyUsedApps|Boolean|Al habilitar esta directiva, se ocultan la mayoría de las aplicaciones usadas en el menú Inicio y se deshabilita la conmutación correspondiente en la aplicación Configuración.|
|startMenuHideHibernate|Boolean|Al habilitar esta directiva, se oculta la opción de hibernación en el botón de encendido del menú Inicio.|
|startMenuHideLock|Boolean|Al habilitar esta directiva, se oculta la opción de bloqueo en el icono de usuario del menú Inicio.|
|startMenuHidePowerButton|Boolean|Al habilitar esta directiva, se oculta el botón de encendido del menú Inicio.|
|startMenuHideRecentJumpLists|Boolean|Al habilitar esta directiva, se ocultan las listas de accesos directos recientes en el menú Inicio o la barra de tareas y se deshabilita la alternancia correspondiente en la aplicación Configuración.|
|startMenuHideRecentlyAddedApps|Boolean|Al habilitar esta directiva, se ocultan las aplicaciones agregadas recientemente en el menú Inicio y se deshabilita la alternancia correspondiente en la aplicación Configuración.|
|startMenuHideRestartOptions|Boolean|Al habilitar esta directiva, se ocultan las opciones de reinicio/actualización y reinicio en el botón de encendido del menú Inicio.|
|startMenuHideShutDown|Boolean|Al habilitar esta directiva, se ocultan las opciones de apagado/actualización y apagado en el botón de encendido del menú Inicio.|
|startMenuHideSignOut|Boolean|Al habilitar esta directiva, se oculta la opción Cerrar sesión en el icono de usuario del menú Inicio.|
|startMenuHideSleep|Boolean|Al habilitar esta directiva, se oculta la opción Suspender en el botón de apagado del menú Inicio.|
|startMenuHideSwitchAccount|Boolean|Al habilitar esta directiva, se oculta la opción Cambiar de cuenta en el icono de usuario del menú Inicio.|
|startMenuHideUserTile|Boolean|Al habilitar esta directiva, se oculta el icono de usuario del menú Inicio.|
|startMenuLayoutEdgeAssetsXml|Binario|Esta configuración de directiva permite importar los recursos de Microsoft Edge que se van a usar con la directiva startMenuLayoutXml. El diseño de la pantalla de inicio puede contener un icono secundario de la aplicación Microsoft Edge que busca el archivo de recursos locales de Edge. En este caso, el recurso local de Microsoft Edge no existirá y hará que el icono secundario de Microsoft Edge aparezca vacío. Esta directiva solo se aplica cuando se modifica la directiva startMenuLayoutXml. El valor debe ser una matriz de bytes codificada base64 UTF8.|
|startMenuLayoutXml|Binario|Permite que los administradores invaliden el diseño predeterminado del menú Inicio e impide que el usuario lo cambie. Para modificar el diseño, se especifica un archivo XML basado en el esquema de modificación del diseño. El archivo XML debe estar en un formato de matriz de bytes codificada UTF8.|
|startMenuMode|[windowsStartMenuModeType](../resources/intune-deviceconfig-windowsstartmenumodetype.md)|Permite que los administradores decidan cómo se muestra el menú Inicio. Los valores posibles son: `userDefined`, `fullScreen` y `nonFullScreen`.|
|startMenuPinnedFolderDocuments|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Documentos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderDownloads|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Documentos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderFileExplorer|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Explorador de archivos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderHomeGroup|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Grupo Hogar en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderMusic|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Música en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderNetwork|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Red en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderPersonalFolder|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Personal en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderPictures|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Imágenes en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderSettings|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Configuración en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|startMenuPinnedFolderVideos|[visibilitySetting](../resources/intune-deviceconfig-visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Vídeos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide` y `show`.|
|settingsBlockSettingsApp|Boolean|Indica si se va a bloquear el acceso a la aplicación Ajustes.|
|settingsBlockSystemPage|Boolean|Indica si se va a bloquear el acceso a Sistema en la aplicación Ajustes.|
|settingsBlockDevicesPage|Boolean|Indica si se va a bloquear el acceso a Dispositivos en la aplicación Ajustes.|
|settingsBlockNetworkInternetPage|Boolean|Indica si se va a bloquear el acceso a Red e Internet en la aplicación Ajustes.|
|settingsBlockPersonalizationPage|Boolean|Indica si se va a bloquear el acceso a Personalización en la aplicación Ajustes.|
|settingsBlockAccountsPage|Boolean|Indica si se va a bloquear el acceso a Cuentas en la aplicación Ajustes.|
|settingsBlockTimeLanguagePage|Boolean|Indica si se va a bloquear el acceso a Hora e idioma en la aplicación Ajustes.|
|settingsBlockEaseOfAccessPage|Boolean|Indica si se va a bloquear el acceso a Accesibilidad en la aplicación Ajustes.|
|settingsBlockPrivacyPage|Boolean|Indica si se va a bloquear el acceso a Privacidad en la aplicación Ajustes.|
|settingsBlockUpdateSecurityPage|Boolean|Indica si se va a bloquear el acceso a Actualización y seguridad en la aplicación Ajustes.|
|settingsBlockAppsPage|Boolean|Indica si se va a bloquear el acceso a Aplicaciones en la aplicación Ajustes.|
|settingsBlockGamingPage|Boolean|Indica si se va a bloquear el acceso a Juegos en la aplicación Ajustes.|
|windowsSpotlightBlockConsumerSpecificFeatures|Boolean|Permite que los administradores de TI bloqueen experiencias que suelen ser solo para consumidores, como las sugerencias de inicio, las notificaciones de suscripción, la instalación de aplicaciones post-OOBE y los iconos de redireccionamiento.|
|windowsSpotlightBlocked|Boolean|Permite que los administradores de TI desactiven todas las características de Contenido destacado de Windows.|
|windowsSpotlightBlockOnActionCenter|Booleano|Bloquear las sugerencias de Microsoft que se muestran después de cada instalación limpia del sistema operativo, actualización o de forma continua para presentar a los usuarios los cambios y novedades.|
|windowsSpotlightBlockTailoredExperiences|Boolean|Bloquear el contenido personalizado del Contenido destacado de Windows según el uso del dispositivo del usuario.|
|windowsSpotlightBlockThirdPartyNotifications|Boolean|Bloquear contenido de terceros que se envía a través del Contenido destacado de Windows.|
|windowsSpotlightBlockWelcomeExperience|Boolean|Bloquear la experiencia de bienvenida de Windows del Contenido destacado de Windows.|
|windowsSpotlightBlockWindowsTips|Boolean|Permite que los administradores de TI desactiven el elemento emergente Sugerencias de Windows.|
|windowsSpotlightConfigureOnLockScreen|[windowsSpotlightEnablementSettings](../resources/intune-deviceconfig-windowsspotlightenablementsettings.md)|Especifica el tipo de luz de foco. Los valores posibles son: `notConfigured`, `disabled` y `enabled`.|
|networkProxyApplySettingsDeviceWide|Boolean|Si se establece, la configuración de proxy se aplicará a todos los procesos y cuentas en el dispositivo. En caso contrario, se aplicará a la cuenta de usuario que está inscrita en MDM.|
|networkProxyDisableAutoDetect|Boolean|Deshabilitar la detección automática de la configuración. Si está habilitada, el sistema intentará encontrar la ruta de acceso a un script de configuración automática de proxy (PAC).|
|networkProxyAutomaticConfigurationUrl|String|Dirección al script de configuración automática de proxy (PAC) que quiera usar.|
|networkProxyServer|[windows10NetworkProxyServer](../resources/intune-deviceconfig-windows10networkproxyserver.md)|Especifica la configuración manual del servidor proxy.|
|accountsBlockAddingNonMicrosoftAccountEmail|Boolean|Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas a una cuenta de Microsoft.|
|antiTheftModeBlocked|Booleano|Indica si se va a impedir que el usuario seleccione una preferencia de modo antirrobo (solo Windows 10 Mobile).|
|bluetoothBlocked|Boolean|Indica si se va a impedir que el usuario utilice Bluetooth.|
|cameraBlocked|Boolean|Indica si se va a impedir que el usuario tenga acceso a la cámara del dispositivo.|
|connectedDevicesServiceBlocked|Boolean|Indica si se va a bloquear el servicio de dispositivos conectados que permite la detección y conexión con otros dispositivos, la mensajería remota, las sesiones de aplicación remota y otras experiencias entre dispositivos.|
|certificatesBlockManualRootCertificateInstallation|Boolean|Indica si se va a impedir que el usuario instale manualmente el certificado raíz.|
|copyPasteBlocked|Boolean|Indica si se va a impedir que el usuario utilice la opción de copiar y pegar.|
|cortanaBlocked|Boolean|Indica si se va a impedir que el usuario utilice Cortana.|
|deviceManagementBlockFactoryResetOnMobile|Boolean|Indica si se va a impedir que el usuario restablezca el teléfono.|
|deviceManagementBlockManualUnenroll|Boolean|Indica si se va a impedir que el usuario realice una anulación manual de la inscripción desde la administración del dispositivo.|
|safeSearchFilter|[safeSearchFilterType](../resources/intune-deviceconfig-safesearchfiltertype.md)|Especifica el nivel de filtro de búsqueda segura que es necesario. Los valores posibles son: `userDefined`, `strict` y `moderate`.|
|edgeBlockPopups|Boolean|Indica si se van a bloquear los elementos emergentes.|
|edgeBlockSearchSuggestions|Boolean|Indica si se va a impedir que el usuario utilice las sugerencias de búsqueda en la barra de direcciones.|
|edgeBlockSendingIntranetTrafficToInternetExplorer|Boolean|Indica si se va a impedir que el usuario envíe tráfico de Intranet a Internet Explorer desde Edge.|
|edgeRequireSmartScreen|Boolean|Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.|
|edgeEnterpriseModeSiteListLocation|String|Indica la ubicación de la lista de sitios del modo de empresa. Puede ser un archivo local, la red local o la ubicación http.|
|edgeFirstRunUrl|String|Primera dirección URL que se ejecuta al abrir el explorador Edge por primera vez.|
|edgeSearchEngine|[edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)|Permite que los administradores de TI configuren un motor de búsqueda predeterminado para dispositivos controlados por MDM. Los usuarios pueden invalidarla y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.|
|edgeHomepageUrls|Colección String|Lista de direcciones URL de páginas principales que se muestran en dispositivos inscritos en MDM en el explorador Edge.|
|edgeBlockAccessToAboutFlags|Boolean|Indica si se va a impedir el acceso a las marcas de información en el explorador Edge.|
|smartScreenBlockPromptOverride|Boolean|Indica si los usuarios pueden invalidar las advertencias de filtro SmartScreen sobre sitios web potencialmente malintencionados.|
|smartScreenBlockPromptOverrideForFiles|Booleano|Indica si los usuarios pueden invalidar las advertencias del filtro SmartScreen sobre la descarga de archivos no comprobados.|
|webRtcBlockLocalhostIpAddress|Boolean|Indica si se muestra la dirección IP de Localhost del usuario durante las llamadas telefónicas mediante WebRTC|
|internetSharingBlocked|Boolean|Indica si se va a impedir que el usuario utilice el uso compartido de Internet.|
|settingsBlockAddProvisioningPackage|Boolean|Indica si se va a impedir que el usuario instale paquetes de aprovisionamiento.|
|settingsBlockRemoveProvisioningPackage|Boolean|Indica si se va a impedir que el agente de configuración en tiempo de ejecución quite los paquetes de aprovisionamiento.|
|settingsBlockChangeSystemTime|Boolean|Indica si se va a impedir que el usuario cambie los ajustes de fecha y hora.|
|settingsBlockEditDeviceName|Boolean|Indica si se va a impedir que el usuario edite el nombre del dispositivo.|
|settingsBlockChangeRegion|Boolean|Indica si se va a impedir que el usuario cambie los ajustes de región.|
|settingsBlockChangeLanguage|Boolean|Indica si se va a impedir que el usuario cambie los ajustes de idioma.|
|settingsBlockChangePowerSleep|Boolean|Indica si se va a impedir que el usuario cambie los ajustes de inicio/apagado y suspensión.|
|locationServicesBlocked|Boolean|Indica si se va a impedir que el usuario utilice los servicios de ubicación.|
|microsoftAccountBlocked|Boolean|Indica si se va a bloquear una cuenta de Microsoft.|
|microsoftAccountBlockSettingsSync|Boolean|Indica si se va a bloquear la sincronización de la configuración de una cuenta de Microsoft.|
|nfcBlocked|Boolean|Indica si se va a impedir que el usuario utilice la transmisión de datos en proximidad.|
|resetProtectionModeBlocked|Boolean|Indica si se va a impedir que el usuario restablezca el modo de protección.|
|screenCaptureBlocked|Boolean|Indica si se va a impedir que el usuario tome capturas de pantalla.|
|storageBlockRemovableStorage|Boolean|Indica si se va a impedir que el usuario utilice almacenamiento extraíble.|
|storageRequireMobileDeviceEncryption|Boolean|Indica si se va a requerir el cifrado en un dispositivo móvil.|
|usbBlocked|Boolean|Indica si se va a impedir que el usuario realice conexiones USB.|
|voiceRecordingBlocked|Boolean|Indica si se va a impedir que el usuario grabe voz.|
|wiFiBlockAutomaticConnectHotspots|Boolean|Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi. No tiene impacto si se bloquea el Wi-Fi.|
|wiFiBlocked|Boolean|Indica si se va a impedir que el usuario utilice Wi-Fi.|
|wiFiBlockManualConfiguration|Boolean|Indica si se va a impedir que el usuario realice la configuración manual de Wi-Fi.|
|wiFiScanInterval|Int32|Especificar la frecuencia con la que los dispositivos buscan redes Wi-Fi. Los valores admitidos son de 1 a 500, donde 100 = predeterminado y 500 = baja frecuencia. Valores válidos de 1 a 500.|
|wirelessDisplayBlockProjectionToThisDevice|Boolean|Indica si se va a permitir que otros dispositivos detecten este equipo para proyección.|
|wirelessDisplayBlockUserInputFromReceiver|Boolean|Indica si se va a permitir la entrada del usuario desde un receptor de visualización inalámbrico.|
|wirelessDisplayRequirePinForPairing|Boolean|Indica si se va a requerir un PIN para iniciar el emparejamiento con nuevos dispositivos.|
|windowsStoreBlocked|Booleano|Indica si se va a impedir que el usuario utilice la Tienda Windows.|
|appsAllowTrustedAppsSideloading|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Indica si las aplicaciones de paquetes AppX firmados con un certificado de confianza se pueden cargar lateralmente. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|windowsStoreBlockAutoUpdate|Boolean|Indica si se va a bloquear la actualización automática de aplicaciones desde la Tienda Windows.|
|developerUnlockSetting|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Indica si se va a permitir el desbloqueo de desarrollador. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|sharedUserAppDataAllowed|Boolean|Indica si se va a impedir que varios usuarios de la misma aplicación compartan datos.|
|appsBlockWindowsStoreOriginatedApps|Boolean|Indica si se va a deshabilitar el inicio de todas las aplicaciones que vienen preinstaladas o que se han descargado desde la Tienda Windows.|
|windowsStoreEnablePrivateStoreOnly|Boolean|Indica si se va a habilitar solo la tienda privada.|
|storageRestrictAppDataToSystemVolume|Boolean|Indica si los datos de la aplicación están restringidos a la unidad del sistema.|
|storageRestrictAppInstallToSystemVolume|Boolean|Indica si la instalación de la aplicación está restringida a la unidad del sistema.|
|gameDvrBlocked|Boolean|Indica si se va a bloquear la DVR y la difusión.|
|experienceBlockDeviceDiscovery|Boolean|Indica si se va a habilitar la experiencia de usuario de detección de dispositivos.|
|experienceBlockErrorDialogWhenNoSIM|Boolean|Indica si se va a permitir que se muestre el cuadro de diálogo de error si no se detecta ninguna tarjeta SIM.|
|experienceBlockTaskSwitcher|Boolean|Indica si se va a habilitar el cambio de tarea en el dispositivo.|
|logonBlockFastUserSwitching|Booleano|Deshabilita la posibilidad de cambiar rápidamente entre usuarios que han iniciado sesión a la vez sin cerrar la sesión.|
|tenantLockdownRequireNetworkDuringOutOfBoxExperience|Boolean|Si el dispositivo es necesario para conectarse a la red.|
|appManagementMSIAllowUserControlOverInstall|Boolean|Esta configuración de directiva permite a los usuarios cambiar las opciones de instalación que normalmente están disponibles sólo para los administradores del sistema.|
|appManagementMSIAlwaysInstallWithElevatedPrivileges|Boolean|Esta configuración de directiva indica a Windows Installer que use permisos elevados cuando instala cualquier programa en el sistema.|
|dataProtectionBlockDirectMemoryAccess|Boolean|Esta configuración de directiva permite bloquear el acceso directo a memoria (DMA) para todos los hot acoplable PCI puertos dirección descendente hasta que un usuario inicia sesión en Windows.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 12134

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "windows10AppsForceUpdateSchedule": {
    "@odata.type": "microsoft.graph.windows10AppsForceUpdateSchedule",
    "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
    "recurrence": "daily",
    "runImmediatelyIfAfterStartDateTime": true
  },
  "enableAutomaticRedeployment": true,
  "assignedAccessSingleModeUserName": "Assigned Access Single Mode User Name value",
  "assignedAccessSingleModeAppUserModelId": "Assigned Access Single Mode App User Model Id value",
  "microsoftAccountSignInAssistantSettings": "disabled",
  "authenticationAllowSecondaryDevice": true,
  "authenticationAllowFIDODevice": true,
  "cryptographyAllowFipsAlgorithmPolicy": true,
  "displayAppListWithGdiDPIScalingTurnedOn": [
    "Display App List With Gdi DPIScaling Turned On value"
  ],
  "displayAppListWithGdiDPIScalingTurnedOff": [
    "Display App List With Gdi DPIScaling Turned Off value"
  ],
  "enterpriseCloudPrintDiscoveryEndPoint": "Enterprise Cloud Print Discovery End Point value",
  "enterpriseCloudPrintOAuthAuthority": "Enterprise Cloud Print OAuth Authority value",
  "enterpriseCloudPrintOAuthClientIdentifier": "Enterprise Cloud Print OAuth Client Identifier value",
  "enterpriseCloudPrintResourceIdentifier": "Enterprise Cloud Print Resource Identifier value",
  "enterpriseCloudPrintDiscoveryMaxLimit": 5,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "Enterprise Cloud Print Mopria Discovery Resource Identifier value",
  "messagingBlockSync": true,
  "messagingBlockMMS": true,
  "messagingBlockRichCommunicationServices": true,
  "printerNames": [
    "Printer Names value"
  ],
  "printerDefaultName": "Printer Default Name value",
  "printerBlockAddition": true,
  "searchBlockDiacritics": true,
  "searchDisableAutoLanguageDetection": true,
  "searchDisableIndexingEncryptedItems": true,
  "searchEnableRemoteQueries": true,
  "searchDisableUseLocation": true,
  "searchDisableLocation": true,
  "searchDisableIndexerBackoff": true,
  "searchDisableIndexingRemovableDrive": true,
  "searchEnableAutomaticIndexSizeManangement": true,
  "searchBlockWebResults": true,
  "securityBlockAzureADJoinedDevicesAutoEncryption": true,
  "diagnosticsDataSubmissionMode": "none",
  "oneDriveDisableFileSync": true,
  "systemTelemetryProxyServer": "System Telemetry Proxy Server value",
  "inkWorkspaceAccess": "enabled",
  "inkWorkspaceAccessState": "blocked",
  "inkWorkspaceBlockSuggestedApps": true,
  "smartScreenEnableAppInstallControl": true,
  "personalizationDesktopImageUrl": "https://example.com/personalizationDesktopImageUrl/",
  "personalizationLockScreenImageUrl": "https://example.com/personalizationLockScreenImageUrl/",
  "bluetoothAllowedServices": [
    "Bluetooth Allowed Services value"
  ],
  "bluetoothBlockAdvertising": true,
  "bluetoothBlockDiscoverableMode": true,
  "bluetoothBlockPrePairing": true,
  "edgeBlockAutofill": true,
  "edgeBlocked": true,
  "edgeCookiePolicy": "allow",
  "edgeBlockDeveloperTools": true,
  "edgeBlockSendingDoNotTrackHeader": true,
  "edgeBlockExtensions": true,
  "edgeBlockInPrivateBrowsing": true,
  "edgeBlockJavaScript": true,
  "edgeBlockPasswordManager": true,
  "edgeBlockAddressBarDropdown": true,
  "edgeBlockCompatibilityList": true,
  "edgeClearBrowsingDataOnExit": true,
  "edgeAllowStartPagesModification": true,
  "edgeDisableFirstRunPage": true,
  "edgeBlockLiveTileDataCollection": true,
  "edgeSyncFavoritesWithInternetExplorer": true,
  "edgeFavoritesListLocation": "Edge Favorites List Location value",
  "edgeBlockEditFavorites": true,
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
  "cellularData": "required",
  "defenderBlockEndUserAccess": true,
  "defenderDaysBeforeDeletingQuarantinedMalware": 12,
  "defenderDetectedMalwareActions": {
    "@odata.type": "microsoft.graph.defenderDetectedMalwareActions",
    "lowSeverity": "clean",
    "moderateSeverity": "clean",
    "highSeverity": "clean",
    "severeSeverity": "clean"
  },
  "defenderSystemScanSchedule": "everyday",
  "defenderFilesAndFoldersToExclude": [
    "Defender Files And Folders To Exclude value"
  ],
  "defenderFileExtensionsToExclude": [
    "Defender File Extensions To Exclude value"
  ],
  "defenderScanMaxCpu": 2,
  "defenderMonitorFileActivity": "disable",
  "defenderPotentiallyUnwantedAppAction": "block",
  "defenderPotentiallyUnwantedAppActionSetting": "enable",
  "defenderProcessesToExclude": [
    "Defender Processes To Exclude value"
  ],
  "defenderPromptForSampleSubmission": "alwaysPrompt",
  "defenderRequireBehaviorMonitoring": true,
  "defenderRequireCloudProtection": true,
  "defenderRequireNetworkInspectionSystem": true,
  "defenderRequireRealTimeMonitoring": true,
  "defenderScanArchiveFiles": true,
  "defenderScanDownloads": true,
  "defenderScanNetworkFiles": true,
  "defenderScanIncomingMail": true,
  "defenderScanMappedNetworkDrivesDuringFullScan": true,
  "defenderScanRemovableDrivesDuringFullScan": true,
  "defenderScanScriptsLoadedInInternetExplorer": true,
  "defenderSignatureUpdateIntervalInHours": 6,
  "defenderScanType": "disabled",
  "defenderScheduledScanTime": "11:59:10.9990000",
  "defenderScheduledQuickScanTime": "11:58:49.3840000",
  "defenderCloudBlockLevel": "high",
  "defenderCloudExtendedTimeout": 12,
  "defenderCloudExtendedTimeoutInSeconds": 5,
  "defenderBlockOnAccessProtection": true,
  "defenderScheduleScanDay": "monday",
  "defenderSubmitSamplesConsentType": "alwaysPrompt",
  "lockScreenAllowTimeoutConfiguration": true,
  "lockScreenBlockActionCenterNotifications": true,
  "lockScreenBlockCortana": true,
  "lockScreenBlockToastNotifications": true,
  "lockScreenTimeoutInSeconds": 10,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "passwordRequireWhenResumeFromIdleState": true,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordMinimumAgeInDays": 8,
  "privacyAdvertisingId": "blocked",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
  "privacyBlockPublishUserActivities": true,
  "privacyBlockActivityFeed": true,
  "startBlockUnpinningAppsFromTaskbar": true,
  "startMenuAppListVisibility": "collapse",
  "startMenuHideChangeAccountSettings": true,
  "startMenuHideFrequentlyUsedApps": true,
  "startMenuHideHibernate": true,
  "startMenuHideLock": true,
  "startMenuHidePowerButton": true,
  "startMenuHideRecentJumpLists": true,
  "startMenuHideRecentlyAddedApps": true,
  "startMenuHideRestartOptions": true,
  "startMenuHideShutDown": true,
  "startMenuHideSignOut": true,
  "startMenuHideSleep": true,
  "startMenuHideSwitchAccount": true,
  "startMenuHideUserTile": true,
  "startMenuLayoutEdgeAssetsXml": "c3RhcnRNZW51TGF5b3V0RWRnZUFzc2V0c1htbA==",
  "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s",
  "startMenuMode": "fullScreen",
  "startMenuPinnedFolderDocuments": "hide",
  "startMenuPinnedFolderDownloads": "hide",
  "startMenuPinnedFolderFileExplorer": "hide",
  "startMenuPinnedFolderHomeGroup": "hide",
  "startMenuPinnedFolderMusic": "hide",
  "startMenuPinnedFolderNetwork": "hide",
  "startMenuPinnedFolderPersonalFolder": "hide",
  "startMenuPinnedFolderPictures": "hide",
  "startMenuPinnedFolderSettings": "hide",
  "startMenuPinnedFolderVideos": "hide",
  "settingsBlockSettingsApp": true,
  "settingsBlockSystemPage": true,
  "settingsBlockDevicesPage": true,
  "settingsBlockNetworkInternetPage": true,
  "settingsBlockPersonalizationPage": true,
  "settingsBlockAccountsPage": true,
  "settingsBlockTimeLanguagePage": true,
  "settingsBlockEaseOfAccessPage": true,
  "settingsBlockPrivacyPage": true,
  "settingsBlockUpdateSecurityPage": true,
  "settingsBlockAppsPage": true,
  "settingsBlockGamingPage": true,
  "windowsSpotlightBlockConsumerSpecificFeatures": true,
  "windowsSpotlightBlocked": true,
  "windowsSpotlightBlockOnActionCenter": true,
  "windowsSpotlightBlockTailoredExperiences": true,
  "windowsSpotlightBlockThirdPartyNotifications": true,
  "windowsSpotlightBlockWelcomeExperience": true,
  "windowsSpotlightBlockWindowsTips": true,
  "windowsSpotlightConfigureOnLockScreen": "disabled",
  "networkProxyApplySettingsDeviceWide": true,
  "networkProxyDisableAutoDetect": true,
  "networkProxyAutomaticConfigurationUrl": "https://example.com/networkProxyAutomaticConfigurationUrl/",
  "networkProxyServer": {
    "@odata.type": "microsoft.graph.windows10NetworkProxyServer",
    "address": "Address value",
    "exceptions": [
      "Exceptions value"
    ],
    "useForLocalAddresses": true
  },
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "antiTheftModeBlocked": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "connectedDevicesServiceBlocked": true,
  "certificatesBlockManualRootCertificateInstallation": true,
  "copyPasteBlocked": true,
  "cortanaBlocked": true,
  "deviceManagementBlockFactoryResetOnMobile": true,
  "deviceManagementBlockManualUnenroll": true,
  "safeSearchFilter": "strict",
  "edgeBlockPopups": true,
  "edgeBlockSearchSuggestions": true,
  "edgeBlockSendingIntranetTrafficToInternetExplorer": true,
  "edgeRequireSmartScreen": true,
  "edgeEnterpriseModeSiteListLocation": "Edge Enterprise Mode Site List Location value",
  "edgeFirstRunUrl": "https://example.com/edgeFirstRunUrl/",
  "edgeSearchEngine": {
    "@odata.type": "microsoft.graph.edgeSearchEngineBase"
  },
  "edgeHomepageUrls": [
    "Edge Homepage Urls value"
  ],
  "edgeBlockAccessToAboutFlags": true,
  "smartScreenBlockPromptOverride": true,
  "smartScreenBlockPromptOverrideForFiles": true,
  "webRtcBlockLocalhostIpAddress": true,
  "internetSharingBlocked": true,
  "settingsBlockAddProvisioningPackage": true,
  "settingsBlockRemoveProvisioningPackage": true,
  "settingsBlockChangeSystemTime": true,
  "settingsBlockEditDeviceName": true,
  "settingsBlockChangeRegion": true,
  "settingsBlockChangeLanguage": true,
  "settingsBlockChangePowerSleep": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "microsoftAccountBlockSettingsSync": true,
  "nfcBlocked": true,
  "resetProtectionModeBlocked": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireMobileDeviceEncryption": true,
  "usbBlocked": true,
  "voiceRecordingBlocked": true,
  "wiFiBlockAutomaticConnectHotspots": true,
  "wiFiBlocked": true,
  "wiFiBlockManualConfiguration": true,
  "wiFiScanInterval": 0,
  "wirelessDisplayBlockProjectionToThisDevice": true,
  "wirelessDisplayBlockUserInputFromReceiver": true,
  "wirelessDisplayRequirePinForPairing": true,
  "windowsStoreBlocked": true,
  "appsAllowTrustedAppsSideloading": "blocked",
  "windowsStoreBlockAutoUpdate": true,
  "developerUnlockSetting": "blocked",
  "sharedUserAppDataAllowed": true,
  "appsBlockWindowsStoreOriginatedApps": true,
  "windowsStoreEnablePrivateStoreOnly": true,
  "storageRestrictAppDataToSystemVolume": true,
  "storageRestrictAppInstallToSystemVolume": true,
  "gameDvrBlocked": true,
  "experienceBlockDeviceDiscovery": true,
  "experienceBlockErrorDialogWhenNoSIM": true,
  "experienceBlockTaskSwitcher": true,
  "logonBlockFastUserSwitching": true,
  "tenantLockdownRequireNetworkDuringOutOfBoxExperience": true,
  "appManagementMSIAllowUserControlOverInstall": true,
  "appManagementMSIAlwaysInstallWithElevatedPrivileges": true,
  "dataProtectionBlockDirectMemoryAccess": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 12310

{
  "@odata.type": "#microsoft.graph.windows10GeneralConfiguration",
  "id": "a4235d71-5d71-a423-715d-23a4715d23a4",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "windows10AppsForceUpdateSchedule": {
    "@odata.type": "microsoft.graph.windows10AppsForceUpdateSchedule",
    "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
    "recurrence": "daily",
    "runImmediatelyIfAfterStartDateTime": true
  },
  "enableAutomaticRedeployment": true,
  "assignedAccessSingleModeUserName": "Assigned Access Single Mode User Name value",
  "assignedAccessSingleModeAppUserModelId": "Assigned Access Single Mode App User Model Id value",
  "microsoftAccountSignInAssistantSettings": "disabled",
  "authenticationAllowSecondaryDevice": true,
  "authenticationAllowFIDODevice": true,
  "cryptographyAllowFipsAlgorithmPolicy": true,
  "displayAppListWithGdiDPIScalingTurnedOn": [
    "Display App List With Gdi DPIScaling Turned On value"
  ],
  "displayAppListWithGdiDPIScalingTurnedOff": [
    "Display App List With Gdi DPIScaling Turned Off value"
  ],
  "enterpriseCloudPrintDiscoveryEndPoint": "Enterprise Cloud Print Discovery End Point value",
  "enterpriseCloudPrintOAuthAuthority": "Enterprise Cloud Print OAuth Authority value",
  "enterpriseCloudPrintOAuthClientIdentifier": "Enterprise Cloud Print OAuth Client Identifier value",
  "enterpriseCloudPrintResourceIdentifier": "Enterprise Cloud Print Resource Identifier value",
  "enterpriseCloudPrintDiscoveryMaxLimit": 5,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "Enterprise Cloud Print Mopria Discovery Resource Identifier value",
  "messagingBlockSync": true,
  "messagingBlockMMS": true,
  "messagingBlockRichCommunicationServices": true,
  "printerNames": [
    "Printer Names value"
  ],
  "printerDefaultName": "Printer Default Name value",
  "printerBlockAddition": true,
  "searchBlockDiacritics": true,
  "searchDisableAutoLanguageDetection": true,
  "searchDisableIndexingEncryptedItems": true,
  "searchEnableRemoteQueries": true,
  "searchDisableUseLocation": true,
  "searchDisableLocation": true,
  "searchDisableIndexerBackoff": true,
  "searchDisableIndexingRemovableDrive": true,
  "searchEnableAutomaticIndexSizeManangement": true,
  "searchBlockWebResults": true,
  "securityBlockAzureADJoinedDevicesAutoEncryption": true,
  "diagnosticsDataSubmissionMode": "none",
  "oneDriveDisableFileSync": true,
  "systemTelemetryProxyServer": "System Telemetry Proxy Server value",
  "inkWorkspaceAccess": "enabled",
  "inkWorkspaceAccessState": "blocked",
  "inkWorkspaceBlockSuggestedApps": true,
  "smartScreenEnableAppInstallControl": true,
  "personalizationDesktopImageUrl": "https://example.com/personalizationDesktopImageUrl/",
  "personalizationLockScreenImageUrl": "https://example.com/personalizationLockScreenImageUrl/",
  "bluetoothAllowedServices": [
    "Bluetooth Allowed Services value"
  ],
  "bluetoothBlockAdvertising": true,
  "bluetoothBlockDiscoverableMode": true,
  "bluetoothBlockPrePairing": true,
  "edgeBlockAutofill": true,
  "edgeBlocked": true,
  "edgeCookiePolicy": "allow",
  "edgeBlockDeveloperTools": true,
  "edgeBlockSendingDoNotTrackHeader": true,
  "edgeBlockExtensions": true,
  "edgeBlockInPrivateBrowsing": true,
  "edgeBlockJavaScript": true,
  "edgeBlockPasswordManager": true,
  "edgeBlockAddressBarDropdown": true,
  "edgeBlockCompatibilityList": true,
  "edgeClearBrowsingDataOnExit": true,
  "edgeAllowStartPagesModification": true,
  "edgeDisableFirstRunPage": true,
  "edgeBlockLiveTileDataCollection": true,
  "edgeSyncFavoritesWithInternetExplorer": true,
  "edgeFavoritesListLocation": "Edge Favorites List Location value",
  "edgeBlockEditFavorites": true,
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
  "cellularData": "required",
  "defenderBlockEndUserAccess": true,
  "defenderDaysBeforeDeletingQuarantinedMalware": 12,
  "defenderDetectedMalwareActions": {
    "@odata.type": "microsoft.graph.defenderDetectedMalwareActions",
    "lowSeverity": "clean",
    "moderateSeverity": "clean",
    "highSeverity": "clean",
    "severeSeverity": "clean"
  },
  "defenderSystemScanSchedule": "everyday",
  "defenderFilesAndFoldersToExclude": [
    "Defender Files And Folders To Exclude value"
  ],
  "defenderFileExtensionsToExclude": [
    "Defender File Extensions To Exclude value"
  ],
  "defenderScanMaxCpu": 2,
  "defenderMonitorFileActivity": "disable",
  "defenderPotentiallyUnwantedAppAction": "block",
  "defenderPotentiallyUnwantedAppActionSetting": "enable",
  "defenderProcessesToExclude": [
    "Defender Processes To Exclude value"
  ],
  "defenderPromptForSampleSubmission": "alwaysPrompt",
  "defenderRequireBehaviorMonitoring": true,
  "defenderRequireCloudProtection": true,
  "defenderRequireNetworkInspectionSystem": true,
  "defenderRequireRealTimeMonitoring": true,
  "defenderScanArchiveFiles": true,
  "defenderScanDownloads": true,
  "defenderScanNetworkFiles": true,
  "defenderScanIncomingMail": true,
  "defenderScanMappedNetworkDrivesDuringFullScan": true,
  "defenderScanRemovableDrivesDuringFullScan": true,
  "defenderScanScriptsLoadedInInternetExplorer": true,
  "defenderSignatureUpdateIntervalInHours": 6,
  "defenderScanType": "disabled",
  "defenderScheduledScanTime": "11:59:10.9990000",
  "defenderScheduledQuickScanTime": "11:58:49.3840000",
  "defenderCloudBlockLevel": "high",
  "defenderCloudExtendedTimeout": 12,
  "defenderCloudExtendedTimeoutInSeconds": 5,
  "defenderBlockOnAccessProtection": true,
  "defenderScheduleScanDay": "monday",
  "defenderSubmitSamplesConsentType": "alwaysPrompt",
  "lockScreenAllowTimeoutConfiguration": true,
  "lockScreenBlockActionCenterNotifications": true,
  "lockScreenBlockCortana": true,
  "lockScreenBlockToastNotifications": true,
  "lockScreenTimeoutInSeconds": 10,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "passwordRequireWhenResumeFromIdleState": true,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordMinimumAgeInDays": 8,
  "privacyAdvertisingId": "blocked",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
  "privacyBlockPublishUserActivities": true,
  "privacyBlockActivityFeed": true,
  "startBlockUnpinningAppsFromTaskbar": true,
  "startMenuAppListVisibility": "collapse",
  "startMenuHideChangeAccountSettings": true,
  "startMenuHideFrequentlyUsedApps": true,
  "startMenuHideHibernate": true,
  "startMenuHideLock": true,
  "startMenuHidePowerButton": true,
  "startMenuHideRecentJumpLists": true,
  "startMenuHideRecentlyAddedApps": true,
  "startMenuHideRestartOptions": true,
  "startMenuHideShutDown": true,
  "startMenuHideSignOut": true,
  "startMenuHideSleep": true,
  "startMenuHideSwitchAccount": true,
  "startMenuHideUserTile": true,
  "startMenuLayoutEdgeAssetsXml": "c3RhcnRNZW51TGF5b3V0RWRnZUFzc2V0c1htbA==",
  "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s",
  "startMenuMode": "fullScreen",
  "startMenuPinnedFolderDocuments": "hide",
  "startMenuPinnedFolderDownloads": "hide",
  "startMenuPinnedFolderFileExplorer": "hide",
  "startMenuPinnedFolderHomeGroup": "hide",
  "startMenuPinnedFolderMusic": "hide",
  "startMenuPinnedFolderNetwork": "hide",
  "startMenuPinnedFolderPersonalFolder": "hide",
  "startMenuPinnedFolderPictures": "hide",
  "startMenuPinnedFolderSettings": "hide",
  "startMenuPinnedFolderVideos": "hide",
  "settingsBlockSettingsApp": true,
  "settingsBlockSystemPage": true,
  "settingsBlockDevicesPage": true,
  "settingsBlockNetworkInternetPage": true,
  "settingsBlockPersonalizationPage": true,
  "settingsBlockAccountsPage": true,
  "settingsBlockTimeLanguagePage": true,
  "settingsBlockEaseOfAccessPage": true,
  "settingsBlockPrivacyPage": true,
  "settingsBlockUpdateSecurityPage": true,
  "settingsBlockAppsPage": true,
  "settingsBlockGamingPage": true,
  "windowsSpotlightBlockConsumerSpecificFeatures": true,
  "windowsSpotlightBlocked": true,
  "windowsSpotlightBlockOnActionCenter": true,
  "windowsSpotlightBlockTailoredExperiences": true,
  "windowsSpotlightBlockThirdPartyNotifications": true,
  "windowsSpotlightBlockWelcomeExperience": true,
  "windowsSpotlightBlockWindowsTips": true,
  "windowsSpotlightConfigureOnLockScreen": "disabled",
  "networkProxyApplySettingsDeviceWide": true,
  "networkProxyDisableAutoDetect": true,
  "networkProxyAutomaticConfigurationUrl": "https://example.com/networkProxyAutomaticConfigurationUrl/",
  "networkProxyServer": {
    "@odata.type": "microsoft.graph.windows10NetworkProxyServer",
    "address": "Address value",
    "exceptions": [
      "Exceptions value"
    ],
    "useForLocalAddresses": true
  },
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "antiTheftModeBlocked": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "connectedDevicesServiceBlocked": true,
  "certificatesBlockManualRootCertificateInstallation": true,
  "copyPasteBlocked": true,
  "cortanaBlocked": true,
  "deviceManagementBlockFactoryResetOnMobile": true,
  "deviceManagementBlockManualUnenroll": true,
  "safeSearchFilter": "strict",
  "edgeBlockPopups": true,
  "edgeBlockSearchSuggestions": true,
  "edgeBlockSendingIntranetTrafficToInternetExplorer": true,
  "edgeRequireSmartScreen": true,
  "edgeEnterpriseModeSiteListLocation": "Edge Enterprise Mode Site List Location value",
  "edgeFirstRunUrl": "https://example.com/edgeFirstRunUrl/",
  "edgeSearchEngine": {
    "@odata.type": "microsoft.graph.edgeSearchEngineBase"
  },
  "edgeHomepageUrls": [
    "Edge Homepage Urls value"
  ],
  "edgeBlockAccessToAboutFlags": true,
  "smartScreenBlockPromptOverride": true,
  "smartScreenBlockPromptOverrideForFiles": true,
  "webRtcBlockLocalhostIpAddress": true,
  "internetSharingBlocked": true,
  "settingsBlockAddProvisioningPackage": true,
  "settingsBlockRemoveProvisioningPackage": true,
  "settingsBlockChangeSystemTime": true,
  "settingsBlockEditDeviceName": true,
  "settingsBlockChangeRegion": true,
  "settingsBlockChangeLanguage": true,
  "settingsBlockChangePowerSleep": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "microsoftAccountBlockSettingsSync": true,
  "nfcBlocked": true,
  "resetProtectionModeBlocked": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireMobileDeviceEncryption": true,
  "usbBlocked": true,
  "voiceRecordingBlocked": true,
  "wiFiBlockAutomaticConnectHotspots": true,
  "wiFiBlocked": true,
  "wiFiBlockManualConfiguration": true,
  "wiFiScanInterval": 0,
  "wirelessDisplayBlockProjectionToThisDevice": true,
  "wirelessDisplayBlockUserInputFromReceiver": true,
  "wirelessDisplayRequirePinForPairing": true,
  "windowsStoreBlocked": true,
  "appsAllowTrustedAppsSideloading": "blocked",
  "windowsStoreBlockAutoUpdate": true,
  "developerUnlockSetting": "blocked",
  "sharedUserAppDataAllowed": true,
  "appsBlockWindowsStoreOriginatedApps": true,
  "windowsStoreEnablePrivateStoreOnly": true,
  "storageRestrictAppDataToSystemVolume": true,
  "storageRestrictAppInstallToSystemVolume": true,
  "gameDvrBlocked": true,
  "experienceBlockDeviceDiscovery": true,
  "experienceBlockErrorDialogWhenNoSIM": true,
  "experienceBlockTaskSwitcher": true,
  "logonBlockFastUserSwitching": true,
  "tenantLockdownRequireNetworkDuringOutOfBoxExperience": true,
  "appManagementMSIAllowUserControlOverInstall": true,
  "appManagementMSIAlwaysInstallWithElevatedPrivileges": true,
  "dataProtectionBlockDirectMemoryAccess": true
}
```





