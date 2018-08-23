# <a name="deviceregistrationstate-enum-type"></a>Tipo de enumeración deviceRegistrationState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de registro de dispositivo.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|notRegistered|0|El dispositivo no está registrado.|
|registered|2|El dispositivo está registrado.|
|revoked|3|El dispositivo se ha bloqueado, borrado o retirado.|
|keyConflict|4|El dispositivo tiene un conflicto con la clave.|
|approvalPending|5|El dispositivo está pendiente de aprobación.|
|certificateReset|6|El certificado del dispositivo se ha restablecido.|
|notRegisteredPendingEnrollment|7|El dispositivo no está registrado y está pendiente de inscripción.|
|unknown|8|El estado de registro del dispositivo es desconocido.|



