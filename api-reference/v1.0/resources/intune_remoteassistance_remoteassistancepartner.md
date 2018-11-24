# <a name="remoteassistancepartner-resource-type"></a>Tipo de recurso remoteAssistancePartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Los recursos remoteAssistPartner representan los metadatos y el estado de un servicio de partner de asistencia remota específico.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar remoteAssistancePartners](../api/intune_remoteassistance_remoteassistancepartner_list.md)|Colección [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md)|Enumere las propiedades y las relaciones de los objetos [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).|
|[Obtener remoteAssistancePartner](../api/intune_remoteassistance_remoteassistancepartner_get.md)|[remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md)|Lea las propiedades y las relaciones del objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).|
|[Crear remoteAssistancePartner](../api/intune_remoteassistance_remoteassistancepartner_create.md)|[remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md)|Cree un objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).|
|[Eliminar remoteAssistancePartner](../api/intune_remoteassistance_remoteassistancepartner_delete.md)|Ninguna|Elimina un [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).|
|[Actualizar remoteAssistancePartner](../api/intune_remoteassistance_remoteassistancepartner_update.md)|[remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md)|Actualice las propiedades de un objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).|
|[Acción beginOnboarding](../api/intune_remoteassistance_remoteassistancepartner_beginonboarding.md)|Ninguna|Todavía no documentado|
|[Acción disconnect](../api/intune_remoteassistance_remoteassistancepartner_disconnect.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Identificador único del partner.|
|displayName|cadena|Nombre para mostrar del partner.|
|onboardingUrl|cadena|Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.|
|onboardingStatus|[remoteAssistanceOnboardingStatus](../resources/intune_remoteassistance_remoteassistanceonboardingstatus.md)|TBD. Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.|
|lastConnectionDateTime|DateTimeOffset|Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.remoteAssistancePartner"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "id": "String (identifier)",
  "displayName": "String",
  "onboardingUrl": "String",
  "onboardingStatus": "String",
  "lastConnectionDateTime": "String (timestamp)"
}
```



