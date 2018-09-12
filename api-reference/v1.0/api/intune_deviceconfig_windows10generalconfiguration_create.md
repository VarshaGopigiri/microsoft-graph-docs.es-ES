# <a name="create-windows10generalconfiguration"></a>Crear windows10GeneralConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un objeto [windows10GeneralConfiguration](../resources/intune_deviceconfig_windows10generalconfiguration.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

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
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10GeneralConfiguration.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10GeneralConfiguration.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|enterpriseCloudPrintDiscoveryEndPoint|Cadena|Punto de conexión para la detección de impresoras en la nube.|
|enterpriseCloudPrintOAuthAuthority|Cadena|Punto de conexión de autenticación para la adquisición de tokens de OAuth.|
|enterpriseCloudPrintOAuthClientIdentifier|Cadena|GUID de una aplicación cliente autorizado a recuperar los tokens de OAuth de la autoridad OAuth.|
|enterpriseCloudPrintResourceIdentifier|Cadena|URI del recurso de OAuth para el servicio de impresión, tal y como está configurado en el portal de Azure.|
|enterpriseCloudPrintDiscoveryMaxLimit|Int32|Número máximo de impresoras que se deben consultar desde un punto de conexión de detección. Se trata de una configuración solo para móviles. Valores válidos de 1 a 65535|
|enterpriseCloudPrintMopriaDiscoveryResourceIdentifier|Cadena|URI del recurso de OAuth para la detección de impresoras, tal y como está configurado en el portal de Azure.|
|searchBlockDiacritics|Booleano|Especifica si la búsqueda puede usar diacríticos.|
|searchDisableAutoLanguageDetection|Booleano|Especifica si se va a utilizar la detección automática de idioma al crear índices de contenido y propiedades.|
|searchDisableIndexingEncryptedItems|Booleano|Indica si se va a bloquear la indexación de los elementos protegidos mediante WIP para impedir que aparezcan en los resultados de búsqueda de Cortana o Explorer.|
|searchEnableRemoteQueries|Booleano|Indica si se van a bloquear las consultas remotas del índice de este equipo.|
|searchDisableIndexerBackoff|Booleano|Indica si se va a deshabilitar la característica que reduce la velocidad del indexador de búsqueda.|
|searchDisableIndexingRemovableDrive|Booleano|Indica si se va a permitir que los usuarios agreguen ubicaciones existentes en unidades extraíbles a las bibliotecas e indexarlas.|
|searchEnableAutomaticIndexSizeManangement|Booleano|Especifica la cantidad mínima de espacio en disco duro en la misma unidad que la ubicación del índice antes de detener la indexación.|
|diagnosticsDataSubmissionMode|[diagnosticDataSubmissionMode](../resources/intune_deviceconfig_diagnosticdatasubmissionmode.md)|Obtiene o establece un valor que permite el dispositivo enviar el diagnóstico y los datos de telemetría de uso, como Watson. Los valores posibles son: `userDefined`, `none`, `basic`, `enhanced`, `full`.|
|oneDriveDisableFileSync|Booleano|Obtiene o establece un valor que permite que los administradores de TI impidan que las aplicaciones y características funcionen con archivos en OneDrive.|
|smartScreenEnableAppInstallControl|Booleano|Permite que los administradores de TI controlen si los usuarios pueden instalar aplicaciones desde lugares que no sean la Tienda.|
|personalizationDesktopImageUrl|Cadena|Dirección URL http o https a una imagen jpg, jpeg o png que debe descargarse y usarse como la imagen de escritorio, o dirección URL de archivo a una imagen local en el sistema de archivos que debe usarse como la imagen de escritorio.|
|personalizationLockScreenImageUrl|Cadena|Dirección URL http o https a una imagen jpg, jpeg o png que debe descargarse y usarse como la imagen de pantalla de bloqueo, o dirección URL de archivo a una imagen local en el sistema de archivos que debe usarse como la imagen de pantalla de bloqueo.|
|bluetoothAllowedServices|Colección String|Especificar una lista de servicios y perfiles Bluetooth permitidos en cadenas de formato hexadecimal.|
|bluetoothBlockAdvertising|Booleano|Indica si se va a impedir que el usuario utilice anuncios de Bluetooth.|
|bluetoothBlockDiscoverableMode|Booleano|Indica si se va a impedir que el usuario utilice el modo visible de Bluetooth.|
|bluetoothBlockPrePairing|Booleano|Indica si se va a impedir que determinados periféricos Bluetooth agrupados se emparejen automáticamente con el dispositivo host.|
|edgeBlockAutofill|Booleano|Indica si se va a bloquear el autorrelleno.|
|edgeBlocked|Booleano|Indica si se va a impedir que el usuario utilice el explorador Edge.|
|edgeCookiePolicy|[edgeCookiePolicy](../resources/intune_deviceconfig_edgecookiepolicy.md)|Indica qué cookies desea bloquear en el navegador Edge. Los valores posibles son: `userDefined`, `allow`, `blockThirdParty`, `blockAll`.|
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
|cellularBlockDataWhenRoaming|Booleano|Indica si se va a impedir que el usuario utilice los datos móviles en itinerancia.|
|cellularBlockVpn|Booleano|Indica si se va a impedir que el usuario utilice VPN en redes de telefonía móvil.|
|cellularBlockVpnWhenRoaming|Booleano|Indica si se va a impedir que el usuario utilice VPN en redes de telefonía móvil en itinerancia.|
|defenderBlockEndUserAccess|Booleano|Indica si se va a impedir que el usuario final tenga acceso a Defender.|
|defenderDaysBeforeDeletingQuarantinedMalware|Int32|Número de días antes de que se elimine el malware en cuarentena. Valores válidos de 0 a 90.|
|defenderDetectedMalwareActions|[defenderDetectedMalwareActions](../resources/intune_deviceconfig_defenderdetectedmalwareactions.md)|Obtiene o especifica las acciones de Defender para el malware detectado por nivel de amenaza.|
|defenderSystemScanSchedule|[weeklySchedule](../resources/intune_deviceconfig_weeklyschedule.md)|Día de la semana para que Defender haga la exploración del sistema. Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.|
|defenderFilesAndFoldersToExclude|Colección String|Archivos y carpetas que se van a excluir de los análisis y la protección en tiempo real.|
|defenderFileExtensionsToExclude|Colección String|Extensiones de archivo que se van a excluir de los análisis y la protección en tiempo real.|
|defenderScanMaxCpu|Int32|Porcentaje máximo de uso de CPU durante el análisis. Valores válidos de 0 a 100.|
|defenderMonitorFileActivity|[defenderMonitorFileActivity](../resources/intune_deviceconfig_defendermonitorfileactivity.md)|Valor para supervisar la actividad de archivo. Los valores posibles son: `userDefined`, `disable`, `monitorAllFiles`, `monitorIncomingFilesOnly`, `monitorOutgoingFilesOnly`.|
|defenderProcessesToExclude|Colección String|Procesos que se van a excluir de los análisis y la protección en tiempo real.|
|defenderPromptForSampleSubmission|[defenderPromptForSampleSubmission](../resources/intune_deviceconfig_defenderpromptforsamplesubmission.md)|La configuración de cómo solicitar confirmación de usuario para el envío de muestras. Los valores posibles son: `userDefined`, `alwaysPrompt`, `promptBeforeSendingPersonalData`, `neverSendData`, `sendAllDataWithoutPrompting`.|
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
|defenderScanType|[defenderScanType](../resources/intune_deviceconfig_defenderscantype.md)|El tipo de análisis de sistema de Defender. Los valores posibles son: `userDefined`, `disabled`, `quick`, `full`.|
|defenderScheduledScanTime|TimeOfDay|Hora de Defender para el análisis del sistema.|
|defenderScheduledQuickScanTime|TimeOfDay|Hora en la que se realiza un análisis rápido diariamente.|
|defenderCloudBlockLevel|[defenderCloudBlockLevelType](../resources/intune_deviceconfig_defendercloudblockleveltype.md)|Especifica el nivel de protección proporcionada en la nube. Los valores posibles son: `notConfigured`, `high`, `highPlus`, `zeroTolerance`.|
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
|passwordRequiredType|[requiredPasswordType](../resources/intune_deviceconfig_requiredpasswordtype.md)|El tipo de contraseña requerida. Los valores posibles son: `deviceDefault`, `alphanumeric`, `numeric`.|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica. Valores válidos de 0 a 999.|
|privacyAdvertisingId|[stateManagementSetting](../resources/intune_deviceconfig_statemanagementsetting.md)|Habilita o deshabilita el uso del identificador de publicidad. Se agregó en Windows 10, versión 1607. Los valores posibles son: `notConfigured`, `blocked`, `allowed`.|
|privacyAutoAcceptPairingAndConsentPrompts|Booleano|Indica si se va a permitir la aceptación automática de los cuadros de diálogo de consentimiento del usuario de emparejamiento y privacidad al iniciar aplicaciones.|
|privacyBlockInputPersonalization|Booleano|Indica si se va a bloquear el uso de servicios de voz basados en la nube de Cortana, el dictado o las aplicaciones de la tienda.|
|startBlockUnpinningAppsFromTaskbar|Booleano|Indica si se va a impedir que el usuario desancle aplicaciones de la barra de tareas.|
|startMenuAppListVisibility|[windowsStartMenuAppListVisibilityType](../resources/intune_deviceconfig_windowsstartmenuapplistvisibilitytype.md)|Al establecer el valor de esto se contrae la lista de aplicaciones, se quita completamente la lista de aplicaciones o se deshabilita la alternancia correspondiente en la aplicación de configuración. Los valores posibles son: `userDefined`, `collapse`, `remove`, `disableSettingsApp`.|
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
|startMenuMode|[windowsStartMenuModeType](../resources/intune_deviceconfig_windowsstartmenumodetype.md)|Permite a los administradores decidir cómo se muestra el menú Inicio. Los valores posibles son: `userDefined`, `fullScreen`, `nonFullScreen`.|
|startMenuPinnedFolderDocuments|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Documentos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderDownloads|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Descargas en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderFileExplorer|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo del Explorador de archivos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderHomeGroup|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Grupo Hogar en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderMusic|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Música en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderNetwork|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Red en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderPersonalFolder|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta personal en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderPictures|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Imágenes en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderSettings|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Configuración en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
|startMenuPinnedFolderVideos|[visibilitySetting](../resources/intune_deviceconfig_visibilitysetting.md)|Controla la visibilidad (mostrar u ocultar) del acceso directo de la carpeta Vídeos en el menú Inicio. Los valores posibles son: `notConfigured`, `hide`, `show`.|
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
|windowsSpotlightConfigureOnLockScreen|[windowsSpotlightEnablementSettings](../resources/intune_deviceconfig_windowsspotlightenablementsettings.md)|Especifica el tipo de Destacados. Los valores posibles son: `notConfigured`, `disabled` y `enabled`.|
|networkProxyApplySettingsDeviceWide|Booleano|Si se establece, la configuración de proxy se aplicará a todos los procesos y cuentas en el dispositivo. En caso contrario, se aplicará a la cuenta de usuario que está inscrita en MDM.|
|networkProxyDisableAutoDetect|Booleano|Deshabilitar la detección automática de la configuración. Si está habilitada, el sistema intentará encontrar la ruta de acceso a un script de configuración automática de proxy (PAC).|
|networkProxyAutomaticConfigurationUrl|Cadena|Dirección al script de configuración automática de proxy (PAC) que quiera usar.|
|networkProxyServer|[windows10NetworkProxyServer](../resources/intune_deviceconfig_windows10networkproxyserver.md)|Especifica la configuración manual del servidor proxy.|
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
|safeSearchFilter|[safeSearchFilterType](../resources/intune_deviceconfig_safesearchfiltertype.md)|Especifica qué nivel de filtro de búsqueda segura es necesario. Los valores posibles son: `userDefined`, `strict`, `moderate`.|
|edgeBlockPopups|Booleano|Indica si se van a bloquear los elementos emergentes.|
|edgeBlockSearchSuggestions|Booleano|Indica si se va a impedir que el usuario utilice las sugerencias de búsqueda en la barra de direcciones.|
|edgeBlockSendingIntranetTrafficToInternetExplorer|Booleano|Indica si se va a impedir que el usuario envíe tráfico de Intranet a Internet Explorer desde Edge.|
|edgeRequireSmartScreen|Booleano|Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.|
|edgeEnterpriseModeSiteListLocation|Cadena|Indica la ubicación de la lista de sitios del modo de empresa. Puede ser un archivo local, la red local o la ubicación http.|
|edgeFirstRunUrl|Cadena|Primera dirección URL que se ejecuta al abrir el explorador Edge por primera vez.|
|edgeSearchEngine|[edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)|Permite que los administradores de TI configuren un motor de búsqueda predeterminado para dispositivos controlados por MDM. Los usuarios pueden invalidarla y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.|
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
|appsAllowTrustedAppsSideloading|[stateManagementSetting](../resources/intune_deviceconfig_statemanagementsetting.md)|Indica si las aplicaciones desde paquetes AppX firmados con un certificado de confianza se pueden transferir localmente. Los valores posibles son: `notConfigured`, `blocked`, `allowed`.|
|windowsStoreBlockAutoUpdate|Booleano|Indica si se va a bloquear la actualización automática de aplicaciones desde la Tienda Windows.|
|developerUnlockSetting|[stateManagementSetting](../resources/intune_deviceconfig_statemanagementsetting.md)|Indica si se permite o no el desbloqueo para desarrolladores. Los valores posibles son: `notConfigured`, `blocked`, `allowed`.|
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



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10GeneralConfiguration](../resources/intune_deviceconfig_windows10generalconfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 9767

{
  "@odata.type": "#microsoft.graph.windows10GeneralConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enterpriseCloudPrintDiscoveryEndPoint": "Enterprise Cloud Print Discovery End Point value",
  "enterpriseCloudPrintOAuthAuthority": "Enterprise Cloud Print OAuth Authority value",
  "enterpriseCloudPrintOAuthClientIdentifier": "Enterprise Cloud Print OAuth Client Identifier value",
  "enterpriseCloudPrintResourceIdentifier": "Enterprise Cloud Print Resource Identifier value",
  "enterpriseCloudPrintDiscoveryMaxLimit": 5,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "Enterprise Cloud Print Mopria Discovery Resource Identifier value",
  "searchBlockDiacritics": true,
  "searchDisableAutoLanguageDetection": true,
  "searchDisableIndexingEncryptedItems": true,
  "searchEnableRemoteQueries": true,
  "searchDisableIndexerBackoff": true,
  "searchDisableIndexingRemovableDrive": true,
  "searchEnableAutomaticIndexSizeManangement": true,
  "diagnosticsDataSubmissionMode": "none",
  "oneDriveDisableFileSync": true,
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
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
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
  "privacyAdvertisingId": "blocked",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
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
  "logonBlockFastUserSwitching": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 9875

{
  "@odata.type": "#microsoft.graph.windows10GeneralConfiguration",
  "id": "a4235d71-5d71-a423-715d-23a4715d23a4",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enterpriseCloudPrintDiscoveryEndPoint": "Enterprise Cloud Print Discovery End Point value",
  "enterpriseCloudPrintOAuthAuthority": "Enterprise Cloud Print OAuth Authority value",
  "enterpriseCloudPrintOAuthClientIdentifier": "Enterprise Cloud Print OAuth Client Identifier value",
  "enterpriseCloudPrintResourceIdentifier": "Enterprise Cloud Print Resource Identifier value",
  "enterpriseCloudPrintDiscoveryMaxLimit": 5,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "Enterprise Cloud Print Mopria Discovery Resource Identifier value",
  "searchBlockDiacritics": true,
  "searchDisableAutoLanguageDetection": true,
  "searchDisableIndexingEncryptedItems": true,
  "searchEnableRemoteQueries": true,
  "searchDisableIndexerBackoff": true,
  "searchDisableIndexingRemovableDrive": true,
  "searchEnableAutomaticIndexSizeManangement": true,
  "diagnosticsDataSubmissionMode": "none",
  "oneDriveDisableFileSync": true,
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
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
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
  "privacyAdvertisingId": "blocked",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
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
  "logonBlockFastUserSwitching": true
}
```








