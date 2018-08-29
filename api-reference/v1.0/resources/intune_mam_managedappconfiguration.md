# <a name="managedappconfiguration-resource-type"></a>Tipo de recurso managedAppConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.

Hereda de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppConfigurations](../api/intune_mam_managedappconfiguration_list.md)|Colección [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md).|
|[Obtener managedAppConfiguration](../api/intune_mam_managedappconfiguration_get.md)|[managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)|Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|Nombre para mostrar de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|descripción|String|Descripción de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Última vez que se modificó la directiva. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|id|Cadena|Clave de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|version|String|Versión de la entidad. Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).|
|customSettings|Colección [keyValuePair](../resources/intune_mam_keyvaluepair.md)|Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.managedAppPolicy",
  "@odata.type": "microsoft.graph.managedAppConfiguration"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppConfiguration",
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
  ]
}
```



