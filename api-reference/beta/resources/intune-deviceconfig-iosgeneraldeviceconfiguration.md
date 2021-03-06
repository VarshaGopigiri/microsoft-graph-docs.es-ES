---
title: Tipo de recurso iosGeneralDeviceConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso iosGeneralDeviceConfiguration.
localization_priority: Normal
ms.openlocfilehash: e1175dc27e4bd6e073b15ec6487650e3a9882bf1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880594"
---
# <a name="iosgeneraldeviceconfiguration-resource-type"></a>Tipo de recurso iosGeneralDeviceConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso iosGeneralDeviceConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosGeneralDeviceConfigurations](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-list.md)|Colección [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).|
|[Obtener iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-get.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|Lea las propiedades y las relaciones del objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).|
|[Crear iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-create.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|Cree un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).|
|[Eliminar iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-delete.md)|Ninguno|Elimina un [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).|
|[Actualizar iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-update.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|Actualice las propiedades de un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).|

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
|accountBlockModification|Booleano|Indica si se va a permitir la modificación de cuentas cuando el dispositivo está en modo supervisado.|
|activationLockAllowWhenSupervised|Booleano|Indica si se va a permitir el bloqueo de activación cuando el dispositivo está en modo supervisado.|
|airDropBlocked|Booleano|Indica si se va a permitir AirDrop cuando el dispositivo está en modo supervisado.|
|airDropForceUnmanagedDropTarget|Booleano|Indica si se va a hacer que AirDrop se considere un destino de colocación no administrado (iOS 9.0 o posterior).|
|airPlayForcePairingPasswordForOutgoingRequests|Booleano|Indica si se va a forzar que todos los dispositivos que reciban solicitudes de AirPlay de este dispositivo usen una contraseña de emparejamiento.|
|appleWatchBlockPairing|Booleano|Indica si se va a permitir el emparejamiento con Apple Watch cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).|
|appleWatchForceWristDetection|Booleano|Indica si se va a forzar que un Apple Watch emparejado use la detección de muñeca (iOS 8.2 y posteriores).|
|appleNewsBlocked|Booleano|Indica si se va a impedir que el usuario use Noticias cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).|
|appsSingleAppModeList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Obtiene o establece la lista de aplicaciones permitidas de iOS que pueden entrar de forma autónoma en el Modo de aplicación única. Solo bajo supervisión. iOS 7.0 y versiones posteriores. Esta colección puede contener un máximo de 500 elementos.|
|appsVisibilityList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones en la lista de visibilidad (sea la lista de aplicaciones visibles o que se pueden iniciar o la lista de aplicaciones ocultas o que no se pueden iniciar, controlada por AppsVisibilityListType) (iOS 9.3 y versiones posteriores). Esta colección puede contener un máximo de 10 000 elementos.|
|appsVisibilityListType|[appListType](../resources/intune-deviceconfig-applisttype.md)|Tipo de lista que se encuentra en la AppsVisibilityList. Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.|
|appStoreBlockAutomaticDownloads|Booleano|Indica si se va a bloquear la descarga automática de aplicaciones compradas en otros dispositivos cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).|
|appStoreBlocked|Booleano|Indica si se va a impedir que el usuario use el App Store.|
|appStoreBlockInAppPurchases|Booleano|Indica si se va a impedir que el usuario haga compras en la aplicación.|
|appStoreBlockUIAppInstallation|Booleano|Indica si se va a bloquear la aplicación App Store, sin restringir la instalación mediante aplicaciones host. Se aplica solo al modo supervisado (iOS 9.0 o posterior).|
|appStoreRequirePassword|Booleano|Indica si se va a requerir una contraseña cuando se use la tienda de aplicaciones.|
|bluetoothBlockModification|Booleano|Indica si se va a permitir la modificación de la configuración Bluetooth cuando el dispositivo está en modo supervisado (iOS 10.0 o posterior).|
|cameraBlocked|Booleano|Indica si se va a impedir que el usuario obtenga acceso a la cámara del dispositivo.|
|cellularBlockDataRoaming|Booleano|Indica si se va a bloquear la itinerancia de datos.|
|cellularBlockGlobalBackgroundFetchWhileRoaming|Booleano|Indica si se va a impedir la captura de fondo global mientras se está en itinerancia.|
|cellularBlockPerAppDataModification|Booleano|Indica si se van a permitir los cambios en la configuración de uso de datos de aplicaciones de telefonía móvil cuando el dispositivo está en modo supervisado.|
|cellularBlockPersonalHotspot|Booleano|Indica si se va a bloquear el punto de acceso personal.|
|cellularBlockVoiceRoaming|Booleano|Indica si se va a bloquear la itinerancia de voz.|
|certificatesBlockUntrustedTlsCertificates|Booleano|Indica si se van a bloquear los certificados TLS que no son de confianza.|
|classroomAppBlockRemoteScreenObservation|Booleano|Indica si se va a permitir la observación de pantalla remota de la aplicación Classroom cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).|
|classroomAppForceUnpromptedScreenObservation|Booleano|Indica si se va a autorizar de forma automática al profesor de un curso administrado en la aplicación Classroom para que vea la pantalla de un alumno sin preguntarle cuando el dispositivo está en modo supervisado.|
|compliantAppsList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType). Esta colección puede contener un máximo de 10 000 elementos.|
|compliantAppListType|[appListType](../resources/intune-deviceconfig-applisttype.md)|Lista que se encuentra en la AppComplianceList. Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.|
|configurationProfileBlockChanges|Booleano|Indica si se va a impedir que el usuario instale perfiles de configuración y certificados de forma interactiva cuando el dispositivo está en modo supervisado.|
|definitionLookupBlocked|Booleano|Indica si se va a bloquear la búsqueda de definiciones cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).|
|deviceBlockEnableRestrictions|Booleano|Indica si se va a permitir que el usuario active las restricciones en los ajustes del dispositivo cuando el dispositivo está en modo supervisado.|
|deviceBlockEraseContentAndSettings|Booleano|Indica si se va a permitir el uso de la opción "Borrar todo el contenido y la configuración" en el dispositivo cuando el dispositivo está en modo supervisado.|
|deviceBlockNameModification|Booleano|Indica si se va a permitir modificar el nombre del dispositivo cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).|
|diagnosticDataBlockSubmission|Booleano|Indica si se va a bloquear el envío de datos de diagnóstico.|
|diagnosticDataBlockSubmissionModification|Booleano|Indica si se va a permitir modificar los ajustes del envío de diagnósticos cuando el dispositivo está en modo supervisado (iOS 9.3.2 o posterior).|
|documentsBlockManagedDocumentsInUnmanagedApps|Booleano|Indica si se va a impedir que el usuario visualice documentos administrados en las aplicaciones no administradas.|
|documentsBlockUnmanagedDocumentsInManagedApps|Booleano|Indica si se va a impedir que el usuario visualice documentos no administrados en las aplicaciones administradas.|
|emailInDomainSuffixes|Colección String|Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.|
|enterpriseAppBlockTrust|Booleano|Indica si se va a impedir que el usuario confíe en una aplicación empresarial.|
|enterpriseAppBlockTrustModification|Booleano|Indica si se va a impedir que el usuario modifique la configuración de confianza de una aplicación empresarial.|
|faceTimeBlocked|Booleano|Indica si se va a impedir que el usuario use FaceTime.|
|findMyFriendsBlocked|Booleano|Indica si se va a bloquear Buscar a mis amigos cuando el dispositivo está en modo supervisado.|
|gamingBlockGameCenterFriends|Booleano|Indica si se va a impedir que el usuario tenga amigos en el Game Center.|
|gamingBlockMultiplayer|Booleano|Indica si se va a impedir que el usuario use los juegos multijugador.|
|gameCenterBlocked|Booleano|Indica si se va a impedir que el usuario use el Game Center cuando el dispositivo está en modo supervisado.|
|hostPairingBlocked|Booleano|Indica si se va a permitir el emparejamiento de host para controlar los dispositivos con los que se puede emparejar un dispositivo iOS cuando el dispositivo iOS está en modo supervisado.|
|iBooksStoreBlocked|Booleano|Indica si se va a impedir que el usuario use iBooks Store cuando el dispositivo está en modo supervisado.|
|iBooksStoreBlockErotica|Booleano|Indica si se va a impedir que el usuario descargue archivos multimedia desde el iBook Store que se han etiquetado como eróticos.|
|iCloudBlockActivityContinuation|Booleano|Indica si se va a impedir que el usuario continúe con el trabajo que empezó en el dispositivo iOS en otro dispositivo macOS o iOS.|
|iCloudBlockBackup|Booleano|Indica si se va a impedir la copia de seguridad de iCloud.|
|iCloudBlockDocumentSync|Booleano|Indica si se va a impedir la sincronización de documentos de iCloud.|
|iCloudBlockManagedAppsSync|Booleano|Indica si se va a impedir la sincronización en la nube de aplicaciones administradas.|
|iCloudBlockPhotoLibrary|Booleano|Indica si se va a bloquear la Fototeca de iCloud.|
|iCloudBlockPhotoStreamSync|Booleano|Indica si se va a bloquear la sincronización de fotos en streaming de iCloud.|
|iCloudBlockSharedPhotoStream|Booleano|Indica si se va a bloquear la sincronización de fotos en streaming compartidas.|
|iCloudRequireEncryptedBackup|Booleano|Indica si se va a requerir que las copias de seguridad de iCloud estén cifradas.|
|iTunesBlockExplicitContent|Booleano|Indica si se va a impedir que el usuario obtenga acceso a contenido explícito en iTunes y el App Store.|
|iTunesBlockMusicService|Booleano|Indica si se va a bloquear el servicio Música y revertir la aplicación Música al modo clásico cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores, y macOS 10.12 y versiones posteriores).|
|iTunesBlockRadio|Booleano|Indica si se va a impedir que el usuario use iTunes Radio cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).|
|keyboardBlockAutoCorrect|Booleano|Indica si se va a bloquear el autocorrector cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).|
|keyboardBlockDictation|Booleano|Indica si se va a impedir que el usuario use la entrada dictada cuando el dispositivo está en modo supervisado.|
|keyboardBlockPredictive|Booleano|Indica si se van a bloquear los teclados predictivos cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).|
|keyboardBlockShortcuts|Booleano|Indica si se van a bloquear los atajos del teclado cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).|
|keyboardBlockSpellCheck|Booleano|Indica si se va a bloquear la revisión ortográfica cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).|
|kioskModeAllowAssistiveSpeak|Booleano|Indica si se va a permitir la lectura de asistencia en el modo de pantalla completa.|
|kioskModeAllowAssistiveTouchSettings|Booleano|Indica si se va a permitir el acceso a la configuración de AssistiveTouch en el modo de pantalla completa.|
|kioskModeAllowAutoLock|Booleano|Indica si se va a permitir el bloqueo automático del dispositivo en el modo de pantalla completa.|
|kioskModeAllowColorInversionSettings|Booleano|Indica si se va a permitir el acceso a la configuración de la inversión del color en el modo de pantalla completa.|
|kioskModeAllowRingerSwitch|Booleano|Indica si se va a permitir el uso del cambio de tono en el modo de pantalla completa.|
|kioskModeAllowScreenRotation|Booleano|Indica si se va a permitir la rotación de pantalla en el modo de pantalla completa.|
|kioskModeAllowSleepButton|Booleano|Indica si se va a permitir el uso del botón de suspensión en el modo de pantalla completa.|
|kioskModeAllowTouchscreen|Booleano|Indica si se va a permitir el uso de la pantalla táctil en el modo de pantalla completa.|
|kioskModeAllowVoiceOverSettings|Booleano|Indica si se va a permitir el acceso a la configuración de voz en off en el modo de pantalla completa.|
|kioskModeAllowVolumeButtons|Booleano|Indica si se va a permitir el uso de los botones de volumen en el modo de pantalla completa.|
|kioskModeBlockVolumeButtons|Booleano|Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.|
|kioskModeAllowZoomSettings|Booleano|Indica si se va a permitir el acceso a la configuración de zoom en el modo de pantalla completa.|
|kioskModeAppStoreUrl|Cadena|Dirección URL en la tienda de aplicaciones a la aplicación que se usará para el modo de pantalla completa. Úsela si KioskModeManagedAppId es desconocido.|
|kioskModeBuiltInAppId|Cadena|Identificador de aplicaciones integradas que se usará para el modo de pantalla completa. Se usa cuando no se establecen KioskModeManagedAppId y KioskModeAppStoreUrl.|
|kioskModeRequireAssistiveTouch|Booleano|Indica si se va a requerir la AssistiveTouch en el modo de pantalla completa.|
|kioskModeRequireColorInversion|Booleano|Indica si se va a requerir la inversión de color en el modo de pantalla completa.|
|kioskModeRequireMonoAudio|Booleano|Indica si se va a requerir el audio mono en el modo de pantalla completa.|
|kioskModeRequireVoiceOver|Booleano|Indica si se va a requerir la voz en off en el modo de pantalla completa.|
|kioskModeRequireZoom|Booleano|Indica si se va a requerir el zoom en el modo de pantalla completa.|
|kioskModeManagedAppId|Cadena|identificador de la aplicación administrada de la aplicación que se usará para el modo de pantalla completa. Si se especifica KioskModeManagedAppId, entonces se omitirá KioskModeAppStoreUrl.|
|lockScreenBlockControlCenter|Booleano|Indica si se va a impedir que el usuario use el centro de control en la pantalla de bloqueo.|
|lockScreenBlockNotificationView|Booleano|Indica si se va a impedir que el usuario use la visualización de notificaciones en la pantalla de bloqueo.|
|lockScreenBlockPassbook|Booleano|Indica si se va a impedir que el usuario use Passbook cuando el dispositivo está bloqueado.|
|lockScreenBlockTodayView|Booleano|Indica si se va a impedir que el usuario use la vista Hoy en la pantalla de bloqueo.|
|mediaContentRatingAustralia|[mediaContentRatingAustralia](../resources/intune-deviceconfig-mediacontentratingaustralia.md)|Clasificación de contenido multimedia para Australia|
|mediaContentRatingCanada|[mediaContentRatingCanada](../resources/intune-deviceconfig-mediacontentratingcanada.md)|Clasificación de contenido multimedia para Canadá|
|mediaContentRatingFrance|[mediaContentRatingFrance](../resources/intune-deviceconfig-mediacontentratingfrance.md)|Clasificación de contenido multimedia para Francia|
|mediaContentRatingGermany|[mediaContentRatingGermany](../resources/intune-deviceconfig-mediacontentratinggermany.md)|Clasificación de contenido multimedia para Alemania|
|mediaContentRatingIreland|[mediaContentRatingIreland](../resources/intune-deviceconfig-mediacontentratingireland.md)|Clasificación de contenido multimedia para Irlanda|
|mediaContentRatingJapan|[mediaContentRatingJapan](../resources/intune-deviceconfig-mediacontentratingjapan.md)|Clasificación de contenido multimedia para Japón|
|mediaContentRatingNewZealand|[mediaContentRatingNewZealand](../resources/intune-deviceconfig-mediacontentratingnewzealand.md)|Clasificación de contenido multimedia para Nueva Zelanda|
|mediaContentRatingUnitedKingdom|[mediaContentRatingUnitedKingdom](../resources/intune-deviceconfig-mediacontentratingunitedkingdom.md)|Clasificación de contenido multimedia para el Reino Unido|
|mediaContentRatingUnitedStates|[mediaContentRatingUnitedStates](../resources/intune-deviceconfig-mediacontentratingunitedstates.md)|Clasificación de contenido multimedia para Estados Unidos|
|networkUsageRules|Colección [iosNetworkUsageRule](../resources/intune-deviceconfig-iosnetworkusagerule.md)|Lista de aplicaciones administradas y las reglas de red que se les aplican. Esta colección puede contener un máximo de 1000 elementos.|
|mediaContentRatingApps|[ratingAppsType](../resources/intune-deviceconfig-ratingappstype.md)|Configuración de clasificación para las aplicaciones de contenido de medios. Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.|
|messagesBlocked|Booleano|Indica si se va a impedir que el usuario use la aplicación Mensajes en el dispositivo supervisado.|
|notificationsBlockSettingsModification|Booleano|Indica si se van a permitir modificar la configuración de las notificaciones (iOS 9,3 y versiones posteriores).|
|passcodeBlockFingerprintUnlock|Booleano|Indica si se va a impedir el desbloqueo por huella dactilar.|
|passcodeBlockFingerprintModification|Booleano|Impide la modificación de huellas digitales registradas de Touch ID en el modo supervisado.|
|passcodeBlockModification|Booleano|Indica si se va a permitir modificar los códigos de acceso cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).|
|passcodeBlockSimple|Booleano|Indica si se van a bloquear los códigos de acceso simples.|
|passcodeExpirationDays|Int32|Número de días antes de que expire el código de acceso. Valores válidos de 1 a 65535|
|passcodeMinimumLength|Int32|Longitud mínima de los códigos de acceso. Valores válidos de 4 a 14|
|passcodeMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesario un código de acceso.|
|passcodeMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.|
|passcodeMinimumCharacterSetCount|Int32|Número de juegos de caracteres que debe contener un código de acceso. Valores válidos de 0 a 4.|
|passcodePreviousPasscodeBlockCount|Int32|Número de códigos de acceso anteriores que bloquear. Valores válidos de 1 a 24.|
|passcodeSignInFailureCountBeforeWipe|Int32|Número de errores de inicio de sesión permitidos antes de borrar los datos del dispositivo. Valores válidos de 4 a 11|
|passcodeRequiredType|[requiredPasswordType](../resources/intune-deviceconfig-requiredpasswordtype.md)|Tipo de código de acceso necesario. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passcodeRequired|Booleano|Indica si se va a requerir un código de acceso.|
|podcastsBlocked|Booleano|Indica si se va a impedir que el usuario use Podcasts cuando el dispositivo está en modo supervisado (iOS 8.0 o posterior).|
|safariBlockAutofill|Booleano|Indica si se va a impedir que el usuario use la opción de autorrellenado en Safari.|
|safariBlockJavaScript|Booleano|Indica si se va a bloquear JavaScript en Safari.|
|safariBlockPopups|Booleano|Indica si se van a bloquear los elementos emergentes en Safari.|
|safariBlocked|Booleano|Indica si se va a impedir que el usuario use Safari.|
|safariCookieSettings|[webBrowserCookieSettings](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|Configuración de cookies para Safari. Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.|
|safariManagedDomains|Colección String|Las direcciones URL que coinciden con los patrones que se enumeran aquí se considerarán administradas.|
|safariPasswordAutoFillDomains|Colección String|Los usuarios pueden guardar las contraseñas en Safari únicamente de las direcciones URL que coinciden con los patrones que se enumeran aquí. Se aplica solo a dispositivos en modo supervisado (iOS 9.3 o posterior).|
|safariRequireFraudWarning|Booleano|Indica si se va a requerir una advertencia de fraude en Safari.|
|screenCaptureBlocked|Booleano|Indica si se impide o no que el usuario tome capturas de pantalla.|
|siriBlocked|Booleano|Indica si se va a impedir que el usuario use Siri.|
|siriBlockedWhenLocked|Booleano|Indica si se va a impedir que el usuario use Siri cuando está bloqueado.|
|siriBlockUserGeneratedContent|Booleano|Indica si se va a impedir que Siri haga consultas de contenido generado por el usuario cuando se usa en un dispositivo supervisado.|
|siriRequireProfanityFilter|Booleano|Indica si se va a evitar que Siri dicte o hable con lenguaje irreverente en un dispositivo supervisado.|
|spotlightBlockInternetResults|Booleano|Indica si se va a impedir que la búsqueda Spotlight devuelva resultados de Internet en un dispositivo supervisado.|
|voiceDialingBlocked|Booleano|Indica si se va a bloquear la marcación por voz.|
|wallpaperBlockModification|Booleano|Indica si se va permitir modificar el fondo de pantalla en un dispositivo supervisado (iOS 9.0 o posterior).|
|wiFiConnectOnlyToConfiguredNetworks|Booleano|Indica si se va a forzar al dispositivo para que use solo redes Wi-Fi de perfiles de configuración cuando el dispositivo está en modo supervisado.|
|classroomForceRequestPermissionToLeaveClasses|Booleano|Indica si un estudiante inscrito en un curso de no administrado a través de aula solicitará permiso del profesor al intentar deje el curso (iOS 11.3 y versiones posteriores).|
|keychainBlockCloudSync|Booleano|Indica si se bloquea iCloud llaves sincronización.|
|pkiBlockOTAUpdates|Booleano|Indica si está o no están bloqueadas por aire actualizaciones PKI. Si se establece esta restricción a false no deshabilitar las comprobaciones de CRL y OCSP (iOS 7.0 y versiones posteriores).|
|privacyForceLimitAdTracking|Booleano|Indica si el seguimiento de anuncios está limitado. (iOS 7.0 y versiones posteriores).|
|enterpriseBookBlockBackup|Booleano|Indica si Enterprise book copia de seguridad está bloqueado.|
|enterpriseBookBlockMetadataSync|Booleano|Indica si se bloquea en Enterprise libreta de direcciones, notas y resalta la sincronización.|
|airPrintBlocked|Booleano|Indica si está o no AirPrint bloqueados (iOS 11.0 y versiones posteriores).|
|airPrintBlockCredentialsStorage|Booleano|Indica si está o no llaves almacenamiento de nombre de usuario y la contraseña de Airprint bloqueados (iOS 11.0 y versiones posteriores).|
|airPrintForceTrustedTLS|Booleano|Indica si los certificados de confianza son necesarios para la comunicación de impresión de TLS (iOS 11.0 y versiones posteriores).|
|airPrintBlockiBeaconDiscovery|Booleano|Indica si se bloquea en iBeacon detección de impresoras AirPrint. Esto evita falsas balizas de AirPrint Bluetooth de suplantación de identidad para el tráfico de red (iOS 11.0 y versiones posteriores).|
|blockSystemAppRemoval|Booleano|Indica si la eliminación de las aplicaciones del sistema desde el dispositivo está bloqueada en un dispositivo supervisado (iOS 11.0 y versiones posteriores).|
|vpnBlockCreation|Booleano|Indica si está o no la creación de configuraciones de VPN bloqueados (iOS 11.0 y versiones posteriores).|

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

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosGeneralDeviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
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
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "appsVisibilityListType": "String",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "compliantAppListType": "String",
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "String"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeBlockVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "String",
  "kioskModeBuiltInAppId": "String",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "String",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "String",
    "tvRating": "String"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "String",
          "publisher": "String",
          "appStoreUrl": "String",
          "appId": "String"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "String",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 1024,
  "passcodeMinimumLength": 1024,
  "passcodeMinutesOfInactivityBeforeLock": 1024,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passcodeMinimumCharacterSetCount": 1024,
  "passcodePreviousPasscodeBlockCount": 1024,
  "passcodeSignInFailureCountBeforeWipe": 1024,
  "passcodeRequiredType": "String",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "String",
  "safariManagedDomains": [
    "String"
  ],
  "safariPasswordAutoFillDomains": [
    "String"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true,
  "classroomForceRequestPermissionToLeaveClasses": true,
  "keychainBlockCloudSync": true,
  "pkiBlockOTAUpdates": true,
  "privacyForceLimitAdTracking": true,
  "enterpriseBookBlockBackup": true,
  "enterpriseBookBlockMetadataSync": true,
  "airPrintBlocked": true,
  "airPrintBlockCredentialsStorage": true,
  "airPrintForceTrustedTLS": true,
  "airPrintBlockiBeaconDiscovery": true,
  "blockSystemAppRemoval": true,
  "vpnBlockCreation": true
}
```





