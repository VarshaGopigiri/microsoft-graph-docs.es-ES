# <a name="defenderthreataction-enum-type"></a>tipo de enumeración defenderThreatAction

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción predeterminada de Defender para realizar ante las amenazas detectadas de malware.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|Aplicar la acción en función de la definición de actualización.|
|clean|1|Limpiar la amenaza detectada.|
|quarantine|2|Poner en cuarentena la amenaza detectada.|
|remove|3|Quitar la amenaza detectada.|
|allow|4|Permitir la amenaza detectada.|
|userDefined|5|Permitir que el usuario determine la acción que se realizará con la amenaza detectada.|
|block|6|Bloquear la amenaza detectada.|



