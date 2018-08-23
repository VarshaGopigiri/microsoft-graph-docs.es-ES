# <a name="automaticupdatemode-enum-type"></a>Tipo de enumeración automaticUpdateMode

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para el modo de actualización automática.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Definido por el usuario, valor predeterminado, sin intención.|
|notifyDownload|1|Notificar al descargar.|
|autoInstallAtMaintenanceTime|2|Instalación automática en horas de mantenimiento.|
|autoInstallAndRebootAtMaintenanceTime|3|Instalación automática y reinicio del equipo en horas de mantenimiento.|
|autoInstallAndRebootAtScheduledTime|4|Instalación automática y reinicio del equipo a la hora programada.|
|autoInstallAndRebootWithoutEndUserControl|5|Instalación automática y reinicio sin control del usuario final.|



