# <a name="managementagenttype-enum-type"></a>Tipo de enumeración managementAgentType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Tipo de agente de administración.
## <a name="members"></a>Miembros
|Miembros|Valor|Descripción|
|:---|:---|:---|
|eas|1|El dispositivo se administra mediante Exchange server.|
|mdm|2|El dispositivo se administra mediante Intune MDM.|
|easMdm|3|El dispositivo se administra mediante Exchange server e Intune MDM.|
|intuneClient|4|Administrado por el cliente Intune.|
|easIntuneClient|5|El dispositivo está administrado dualmente por el cliente EAS e Intune.|
|configurationManagerClient|8|El dispositivo se administra mediante el Administrador de configuración.|
|configurationManagerClientMdm|10|El dispositivo está administrado por el Administrador de configuración y MDM.|
|configurationManagerClientMdmEas|11|El dispositivo se administra mediante el Administrador de configuración, MDM y Eas.|
|unknown|16|Tipo de agente de administración desconocido.|
|jamf|32|Los atributos del dispositivo se obtienen de Jamf.|
|googleCloudDevicePolicyController|64|El dispositivo se administra mediante CloudDPC de Google.|



