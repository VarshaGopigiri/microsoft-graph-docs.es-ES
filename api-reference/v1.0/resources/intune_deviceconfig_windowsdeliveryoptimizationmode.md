# <a name="windowsdeliveryoptimizationmode-enum-type"></a>tipo de enumeración windowsDeliveryOptimizationMode

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Modo de optimización de entrega para la distribución de mismo nivel
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Permite que el usuario lo establezca.|
|httpOnly|1|solo HTTP, sin emparejamientos|
|httpWithPeeringNat|2|Predeterminado del sistema operativo: HTTP combinado con el emparejamiento que se encuentra en el mismo traductor de direcciones de red|
|httpWithPeeringPrivateGroup|3|HTTP combinado con el emparejamiento a través de un grupo privado|
|httpWithInternetPeering|4|HTTP combinado con el emparejamiento de Internet|
|simpleDownload|99|Modo de descarga simple sin ningún emparejamiento|
|bypassMode|100|Modo bypass. No utiliza la Optimización de entrega y emplea BITS en su lugar|



