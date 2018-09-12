# <a name="deviceenrollmentfailurereason-enum-type"></a>Tipo de enumeración deviceEnrollmentFailureReason

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Categorías de fallos de nivel superior para la inscripción.

## <a name="members"></a>Miembros

|Miembro|Valor|Descripción|
|:---|:---|:---|
|unknown|0|Valor predeterminado, se desconoce la razón de este fallo.|
|authentication|1|Error de autenticación|
|authorization|2|La llamada se ha autenticado, pero no se ha autorizado para la inscripción.|
|accountValidation|3|Error al validar la cuenta para la inscripción. (Cuenta bloqueada, inscripción no habilitada)|
|userValidation|4|No se pudo validar el usuario. (El usuario no existe, falta la licencia)|
|deviceNotSupported|5|El dispositivo no es compatible con la administración de dispositivos móviles.|
|inMaintenance|6|La cuenta está en mantenimiento.|
|badRequest|7|El cliente envió una solicitud que el servicio no entiende o que es incompatible con él.|
|featureNotSupported|8|La(s) característica(s) utilizada(s) por esta inscripción no son compatibles con esta cuenta.|
|enrollmentRestrictionsEnforced|9|Esta inscripción fue bloqueada por restricciones de inscripción configuradas por el administrador.|
|clientDisconnected|10|El cliente agotó el tiempo de espera o el usuario final anuló la inscripción.|
|userAbandonment|11|El usuario final abandonó la inscripción. (El usuario final inició la incorporación pero no se pudo completar a tiempo)|


<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: Enum deviceEnrollmentFailureReason has some values specified and others unspecified."
  ],
}
-->


