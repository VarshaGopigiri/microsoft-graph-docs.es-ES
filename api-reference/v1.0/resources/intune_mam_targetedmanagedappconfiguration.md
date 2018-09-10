# <a name="targetedmanagedappconfiguration-resource-type"></a>Tipo de recurso targetedManagedAppConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración que se usa para proporcionar un conjunto de ajustes personalizados tal cual para todos los usuarios del grupo de seguridad de destino

Hereda de [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar targetedManagedAppConfigurations](../api/intune_mam_targetedmanagedappconfiguration_list.md)|Colección [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).|
|[Obtener targetedManagedAppConfiguration](../api/intune_mam_targetedmanagedappconfiguration_get.md)|[targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md)|Lea las propiedades y las relaciones del objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).|
|[Crear targetedManagedAppConfiguration](../api/intune_mam_targetedmanagedappconfiguration_create.md)|[targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md)|Cree un objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).|
|[Eliminar targetedManagedAppConfiguration](../api/intune_mam_targetedmanagedappconfiguration_delete.md)|Ninguno|Elimina un [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).|
|[Actualizar targetedManagedAppConfiguration](../api/intune_mam_targetedmanagedappconfiguration_update.md)|[targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md)|Actualice las propiedades de un objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).|
|[Acción assign](../api/intune_mam_targetedmanagedappconfiguration_assign.md)|Ninguna|Todavía no documentado|
|[Acción targetApps](../api/intune_mam_targetedmanagedappconfiguration_targetapps.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|Cadena|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|description|Cadena|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|version|Cadena|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|customSettings|Colección [keyValuePair](../resources/intune_mam_keyvaluepair.md)|Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio. Heredado de [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)|
|deployedAppCount|Int32|Número de aplicaciones en las que se implementará la directiva actual.|
|isAssigned|Booleano|Indica si la directiva se implementará en los grupos de inclusión o no.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|apps|Colección [managedMobileApp](../resources/intune_mam_managedmobileapp.md)|Lista de aplicaciones en las que se implementará la directiva.|
|deploymentSummary|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|Propiedad de navegación para el resumen de implementación de la configuración.|
|asignaciones|Colección [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md)|Propiedad de navegación a la lista de inclusión y exclusión de los grupos en los que se implementará la directiva.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.managedAppConfiguration",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.targetedManagedAppConfiguration"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.targetedManagedAppConfiguration",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ],
  "deployedAppCount": 1024,
  "isAssigned": true
}
```








