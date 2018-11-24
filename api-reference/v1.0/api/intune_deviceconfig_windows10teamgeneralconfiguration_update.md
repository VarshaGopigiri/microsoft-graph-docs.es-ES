# <a name="update-windows10teamgeneralconfiguration"></a>Actualizar windows10TeamGeneralConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).
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
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).

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



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1150

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1322

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "0c94aa20-aa20-0c94-20aa-940c20aa940c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```



