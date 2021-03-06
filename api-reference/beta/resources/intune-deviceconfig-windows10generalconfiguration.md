---
title: Tipo de recurso windows10GeneralConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windows10GeneralConfiguration.
localization_priority: Normal
ms.openlocfilehash: a4fa24d6ef11608d19649925debf3a4855b61e98
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845510"
---
# <a name="windows10generalconfiguration-resource-type"></a>Tipo de recurso windows10GeneralConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windows10GeneralConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows10GeneralConfigurations](../api/intune-deviceconfig-windows10generalconfiguration-list.md)|Colección [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).|
|[Obtener windows10GeneralConfiguration](../api/intune-deviceconfig-windows10generalconfiguration-get.md)|[windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md)|Lea las propiedades y las relaciones del objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).|
|[Crear windows10GeneralConfiguration](../api/intune-deviceconfig-windows10generalconfiguration-create.md)|[windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md)|Cree un objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).|
|[Eliminar windows10GeneralConfiguration](../api/intune-deviceconfig-windows10generalconfiguration-delete.md)|Ninguno|Elimina un [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).|
|[Actualizar windows10GeneralConfiguration](../api/intune-deviceconfig-windows10generalconfiguration-update.md)|[windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md)|Actualice las propiedades de un objeto [windows10GeneralConfiguration](../resources/intune-deviceconfig-windows10generalconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|windows10AppsForceUpdateSchedule|[windows10AppsForceUpdateSchedule](../resources/intune-deviceconfig-windows10appsforceupdateschedule.md)|Programación de actualización de Windows 10 force para las aplicaciones.|
|enableAutomaticRedeployment|Booleano|Permitir a los usuarios con derechos administrativos para eliminar todos los datos de usuario y la configuración con CTRL + Win + R en la pantalla de bloqueo de dispositivo para que pueda volver a configurar automáticamente el dispositivo y reinscrito en administración.|
|assignedAccessSingleModeUserName|Cadena|Esta configuración de directiva permite que para definir la cuenta de usuario que se bloqueará al único modo de quiosco de aplicación.|
|assignedAccessSingleModeAppUserModelId|Cadena|Esta configuración de directiva permite que para definir el identificador de modelo de usuario aplicación (AUMID) que se bloqueará al único modo de quiosco de aplicación.|
|microsoftAccountSignInAssistantSettings|[signInAssistantOptions](../resources/intune-deviceconfig-signinassistantoptions.md)|Controla el servicio NT de cuenta de inicio de sesión Ayudante de Microsoft (wlidsvc). Los valores posibles son: `notConfigured` y `disabled`.|
|authenticationAllowSecondaryDevice|Booleano|Permite que los dispositivos de autenticación secundario para que funcione con Windows.|
|authenticationAllowFIDODevice|Booleano|Indica si se va a permitir la autenticación mediante BOBI dispositivo (o nohttps://fidoalliance.org/)|
|cryptographyAllowFipsAlgorithmPolicy|Booleano|Especifique si desea permitir o no permitir la directiva de Federal Information Processing Standard (FIPS).|
|displayAppListWithGdiDPIScalingTurnedOn|Colección String|Lista de aplicaciones heredadas que tienen GDI activado de escala de PPP.|
|displayAppListWithGdiDPIScalingTurnedOff|Colección String|Lista de aplicaciones heredadas que tienen GDI desactivado de escala de PPP.|
|enterpriseCloudPrintDiscoveryEndPoint|Cadena|Punto de conexión para la detección de impresoras en la nube.|
|enterpriseCloudPrintOAuthAuthority|Cadena|Punto de conexión de autenticación para la adquisición de tokens de OAuth.|
|enterpriseCloudPrintOAuthClientIdentifier|Cadena|GUID de una aplicación cliente autorizado a recuperar los tokens de OAuth de la autoridad OAuth.|
|enterpriseCloudPrintResourceIdentifier|Cadena|URI del recurso de OAuth para el servicio de impresión, tal y como está configurado en el portal de Azure.|
|enterpriseCloudPrintDiscoveryMaxLimit|Int32|Número máximo de impresoras que se deben consultar desde un punto de conexión de detección. Se trata de una configuración solo para móviles. Valores válidos de 1 a 65535|
|enterpriseCloudPrintMopriaDiscoveryResourceIdentifier|Cadena|URI del recurso de OAuth para la detección de impresoras, tal y como está configurado en el portal de Azure.|
|messagingBlockSync|Booleano|Indica si se deben bloquear el mensaje de texto copia de seguridad y restauración y mensajería en cualquier lugar.|
|messagingBlockMMS|Booleano|Indica si se va a bloquear o no el envío o recepción el MMS funcionalidad en el dispositivo.|
|messagingBlockRichCommunicationServices|Booleano|Indica si se va a bloquear o no el envío o recepción del conmutador funcionalidad en el dispositivo.|
|printerNames|Colección String|Aprovisionar automáticamente las impresoras en función de sus nombres (nombres de host de red).|
|printerDefaultName|Cadena|Nombre (nombre de host de red) de una impresora instalada.|
|printerBlockAddition|Booleano|Impedir la instalación de usuario de impresoras adicionales de configuración de las impresoras.|
|searchBlockDiacritics|Booleano|Especifica si la búsqueda puede usar diacríticos.|
|searchDisableAutoLanguageDetection|Booleano|Especifica si se va a utilizar la detección automática de idioma al crear índices de contenido y propiedades.|
|searchDisableIndexingEncryptedItems|Booleano|Indica si se va a bloquear la indexación de los elementos protegidos mediante WIP para impedir que aparezcan en los resultados de búsqueda de Cortana o Explorer.|
|searchEnableRemoteQueries|Booleano|Indica si se van a bloquear las consultas remotas del índice de este equipo.|
|searchDisableUseLocation|Booleano|Especifica si búsqueda puede usar la información de ubicación.|
|searchDisableLocation|Booleano|Especifica si búsqueda puede usar la información de ubicación.|
|searchDisableIndexerBackoff|Booleano|Indica si se va a deshabilitar la característica que reduce la velocidad del indexador de búsqueda.|
|searchDisableIndexingRemovableDrive|Booleano|Indica si se va a permitir que los usuarios agreguen ubicaciones existentes en unidades extraíbles a las bibliotecas e indexarlas.|
|searchEnableAutomaticIndexSizeManangement|Booleano|Especifica la cantidad mínima de espacio en disco duro en la misma unidad que la ubicación del índice antes de detener la indexación.|
|searchBlockWebResults|Booleano|Indica si se deben bloquear la búsqueda en Internet.|
|securityBlockAzureADJoinedDevicesAutoEncryption|Booleano|Especifique si desea permitir el cifrado de automáticas de dispositivos durante OOBE cuando el dispositivo está Azure AD Unido (sólo escritorio).|
|diagnosticsDataSubmissionMode|[diagnosticDataSubmissionMode](../resources/intune-deviceconfig-diagnosticdatasubmissionmode.md)|Obtiene o establece un valor que permite que el dispositivo envíe datos de diagnóstico y telemetría de uso, como Watson. Los valores posibles son: `userDefined`, `none`, `basic`, `enhanced` y `full`.|
|oneDriveDisableFileSync|Booleano|Obtiene o establece un valor que permite que los administradores de TI impidan que las aplicaciones y características funcionen con archivos en OneDrive.|
|systemTelemetryProxyServer|Cadena|Obtiene o establece el nombre de dominio completo (FQDN) o la dirección IP de un servidor proxy para reenviar solicitudes de telemetría y experiencias de usuario conectado.|
|inkWorkspaceAccess|[inkAccessSetting](../resources/intune-deviceconfig-inkaccesssetting.md)|Controla el acceso de usuarios al área de trabajo de entrada de lápiz, desde el escritorio y desde encima de la pantalla de bloqueo. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.|
|inkWorkspaceAccessState|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Controla el acceso de usuarios al área de trabajo de entrada de lápiz, desde el escritorio y desde encima de la pantalla de bloqueo. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|inkWorkspaceBlockSuggestedApps|Booleano|Especifique si desea mostrar sugerencias de aplicación recomendada en el área de trabajo de entrada de lápiz.|
|smartScreenEnableAppInstallControl|Booleano|Permite que los administradores de TI controlen si los usuarios pueden instalar aplicaciones desde lugares que no sean la Tienda.|
|personalizationDesktopImageUrl|Cadena|Dirección URL http o https a una imagen jpg, jpeg o png que debe descargarse y usarse como la imagen de escritorio, o dirección URL de archivo a una imagen local en el sistema de archivos que debe usarse como la imagen de escritorio.|
|personalizationLockScreenImageUrl|Cadena|Dirección URL http o https a una imagen jpg, jpeg o png que debe descargarse y usarse como la imagen de pantalla de bloqueo, o dirección URL de archivo a una imagen local en el sistema de archivos que debe usarse como la imagen de pantalla de bloqueo.|
|bluetoothAllowedServices|Colección String|Especificar una lista de servicios y perfiles Bluetooth permitidos en cadenas de formato hexadecimal.|
|bluetoothBlockAdvertising|Booleano|Indica si se va a impedir que el usuario utilice anuncios de Bluetooth.|
|bluetoothBlockDiscoverableMode|Booleano|Indica si se va a impedir que el usuario utilice el modo visible de Bluetooth.|
|bluetoothBlockPrePairing|Booleano|Indica si se va a impedir que determinados periféricos Bluetooth agrupados se emparejen automáticamente con el dispositivo host.|
|edgeBlockAutofill|Booleano|Indica si se va a bloquear el autorrelleno.|
|edgeBlocked|Booleano|Indica si se va a impedir que el usuario utilice el explorador Edge.|
|edgeCookiePolicy|[edgeCookiePolicy](../resources/intune-deviceconfig-edgecookiepolicy.md)|Indica las cookies que se van a bloquear en el explorador Edge. Los valores posibles son: `userDefined`, `allow`, `blockThirdParty` y `blockAll`.|
|edgeBlockDeveloperTools|Booleano|Indica si se van a bloquear las herramientas de desarrollador en el explorador Edge.|
|edgeBlockSendingDoNotTrackHeader|Booleano|Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.|
|edgeBlockExtensions|Booleano|Indica si se van a bloquear las extensiones en el explorador Edge.|
|edgeBlockInPrivateBrowsing|Booleano|Indica si se va a bloquear la exploración de InPrivate en redes corporativas, en el explorador Edge.|
|edgeBlockJavaScript|Booleano|Indica si se va a impedir que el usuario utilice JavaScript.|
|edgeBlockPasswordManager|Booleano|Indica si se va a bloquear el administrador de contraseñas.|
|edgeBlockAddressBarDropdown|Booleano|Bloquear la funcionalidad de lista desplegable de la barra de direcciones en Microsoft Edge. Deshabilite esta opción para minimizar las conexiones de red de Microsoft Edge con servicios de Microsoft.|
|edgeBlockCompatibilityList|Booleano|Bloquear la lista de compatibilidad de Microsoft en Microsoft Edge. Esta lista de Microsoft ayuda a que Edge muestre correctamente los sitios con problemas de compatibilidad conocidos.|
|edgeClearBrowsingDataOnExit|Booleano|Borrar los datos de navegación al salir de Microsoft Edge.|
|edgeAllowStartPagesModification|Booleano|Permitir que los usuarios cambien las páginas de inicio en Edge. Use la propiedad EdgeHomepageUrls para especificar las páginas de inicio que vería el usuario de forma predeterminada al abrir Edge.|
|edgeDisableFirstRunPage|Booleano|Bloquear la página web de Microsoft que se abre la primera vez que se usa Microsoft Edge. Esta directiva permite que las empresas (por ejemplo, las inscritas en configuraciones de cero emisiones) bloqueen esta página.|
|edgeBlockLiveTileDataCollection|Booleano|Bloquear la recopilación de información por parte de Microsoft para la creación de iconos dinámicos cuando los usuarios anclan un sitio a la pantalla Inicio desde Microsoft Edge.|
|edgeSyncFavoritesWithInternetExplorer|Booleano|Habilitar la sincronización de favoritos entre Internet Explorer y Microsoft Edge. Las adiciones, los cambios de orden, las eliminaciones y las modificaciones de favoritos se comparten entre los dos exploradores.|
|edgeFavoritesListLocation|Cadena|La ubicación de la lista de favoritos para aprovisionar. Puede ser un archivo local, la red local o la ubicación http.|
|edgeBlockEditFavorites|Booleano|Indica si se deben bloquear al usuario de hacer cambios en los favoritos.|
|cellularBlockDataWhenRoaming|Booleano|Indica si se va a impedir que el usuario utilice los datos móviles en itinerancia.|
|cellularBlockVpn|Booleano|Indica si se va a impedir que el usuario utilice VPN en redes de telefonía móvil.|
|cellularBlockVpnWhenRoaming|Booleano|Indica si se va a impedir que el usuario utilice VPN en redes de telefonía móvil en itinerancia.|
|cellularData|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|Si desea permitir que el canal de conexión de datos en el dispositivo. Si no configurado, se permite el canal de conexión de datos y el usuario puede desactivarla. Los valores posibles son: `blocked`, `required` y `allowed`.|
|defenderBlockEndUserAccess|Booleano|Indica si se va a impedir que el usuario final tenga acceso a Defender.|
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
|defenderRequireBehaviorMonitoring|Booleano|Indica si se va a requerir la supervisión de comportamiento.|
|defenderRequireCloudProtection|Booleano|Indica si se va a requerir la protección en la nube.|
|defenderRequireNetworkInspectionSystem|Booleano|Indica si se va a requerir el sistema de inspección de red.|
|defenderRequireRealTimeMonitoring|Booleano|Indica si se va a requerir la supervisión en tiempo real.|
|defenderScanArchiveFiles|Booleano|Indica si se van a examinar archivos de almacenamiento.|
|defenderScanDownloads|Booleano|Indica si se van a examinar las descargas.|
|defenderScanNetworkFiles|Booleano|Indica si se van a examinar los archivos abiertos desde una carpeta de red.|
|defenderScanIncomingMail|Booleano|Indica si se van a examinar los mensajes de correo entrante.|
|defenderScanMappedNetworkDrivesDuringFullScan|Booleano|Indica si se van a analizar las unidades de red asignadas durante el análisis completo.|
|defenderScanRemovableDrivesDuringFullScan|Booleano|Indica si se van a analizar las unidades extraíbles durante el análisis completo.|
|defenderScanScriptsLoadedInInternetExplorer|Booleano|Indica si se van a analizar scripts cargados en el explorador Internet Explorer.|
|defenderSignatureUpdateIntervalInHours|Int32|Intervalo de actualización de la firma en horas. Especifique 0 para no comprobarla. Valores válidos de 0 a 24|
|defenderScanType|[defenderScanType](../resources/intune-deviceconfig-defenderscantype.md)|Tipo de análisis del sistema de Defender. Los valores posibles son: `userDefined`, `disabled`, `quick` y `full`.|
|defenderScheduledScanTime|TimeOfDay|Hora de Defender para el análisis del sistema.|
|defenderScheduledQuickScanTime|TimeOfDay|Hora en la que se realiza un análisis rápido diariamente.|
|defenderCloudBlockLevel|[defenderCloudBlockLevelType](../resources/intune-deviceconfig-defendercloudblockleveltype.md)|Especifica el nivel de protección que proporciona la nube. Los valores posibles son: `notConfigured`, `high`, `highPlus` y `zeroTolerance`.|
|defenderCloudExtendedTimeout|Int32|Extensión de tiempo de espera para el archivo de examen de la nube. Valores válidos de 0 a 50.|
|defenderCloudExtendedTimeoutInSeconds|Int32|Extensión de tiempo de espera para el archivo de examen de la nube. Valores válidos de 0 a 50.|
|defenderBlockOnAccessProtection|Booleano|Permiten o impiden la funcionalidad de Windows Defender en protección de acceso.|
|defenderScheduleScanDay|[defenderScheduleScanDay](../resources/intune-deviceconfig-defenderschedulescanday.md)|Selecciona el día en que se debe ejecutar el examen de Windows Defender. Los valores posibles son: `everyday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday` y `noScheduledScan`.|
|defenderSubmitSamplesConsentType|[defenderSubmitSamplesConsentType](../resources/intune-deviceconfig-defendersubmitsamplesconsenttype.md)|Comprueba si el usuario da su consentimiento nivel en Windows Defender para enviar datos. Los valores posibles son: `sendSafeSamplesAutomatically`, `alwaysPrompt`, `neverSend` y `sendAllSamplesAutomatically`.|
|lockScreenAllowTimeoutConfiguration|Booleano|Especifica si se mostrará una opción configurable por el usuario para controlar el tiempo de espera de la pantalla mientras se está en la pantalla de bloqueo de dispositivos Windows 10 Mobile. Si esta directiva está establecida en Permitir, se ignora el valor establecido por lockScreenTimeoutInSeconds.|
|lockScreenBlockActionCenterNotifications|Booleano|Indica si se van a bloquear las notificaciones del centro de acciones en la pantalla de bloqueo.|
|lockScreenBlockCortana|Booleano|Indica si el usuario puede interactuar con Cortana mediante la voz mientras el sistema está bloqueado.|
|lockScreenBlockToastNotifications|Booleano|Indica si se permiten las notificaciones del sistema por encima de la pantalla de bloqueo del dispositivo.|
|lockScreenTimeoutInSeconds|Int32|Establecer la duración (en segundos) entre el bloqueo de la pantalla y su desactivación en dispositivos Windows 10 Mobile. Los valores admitidos son de 11 a 1800. Valores válidos de 11 a 1800|
|passwordBlockSimple|Booleano|Especifique si se permiten números PIN o contraseñas, como "1111" o "1234". En equipos de escritorio Windows 10, también controla el uso de contraseñas de imagen.|
|passwordExpirationDays|Int32|La expiración de la contraseña en días. Valores válidos de 0 a 730.|
|passwordMinimumLength|Int32|La longitud mínima de contraseña. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passwordMinimumCharacterSetCount|Int32|Número de juegos de caracteres necesarios en la contraseña.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que impiden su reutilización. Valores válidos de 0 a 50.|
|passwordRequired|Booleano|Indica si se va a requerir que el usuario tenga una contraseña.|
|passwordRequireWhenResumeFromIdleState|Booleano|Indica si se va a requerir una contraseña al reanudar desde un estado inactivo.|
|passwordRequiredType|[requiredPasswordType](../resources/intune-deviceconfig-requiredpasswordtype.md)|Tipo de contraseña necesaria. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica. Valores válidos de 0 a 999.|
|passwordMinimumAgeInDays|Int32|Esta configuración de seguridad determina el período de tiempo (en días) que debe ser una contraseña utilizada antes de que el usuario puede cambiarla. Valores válidos de 0 a 998|
|privacyAdvertisingId|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Habilita o deshabilita el uso del identificador de publicidad. Se agregó en Windows 10, versión 1607. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|privacyAutoAcceptPairingAndConsentPrompts|Booleano|Indica si se va a permitir la aceptación automática de los cuadros de diálogo de consentimiento del usuario de emparejamiento y privacidad al iniciar aplicaciones.|
|privacyBlockInputPersonalization|Booleano|Indica si se va a bloquear el uso de servicios de voz basados en la nube de Cortana, el dictado o las aplicaciones de la tienda.|
|privacyBlockPublishUserActivities|Booleano|Bloquea la detección/experiencias compartida de recursos usados recientemente en el conmutador de tareas de etcetera.|
|privacyBlockActivityFeed|Booleano|Bloquea el uso de servicios de nube en función de voz para Cortana, Dictation o almacén de aplicaciones.|
|startBlockUnpinningAppsFromTaskbar|Booleano|Indica si se va a impedir que el usuario desancle aplicaciones de la barra de tareas.|
|startMenuAppListVisibility|[windowsStartMenuAppListVisibilityType](../resources/intune-deviceconfig-windowsstartmenuapplistvisibilitytype.md)|Al configurar este valor, se contrae la lista de aplicaciones, se quita la lista de aplicaciones por completo o se deshabilita la alternancia correspondiente en la aplicación Configuración. Los valores posibles son: `userDefined`, `collapse`, `remove` y `disableSettingsApp`.|
|startMenuHideChangeAccountSettings|Booleano|Al habilitar esta directiva, se impide que la opción Cambiar configuración de cuenta aparezca en el icono de usuario del menú Inicio.|
|startMenuHideFrequentlyUsedApps|Booleano|Al habilitar esta directiva, se ocultan la mayoría de las aplicaciones usadas en el menú Inicio y se deshabilita la conmutación correspondiente en la aplicación Configuración.|
|startMenuHideHibernate|Booleano|Al habilitar esta directiva, se oculta la opción de hibernación en el botón de encendido del menú Inicio.|
|startMenuHideLock|Booleano|Al habilitar esta directiva, se oculta la opción de bloqueo en el icono de usuario del menú Inicio.|
|startMenuHidePowerButton|Booleano|Al habilitar esta directiva, se oculta el botón de encendido del menú Inicio.|
|startMenuHideRecentJumpLists|Booleano|Al habilitar esta directiva, se ocultan las listas de accesos directos recientes en el menú Inicio o la barra de tareas y se deshabilita la alternancia correspondiente en la aplicación Configuración.|
|startMenuHideRecentlyAddedApps|Booleano|Al habilitar esta directiva, se ocultan las aplicaciones agregadas recientemente en el menú Inicio y se deshabilita la alternancia correspondiente en la aplicación Configuración.|
|startMenuHideRestartOptions|Booleano|Al habilitar esta directiva, se ocultan las opciones de reinicio/actualización y reinicio en el botón de encendido del menú Inicio.|
|startMenuHideShutDown|Booleano|Al habilitar esta directiva, se ocultan las opciones de apagado/actualización y apagado en el botón de encendido del menú Inicio.|
|startMenuHideSignOut|Booleano|Al habilitar esta directiva, se oculta la opción Cerrar sesión en el icono de usuario del menú Inicio.|
|startMenuHideSleep|Booleano|Al habilitar esta directiva, se oculta la opción Suspender en el botón de apagado del menú Inicio.|
|startMenuHideSwitchAccount|Booleano|Al habilitar esta directiva, se oculta la opción Cambiar de cuenta en el icono de usuario del menú Inicio.|
|startMenuHideUserTile|Booleano|Al habilitar esta directiva, se oculta el icono de usuario del menú Inicio.|
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
|settingsBlockSettingsApp|Booleano|Indica si se va a bloquear el acceso a la aplicación Ajustes.|
|settingsBlockSystemPage|Booleano|Indica si se va a bloquear el acceso a Sistema en la aplicación Ajustes.|
|settingsBlockDevicesPage|Booleano|Indica si se va a bloquear el acceso a Dispositivos en la aplicación Ajustes.|
|settingsBlockNetworkInternetPage|Booleano|Indica si se va a bloquear el acceso a Red e Internet en la aplicación Ajustes.|
|settingsBlockPersonalizationPage|Booleano|Indica si se va a bloquear el acceso a Personalización en la aplicación Ajustes.|
|settingsBlockAccountsPage|Booleano|Indica si se va a bloquear el acceso a Cuentas en la aplicación Ajustes.|
|settingsBlockTimeLanguagePage|Booleano|Indica si se va a bloquear el acceso a Hora e idioma en la aplicación Ajustes.|
|settingsBlockEaseOfAccessPage|Booleano|Indica si se va a bloquear el acceso a Accesibilidad en la aplicación Ajustes.|
|settingsBlockPrivacyPage|Booleano|Indica si se va a bloquear el acceso a Privacidad en la aplicación Ajustes.|
|settingsBlockUpdateSecurityPage|Booleano|Indica si se va a bloquear el acceso a Actualización y seguridad en la aplicación Ajustes.|
|settingsBlockAppsPage|Booleano|Indica si se va a bloquear el acceso a Aplicaciones en la aplicación Ajustes.|
|settingsBlockGamingPage|Booleano|Indica si se va a bloquear el acceso a Juegos en la aplicación Ajustes.|
|windowsSpotlightBlockConsumerSpecificFeatures|Booleano|Permite que los administradores de TI bloqueen experiencias que suelen ser solo para consumidores, como las sugerencias de inicio, las notificaciones de suscripción, la instalación de aplicaciones post-OOBE y los iconos de redireccionamiento.|
|windowsSpotlightBlocked|Booleano|Permite que los administradores de TI desactiven todas las características de Contenido destacado de Windows.|
|windowsSpotlightBlockOnActionCenter|Booleano|Bloquear las sugerencias de Microsoft que se muestran después de cada instalación limpia del sistema operativo, actualización o de forma continua para presentar a los usuarios los cambios y novedades.|
|windowsSpotlightBlockTailoredExperiences|Booleano|Bloquear el contenido personalizado del Contenido destacado de Windows según el uso del dispositivo del usuario.|
|windowsSpotlightBlockThirdPartyNotifications|Booleano|Bloquear contenido de terceros que se envía a través del Contenido destacado de Windows.|
|windowsSpotlightBlockWelcomeExperience|Booleano|Bloquear la experiencia de bienvenida de Windows del Contenido destacado de Windows.|
|windowsSpotlightBlockWindowsTips|Booleano|Permite que los administradores de TI desactiven el elemento emergente Sugerencias de Windows.|
|windowsSpotlightConfigureOnLockScreen|[windowsSpotlightEnablementSettings](../resources/intune-deviceconfig-windowsspotlightenablementsettings.md)|Especifica el tipo de luz de foco. Los valores posibles son: `notConfigured`, `disabled` y `enabled`.|
|networkProxyApplySettingsDeviceWide|Booleano|Si se establece, la configuración de proxy se aplicará a todos los procesos y cuentas en el dispositivo. En caso contrario, se aplicará a la cuenta de usuario que está inscrita en MDM.|
|networkProxyDisableAutoDetect|Booleano|Deshabilitar la detección automática de la configuración. Si está habilitada, el sistema intentará encontrar la ruta de acceso a un script de configuración automática de proxy (PAC).|
|networkProxyAutomaticConfigurationUrl|Cadena|Dirección al script de configuración automática de proxy (PAC) que quiera usar.|
|networkProxyServer|[windows10NetworkProxyServer](../resources/intune-deviceconfig-windows10networkproxyserver.md)|Especifica la configuración manual del servidor proxy.|
|accountsBlockAddingNonMicrosoftAccountEmail|Booleano|Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas a una cuenta de Microsoft.|
|antiTheftModeBlocked|Booleano|Indica si se va a impedir que el usuario seleccione una preferencia de modo antirrobo (solo Windows 10 Mobile).|
|bluetoothBlocked|Booleano|Indica si se va a impedir que el usuario utilice Bluetooth.|
|cameraBlocked|Booleano|Indica si se va a impedir que el usuario tenga acceso a la cámara del dispositivo.|
|connectedDevicesServiceBlocked|Booleano|Indica si se va a bloquear el servicio de dispositivos conectados que permite la detección y conexión con otros dispositivos, la mensajería remota, las sesiones de aplicación remota y otras experiencias entre dispositivos.|
|certificatesBlockManualRootCertificateInstallation|Booleano|Indica si se va a impedir que el usuario instale manualmente el certificado raíz.|
|copyPasteBlocked|Booleano|Indica si se va a impedir que el usuario utilice la opción de copiar y pegar.|
|cortanaBlocked|Booleano|Indica si se va a impedir que el usuario utilice Cortana.|
|deviceManagementBlockFactoryResetOnMobile|Booleano|Indica si se va a impedir que el usuario restablezca el teléfono.|
|deviceManagementBlockManualUnenroll|Booleano|Indica si se va a impedir que el usuario realice una anulación manual de la inscripción desde la administración del dispositivo.|
|safeSearchFilter|[safeSearchFilterType](../resources/intune-deviceconfig-safesearchfiltertype.md)|Especifica el nivel de filtro de búsqueda segura que es necesario. Los valores posibles son: `userDefined`, `strict` y `moderate`.|
|edgeBlockPopups|Booleano|Indica si se van a bloquear los elementos emergentes.|
|edgeBlockSearchSuggestions|Booleano|Indica si se va a impedir que el usuario utilice las sugerencias de búsqueda en la barra de direcciones.|
|edgeBlockSendingIntranetTrafficToInternetExplorer|Booleano|Indica si se va a impedir que el usuario envíe tráfico de Intranet a Internet Explorer desde Edge.|
|edgeRequireSmartScreen|Booleano|Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.|
|edgeEnterpriseModeSiteListLocation|Cadena|Indica la ubicación de la lista de sitios del modo de empresa. Puede ser un archivo local, la red local o la ubicación http.|
|edgeFirstRunUrl|Cadena|Primera dirección URL que se ejecuta al abrir el explorador Edge por primera vez.|
|edgeSearchEngine|[edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)|Permite que los administradores de TI configuren un motor de búsqueda predeterminado para dispositivos controlados por MDM. Los usuarios pueden invalidarla y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.|
|edgeHomepageUrls|Colección String|Lista de direcciones URL de páginas principales que se muestran en dispositivos inscritos en MDM en el explorador Edge.|
|edgeBlockAccessToAboutFlags|Booleano|Indica si se va a impedir el acceso a las marcas de información en el explorador Edge.|
|smartScreenBlockPromptOverride|Booleano|Indica si los usuarios pueden invalidar las advertencias de filtro SmartScreen sobre sitios web potencialmente malintencionados.|
|smartScreenBlockPromptOverrideForFiles|Booleano|Indica si los usuarios pueden invalidar las advertencias del filtro SmartScreen sobre la descarga de archivos no comprobados.|
|webRtcBlockLocalhostIpAddress|Booleano|Indica si se muestra la dirección IP de Localhost del usuario durante las llamadas telefónicas mediante WebRTC|
|internetSharingBlocked|Booleano|Indica si se va a impedir que el usuario utilice el uso compartido de Internet.|
|settingsBlockAddProvisioningPackage|Booleano|Indica si se va a impedir que el usuario instale paquetes de aprovisionamiento.|
|settingsBlockRemoveProvisioningPackage|Booleano|Indica si se va a impedir que el agente de configuración en tiempo de ejecución quite los paquetes de aprovisionamiento.|
|settingsBlockChangeSystemTime|Booleano|Indica si se va a impedir que el usuario cambie los ajustes de fecha y hora.|
|settingsBlockEditDeviceName|Booleano|Indica si se va a impedir que el usuario edite el nombre del dispositivo.|
|settingsBlockChangeRegion|Booleano|Indica si se va a impedir que el usuario cambie los ajustes de región.|
|settingsBlockChangeLanguage|Booleano|Indica si se va a impedir que el usuario cambie los ajustes de idioma.|
|settingsBlockChangePowerSleep|Booleano|Indica si se va a impedir que el usuario cambie los ajustes de inicio/apagado y suspensión.|
|locationServicesBlocked|Booleano|Indica si se va a impedir que el usuario utilice los servicios de ubicación.|
|microsoftAccountBlocked|Booleano|Indica si se va a bloquear una cuenta de Microsoft.|
|microsoftAccountBlockSettingsSync|Booleano|Indica si se va a bloquear la sincronización de la configuración de una cuenta de Microsoft.|
|nfcBlocked|Booleano|Indica si se va a impedir que el usuario utilice la transmisión de datos en proximidad.|
|resetProtectionModeBlocked|Booleano|Indica si se va a impedir que el usuario restablezca el modo de protección.|
|screenCaptureBlocked|Booleano|Indica si se va a impedir que el usuario tome capturas de pantalla.|
|storageBlockRemovableStorage|Booleano|Indica si se va a impedir que el usuario utilice almacenamiento extraíble.|
|storageRequireMobileDeviceEncryption|Booleano|Indica si se va a requerir el cifrado en un dispositivo móvil.|
|usbBlocked|Booleano|Indica si se va a impedir que el usuario realice conexiones USB.|
|voiceRecordingBlocked|Booleano|Indica si se va a impedir que el usuario grabe voz.|
|wiFiBlockAutomaticConnectHotspots|Booleano|Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi. No tiene impacto si se bloquea el Wi-Fi.|
|wiFiBlocked|Booleano|Indica si se va a impedir que el usuario utilice Wi-Fi.|
|wiFiBlockManualConfiguration|Booleano|Indica si se va a impedir que el usuario realice la configuración manual de Wi-Fi.|
|wiFiScanInterval|Int32|Especificar la frecuencia con la que los dispositivos buscan redes Wi-Fi. Los valores admitidos son de 1 a 500, donde 100 = predeterminado y 500 = baja frecuencia. Valores válidos de 1 a 500.|
|wirelessDisplayBlockProjectionToThisDevice|Booleano|Indica si se va a permitir que otros dispositivos detecten este equipo para proyección.|
|wirelessDisplayBlockUserInputFromReceiver|Booleano|Indica si se va a permitir la entrada del usuario desde un receptor de visualización inalámbrico.|
|wirelessDisplayRequirePinForPairing|Booleano|Indica si se va a requerir un PIN para iniciar el emparejamiento con nuevos dispositivos.|
|windowsStoreBlocked|Booleano|Indica si se va a impedir que el usuario utilice la Tienda Windows.|
|appsAllowTrustedAppsSideloading|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Indica si las aplicaciones de paquetes AppX firmados con un certificado de confianza se pueden cargar lateralmente. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|windowsStoreBlockAutoUpdate|Booleano|Indica si se va a bloquear la actualización automática de aplicaciones desde la Tienda Windows.|
|developerUnlockSetting|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Indica si se va a permitir el desbloqueo de desarrollador. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|sharedUserAppDataAllowed|Booleano|Indica si se va a impedir que varios usuarios de la misma aplicación compartan datos.|
|appsBlockWindowsStoreOriginatedApps|Booleano|Indica si se va a deshabilitar el inicio de todas las aplicaciones que vienen preinstaladas o que se han descargado desde la Tienda Windows.|
|windowsStoreEnablePrivateStoreOnly|Booleano|Indica si se va a habilitar solo la tienda privada.|
|storageRestrictAppDataToSystemVolume|Booleano|Indica si los datos de la aplicación están restringidos a la unidad del sistema.|
|storageRestrictAppInstallToSystemVolume|Booleano|Indica si la instalación de la aplicación está restringida a la unidad del sistema.|
|gameDvrBlocked|Booleano|Indica si se va a bloquear la DVR y la difusión.|
|experienceBlockDeviceDiscovery|Booleano|Indica si se va a habilitar la experiencia de usuario de detección de dispositivos.|
|experienceBlockErrorDialogWhenNoSIM|Booleano|Indica si se va a permitir que se muestre el cuadro de diálogo de error si no se detecta ninguna tarjeta SIM.|
|experienceBlockTaskSwitcher|Booleano|Indica si se va a habilitar el cambio de tarea en el dispositivo.|
|logonBlockFastUserSwitching|Booleano|Deshabilita la posibilidad de cambiar rápidamente entre usuarios que han iniciado sesión a la vez sin cerrar la sesión.|
|tenantLockdownRequireNetworkDuringOutOfBoxExperience|Booleano|Si el dispositivo es necesario para conectarse a la red.|
|appManagementMSIAllowUserControlOverInstall|Booleano|Esta configuración de directiva permite a los usuarios cambiar las opciones de instalación que normalmente están disponibles sólo para los administradores del sistema.|
|appManagementMSIAlwaysInstallWithElevatedPrivileges|Booleano|Esta configuración de directiva indica a Windows Installer que use permisos elevados cuando instala cualquier programa en el sistema.|
|dataProtectionBlockDirectMemoryAccess|Booleano|Esta configuración de directiva permite bloquear el acceso directo a memoria (DMA) para todos los hot acoplable PCI puertos dirección descendente hasta que un usuario inicia sesión en Windows.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|groupAssignments|colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|assignedAccessMultiModeProfiles|colección de [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)|Esta configuración de directiva permite que para definir una lista de perfiles de acceso asignado para el modo de aplicación múltiples.|
|privacyAccessControls|colección de [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md)|Indica una lista de aplicaciones con sus niveles de control de acceso a través de categorías de privacidad de datos, o los niveles de acceso predeterminada por categoría.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10GeneralConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10GeneralConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "windows10AppsForceUpdateSchedule": {
    "@odata.type": "microsoft.graph.windows10AppsForceUpdateSchedule",
    "startDateTime": "String (timestamp)",
    "recurrence": "String",
    "runImmediatelyIfAfterStartDateTime": true
  },
  "enableAutomaticRedeployment": true,
  "assignedAccessSingleModeUserName": "String",
  "assignedAccessSingleModeAppUserModelId": "String",
  "microsoftAccountSignInAssistantSettings": "String",
  "authenticationAllowSecondaryDevice": true,
  "authenticationAllowFIDODevice": true,
  "cryptographyAllowFipsAlgorithmPolicy": true,
  "displayAppListWithGdiDPIScalingTurnedOn": [
    "String"
  ],
  "displayAppListWithGdiDPIScalingTurnedOff": [
    "String"
  ],
  "enterpriseCloudPrintDiscoveryEndPoint": "String",
  "enterpriseCloudPrintOAuthAuthority": "String",
  "enterpriseCloudPrintOAuthClientIdentifier": "String",
  "enterpriseCloudPrintResourceIdentifier": "String",
  "enterpriseCloudPrintDiscoveryMaxLimit": 1024,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "String",
  "messagingBlockSync": true,
  "messagingBlockMMS": true,
  "messagingBlockRichCommunicationServices": true,
  "printerNames": [
    "String"
  ],
  "printerDefaultName": "String",
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
  "diagnosticsDataSubmissionMode": "String",
  "oneDriveDisableFileSync": true,
  "systemTelemetryProxyServer": "String",
  "inkWorkspaceAccess": "String",
  "inkWorkspaceAccessState": "String",
  "inkWorkspaceBlockSuggestedApps": true,
  "smartScreenEnableAppInstallControl": true,
  "personalizationDesktopImageUrl": "String",
  "personalizationLockScreenImageUrl": "String",
  "bluetoothAllowedServices": [
    "String"
  ],
  "bluetoothBlockAdvertising": true,
  "bluetoothBlockDiscoverableMode": true,
  "bluetoothBlockPrePairing": true,
  "edgeBlockAutofill": true,
  "edgeBlocked": true,
  "edgeCookiePolicy": "String",
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
  "edgeFavoritesListLocation": "String",
  "edgeBlockEditFavorites": true,
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
  "cellularData": "String",
  "defenderBlockEndUserAccess": true,
  "defenderDaysBeforeDeletingQuarantinedMalware": 1024,
  "defenderDetectedMalwareActions": {
    "@odata.type": "microsoft.graph.defenderDetectedMalwareActions",
    "lowSeverity": "String",
    "moderateSeverity": "String",
    "highSeverity": "String",
    "severeSeverity": "String"
  },
  "defenderSystemScanSchedule": "String",
  "defenderFilesAndFoldersToExclude": [
    "String"
  ],
  "defenderFileExtensionsToExclude": [
    "String"
  ],
  "defenderScanMaxCpu": 1024,
  "defenderMonitorFileActivity": "String",
  "defenderPotentiallyUnwantedAppAction": "String",
  "defenderPotentiallyUnwantedAppActionSetting": "String",
  "defenderProcessesToExclude": [
    "String"
  ],
  "defenderPromptForSampleSubmission": "String",
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
  "defenderSignatureUpdateIntervalInHours": 1024,
  "defenderScanType": "String",
  "defenderScheduledScanTime": "String (time of day)",
  "defenderScheduledQuickScanTime": "String (time of day)",
  "defenderCloudBlockLevel": "String",
  "defenderCloudExtendedTimeout": 1024,
  "defenderCloudExtendedTimeoutInSeconds": 1024,
  "defenderBlockOnAccessProtection": true,
  "defenderScheduleScanDay": "String",
  "defenderSubmitSamplesConsentType": "String",
  "lockScreenAllowTimeoutConfiguration": true,
  "lockScreenBlockActionCenterNotifications": true,
  "lockScreenBlockCortana": true,
  "lockScreenBlockToastNotifications": true,
  "lockScreenTimeoutInSeconds": 1024,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passwordMinimumCharacterSetCount": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordRequired": true,
  "passwordRequireWhenResumeFromIdleState": true,
  "passwordRequiredType": "String",
  "passwordSignInFailureCountBeforeFactoryReset": 1024,
  "passwordMinimumAgeInDays": 1024,
  "privacyAdvertisingId": "String",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
  "privacyBlockPublishUserActivities": true,
  "privacyBlockActivityFeed": true,
  "startBlockUnpinningAppsFromTaskbar": true,
  "startMenuAppListVisibility": "String",
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
  "startMenuLayoutEdgeAssetsXml": "binary",
  "startMenuLayoutXml": "binary",
  "startMenuMode": "String",
  "startMenuPinnedFolderDocuments": "String",
  "startMenuPinnedFolderDownloads": "String",
  "startMenuPinnedFolderFileExplorer": "String",
  "startMenuPinnedFolderHomeGroup": "String",
  "startMenuPinnedFolderMusic": "String",
  "startMenuPinnedFolderNetwork": "String",
  "startMenuPinnedFolderPersonalFolder": "String",
  "startMenuPinnedFolderPictures": "String",
  "startMenuPinnedFolderSettings": "String",
  "startMenuPinnedFolderVideos": "String",
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
  "windowsSpotlightConfigureOnLockScreen": "String",
  "networkProxyApplySettingsDeviceWide": true,
  "networkProxyDisableAutoDetect": true,
  "networkProxyAutomaticConfigurationUrl": "String",
  "networkProxyServer": {
    "@odata.type": "microsoft.graph.windows10NetworkProxyServer",
    "address": "String",
    "exceptions": [
      "String"
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
  "safeSearchFilter": "String",
  "edgeBlockPopups": true,
  "edgeBlockSearchSuggestions": true,
  "edgeBlockSendingIntranetTrafficToInternetExplorer": true,
  "edgeRequireSmartScreen": true,
  "edgeEnterpriseModeSiteListLocation": "String",
  "edgeFirstRunUrl": "String",
  "edgeSearchEngine": {
    "@odata.type": "microsoft.graph.edgeSearchEngineBase"
  },
  "edgeHomepageUrls": [
    "String"
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
  "wiFiScanInterval": 1024,
  "wirelessDisplayBlockProjectionToThisDevice": true,
  "wirelessDisplayBlockUserInputFromReceiver": true,
  "wirelessDisplayRequirePinForPairing": true,
  "windowsStoreBlocked": true,
  "appsAllowTrustedAppsSideloading": "String",
  "windowsStoreBlockAutoUpdate": true,
  "developerUnlockSetting": "String",
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





