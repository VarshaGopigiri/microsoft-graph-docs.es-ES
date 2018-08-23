# <a name="devicethreatprotectionlevel-enum-type"></a>tipo de enumeración deviceThreatProtectionLevel

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Niveles de protección contra amenazas de dispositivo de la API de protección contra amenazas de dispositivo.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|unavailable|0|Valor predeterminado. No usar.|
|secured|1|Requisito de nivel de amenaza de dispositivo: protegido. Este es el nivel más seguro y representa que no se encontraron amenazas en el dispositivo.|
|low|2|Requisito de nivel de protección contra amenazas de dispositivo: baja. Baja indica una gravedad de amenaza que representa un riesgo mínimo para el dispositivo o los datos que contiene.|
|medium|3|Requisito de nivel de protección contra amenazas de dispositivo: media. Media indica una gravedad de amenaza que representa un riesgo moderado para el dispositivo o los datos que contiene.|
|high|4|Requisito de nivel de protección contra amenazas de dispositivo: alta. Alta indica una gravedad de amenaza que representa un riesgo grave para el dispositivo o los datos que contiene.|
|notSet|10|Requisito de nivel de protección contra amenazas de dispositivo: no establecido. No establecido indica que no hay ningún requisito de que el dispositivo cumpla un nivel de protección contra amenazas.|



