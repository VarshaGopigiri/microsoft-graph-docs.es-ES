# <a name="windows10teamgeneralconfiguration-resource-type"></a>Tipo de recurso windows10TeamGeneralConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windows10TeamGeneralConfiguration.

Hereda de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows10TeamGeneralConfigurations](../api/intune_deviceconfig_windows10teamgeneralconfiguration_list.md)|Colección [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).|
|[Obtener windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_get.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|Lea las propiedades y las relaciones del objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).|
|[Crear windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_create.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|Cree un objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).|
|[Eliminar windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_delete.md)|Ninguno|Elimina un [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).|
|[Actualizar windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_update.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|Actualice las propiedades de un objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|description|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|azureOperationalInsightsBlockTelemetry|Booleano|Indica si se va a bloquear Azure Operational Insights.|
|azureOperationalInsightsWorkspaceId|String|Identificador del área de trabajo de Azure Operational Insights.|
|azureOperationalInsightsWorkspaceKey|String|Clave del área de trabajo de Azure Operational Insights.|
|connectAppBlockAutoLaunch|Booleano|Especifica si se iniciará automáticamente la aplicación Conectar cada vez que se inicie un proyecto.|
|maintenanceWindowBlocked|Booleano|Indica si se va a bloquear la configuración de un período de mantenimiento para las actualizaciones del dispositivo.|
|maintenanceWindowDurationInHours|Int32|Duración del período de mantenimiento para las actualizaciones del dispositivo. Valores válidos de 0 a 5|
|maintenanceWindowStartTime|TimeOfDay|Hora de inicio del periodo de mantenimiento para las actualizaciones del dispositivo.|
|miracastChannel|[miracastChannel](../resources/intune_deviceconfig_miracastchannel.md)|Canal. Los valores posibles son: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne` y `oneHundredSixtyFive`.|
|miracastBlocked|Booleano|Indica si se van a bloquear las proyecciones inalámbricas.|
|miracastRequirePin|Booleano|Indica si se va a requerir un PIN para las proyecciones inalámbricas.|
|settingsBlockMyMeetingsAndFiles|Booleano|Especifica si se deshabilita la característica "Mis reuniones y archivos" en el menú Inicio, que muestra las reuniones y los archivos del usuario que ha iniciado sesión en Office 365.|
|settingsBlockSessionResume|Booleano|Especifica si se permite la posibilidad de reanudar una sesión cuando se agota el tiempo de espera de la sesión.|
|settingsBlockSigninSuggestions|Booleano|Especifica si se deshabilita la opción de rellenar automáticamente el cuadro de diálogo de inicio de sesión con invitados de reuniones programadas.|
|settingsDefaultVolume|Int32|Especifica el valor de volumen predeterminado para una nueva sesión. Los valores permitidos son de 0 a 100. El valor predeterminado es 45. Valores válidos de 0 a 100.|
|settingsScreenTimeoutInMinutes|Int32|Especifica el número de minutos hasta que se desconecta la pantalla Concentrador.|
|settingsSessionTimeoutInMinutes|Int32|Especifica el número de minutos hasta que se agota el tiempo de espera de la sesión.|
|settingsSleepTimeoutInMinutes|Int32|Especifica el número de minutos hasta que el concentrador entra en modo de suspensión.|
|welcomeScreenBlockAutomaticWakeUp|Booleano|Indica si se va a impedir que la pantalla de inicio de sesión se reactive automáticamente cuando alguien entre en la sala.|
|welcomeScreenBackgroundImageUrl|String|Dirección URL de la imagen de fondo de la pantalla de inicio de sesión. La dirección URL debe utilizar el protocolo HTTPS y devolver una imagen PNG.|
|welcomeScreenMeetingInformation|[welcomeScreenMeetingInformation](../resources/intune_deviceconfig_welcomescreenmeetinginformation.md)|Información de la reunión que se muestra en la pantalla de inicio de sesión. Los valores posibles son: `userDefined`, `showOrganizerAndTimeOnly` y `showOrganizerAndTimeAndSubject`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|assignments|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10TeamGeneralConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "String",
  "azureOperationalInsightsWorkspaceKey": "String",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 1024,
  "maintenanceWindowStartTime": "String (time of day)",
  "miracastChannel": "String",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 1024,
  "settingsScreenTimeoutInMinutes": 1024,
  "settingsSessionTimeoutInMinutes": 1024,
  "settingsSleepTimeoutInMinutes": 1024,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "String",
  "welcomeScreenMeetingInformation": "String"
}
```



