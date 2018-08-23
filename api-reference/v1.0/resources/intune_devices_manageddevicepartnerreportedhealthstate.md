# <a name="manageddevicepartnerreportedhealthstate-enum-type"></a>Tipo de enumeración managedDevicePartnerReportedHealthState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de mantenimiento disponibles para la API de estado de dispositivo
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|unknown|0|El estado de mantenimiento del dispositivo no se ha notificado|
|activated|1|El dispositivo ha sido activado por un socio de defensa de amenazas móviles, pero aún no ha notificado el estado.|
|deactivated|2|El dispositivo ha sido desactivado por un socio de defensa de amenazas móviles. No se conoce el estado del dispositivo.|
|secured|3|El socio de defensa de amenazas móviles considera el dispositivo como seguro.|
|lowSeverity|4|El socio de defensa de amenazas móviles considera el dispositivo como amenaza baja.|
|mediumSeverity|5|El socio de defensa de amenazas móviles considera el dispositivo como amenaza media.|
|highSeverity|6|El socio de defensa de amenazas móviles considera el dispositivo como amenaza alta.|
|unresponsive|7|El socio de defensa de amenazas móviles considera el dispositivo como sin respuesta. No se conoce el estado del dispositivo.|



