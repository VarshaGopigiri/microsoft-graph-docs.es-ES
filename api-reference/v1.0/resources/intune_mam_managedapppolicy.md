# <a name="managedapppolicy-resource-type"></a>Tipo de recurso managedAppPolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppPolicies](../api/intune_mam_managedapppolicy_list.md)|Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|[Obtener managedAppPolicy](../api/intune_mam_managedapppolicy_get.md)|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|[Acción targetApps](../api/intune_mam_managedapppolicy_targetapps.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar de la directiva.|
|descripción|cadena|La descripción de la directiva.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la directiva.|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva.|
|id|cadena|Clave de la entidad.|
|versión|cadena|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicy",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String"
}
```



