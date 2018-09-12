# <a name="devicemanagementexchangeaccessstatereason-enum-type"></a>Tipo de enumeración deviceManagementExchangeAccessStateReason

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Motivo del estado de acceso del dispositivo a Exchange.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|none|0|No hay ningún motivo de estado de acceso detectado desde Exchange|
|unknown|1|Motivo del estado de acceso desconocido|
|exchangeGlobalRule|2|Estado de acceso determinado por la regla Exchange Global|
|exchangeIndividualRule|3|Estado de acceso determinado por la regla Exchange Individual|
|exchangeDeviceRule|4|Estado de acceso determinado por la regla Exchange Device|
|exchangeUpgrade|5|Estado de acceso debido a la actualización de Exchange|
|exchangeMailboxPolicy|6|Estado de acceso determinado por una directiva de Exchange Mailbox|
|other|7|Estado de acceso determinado por Exchange|
|compliant|8|Estado de acceso concedido por desafío de cumplimiento normativo|
|notCompliant|9|Estado de acceso revocado por desafío de cumplimiento normativo|
|notEnrolled|10|Estado de acceso revocado por desafío de administración|
|unknownLocation|12|Estado de acceso debido a ubicación desconocida|
|mfaRequired|13|Estado de acceso debido a desafío MFA|
|azureADBlockDueToAccessPolicy|14|Estado de acceso revocado por una directiva de acceso AAD|
|compromisedPassword|15|Estado de acceso revocado por contraseña en peligro|
|deviceNotKnownWithManagedApp|16|Estado de acceso revocado por desafío de aplicación administrada|








