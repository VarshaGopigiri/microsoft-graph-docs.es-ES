# <a name="manageddevicepartnerreportedhealthstate-enum-type"></a>Tipo de enumeración managedDevicePartnerReportedHealthState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de mantenimiento disponibles para la API de estado de dispositivo
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|El estado de mantenimiento del dispositivo no se ha notificado|
|activado|1|El dispositivo ha sido activado por un socio de defensa de amenazas móviles, pero aún no ha notificado el estado.|
|desactivado|2|El dispositivo ha sido desactivado por un socio de defensa de amenazas móviles. No se conoce el estado del dispositivo.|
|asegurado|3|El socio de defensa de amenazas móviles considera el dispositivo como seguro.|
|lowSeverity|4|El socio de defensa de amenazas móviles considera el dispositivo como amenaza baja.|
|mediumSeverity|5|El socio de defensa de amenazas móviles considera el dispositivo como amenaza media.|
|highSeverity|6|El socio de defensa de amenazas móviles considera el dispositivo como amenaza alta.|
|sin respuesta|7|El socio de defensa de amenazas móviles considera el dispositivo como sin respuesta. No se conoce el estado del dispositivo.|
|comprometido|8|El dispositivo se considera comprometido por el socio de defensa de amenazas. Esto significa que el dispositivo es una amenaza o un riesgo activo que no se puede corregir fácilmente por el usuario final y el usuario debería ponerse en contacto con su administrador de TI.|
|configuración errónea|9|El dispositivo se considera mal configurado por el socio de defensa de amenazas. Esto significa que al dispositivo le falta un perfil requerido o una configuración para que el socio de defensa de amenazas funcione correctamente y, por lo tanto, el análisis de riesgos o amenazas  no se puede completar.|








