# <a name="windowsdeliveryoptimizationmode-enum-type"></a>tipo de enumeración windowsDeliveryOptimizationMode

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Modo de optimización de entrega para la distribución del mismo nivel
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Permitir al usuario que establezca.|
|httpOnly|1|HTTP sólo, sin interconexión|
|httpWithPeeringNat|2|Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red|
|httpWithPeeringPrivateGroup|3|Mezcla de HTTP con interconexión a través de un grupo privado|
|httpWithInternetPeering|4|HTTP mezclado con interconexión de Internet|
|simpleDownload|99|Modo de descarga simple con ningún interconexión|
|bypassMode|100|Modo de derivación. No use la optimización de entrega y usar BITS en su lugar|



