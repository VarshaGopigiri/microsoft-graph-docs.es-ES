# <a name="managedapppolicydeploymentsummary-resource-type"></a>Tipo de recurso managedAppPolicyDeploymentSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener managedAppPolicyDeploymentSummary](../api/intune_mam_managedapppolicydeploymentsummary_get.md)|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|Lea las propiedades y las relaciones del objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).|
|[Actualizar managedAppPolicyDeploymentSummary](../api/intune_mam_managedapppolicydeploymentsummary_update.md)|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|Actualice las propiedades de un objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|Todavía no documentado|
|configurationDeployedUserCount|Int32|Todavía no documentado|
|lastRefreshTime|DateTimeOffset|Todavía no documentado|
|configurationDeploymentSummaryPerApp|Colección [managedAppPolicyDeploymentSummaryPerApp](../resources/intune_mam_managedapppolicydeploymentsummaryperapp.md)|Todavía no documentado|
|id|Cadena|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummary",
  "displayName": "String",
  "configurationDeployedUserCount": 1024,
  "lastRefreshTime": "String (timestamp)",
  "configurationDeploymentSummaryPerApp": [
    {
      "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "String"
      },
      "configurationAppliedUserCount": 1024
    }
  ],
  "id": "String (identifier)",
  "version": "String"
}
```



