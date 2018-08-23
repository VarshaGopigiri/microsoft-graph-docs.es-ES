# <a name="managedappdataencryptiontype-enum-type"></a>Tipo de enumeración managedAppDataEncryptionType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa el nivel al que se cifran los datos de las aplicaciones para las aplicaciones administradas.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|useDeviceSettings|0|Los datos de las aplicaciones se cifran según la configuración predeterminada en el dispositivo.|
|afterDeviceRestart|1|Los datos de las aplicaciones se cifran cuando se reinicia el dispositivo.|
|whenDeviceLockedExceptOpenFiles|2|Los datos de las aplicaciones asociadas con esta directiva se cifran cuando el dispositivo se bloquea, excepto los datos de los archivos que están abiertos.|
|whenDeviceLocked|3|Los datos de las aplicaciones asociadas con esta directiva se cifran cuando el dispositivo se bloquea.|



