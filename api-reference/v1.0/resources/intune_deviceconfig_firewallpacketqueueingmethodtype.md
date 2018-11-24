# <a name="firewallpacketqueueingmethodtype-enum-type"></a>tipo de enumeración firewallPacketQueueingMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallPacketQueueingMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|deshabilitado|1|Deshabilitar la puesta en cola de paquetes|
|queueInbound|2|Poner en cola los paquetes cifrados entrantes|
|queueOutbound|3|Cola descifra los paquetes salientes para desvío de llamadas|
|queueBoth|4|Paquetes entrantes y salientes en cola|



