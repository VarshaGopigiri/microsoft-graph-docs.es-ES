# <a name="compliancestate-enum-type"></a>Tipo de enumeración complianceState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de cumplimiento.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|unknown|0|Desconocido.|
|compliant|1|Compatible.|
|nonCompliant|2|El dispositivo no es compatible y está bloqueado para acceder a los recursos corporativos.|
|conflict|3|Conflicto con otras reglas.|
|error|4|Error.|
|inGracePeriod|254|El dispositivo no es compatible pero tiene acceso a recursos corporativos.|
|configManager|255|Administrado por el administrador de configuraciones.|



