# <a name="diagnosticdatasubmissionmode-enum-type"></a>Tipo de enumeración diagnosticDataSubmissionMode

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Permitir que el dispositivo envíe datos de telemetría de diagnóstico y de uso, como Watson.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|userDefined|0|Permite que el usuario lo establezca.|
|none|1|No se envían datos de telemetría desde los componentes del sistema operativo. Nota: Este valor solo es aplicable a dispositivos de servidor y de empresa. El uso de esta configuración en otros dispositivos equivale a establecer el valor de 1.|
|basic|2|Envía datos de telemetría básicos.|
|enhanced|3|Envía datos de telemetría mejorados, incluidos los datos de uso y conocimiento.|
|full|4|Envía datos de telemetría completos, incluidos los datos de diagnósticos, como el estado del sistema.|








