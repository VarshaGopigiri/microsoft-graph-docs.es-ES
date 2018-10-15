# <a name="firewallpacketqueueingmethodtype-enum-type"></a>Tipo de enumeración firewallPacketQueueingMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallPacketQueueingMethod
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay ningún valor configurado por Intune, no invalide el valor predeterminado del dispositivo configurado por el usuario|
|disabled|1|Deshabilitar la puesta en cola de paquetes|
|queueInbound|2|Poner en cola los paquetes cifrados entrantes|
|queueOutbound|3|Poner en cola los paquetes salientes descifrados para reenviarlos|
|queueBoth|4|Poner en cola los paquetes entrantes y salientes|








