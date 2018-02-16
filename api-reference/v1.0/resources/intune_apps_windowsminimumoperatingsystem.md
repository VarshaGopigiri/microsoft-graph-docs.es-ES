# <a name="windowsminimumoperatingsystem-resource-type"></a>Tipo de recurso windowsMinimumOperatingSystem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El sistema operativo mínimo necesario para una aplicación móvil de Windows.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|v8_0|Booleano|Windows versión 8.0 o posterior.|
|v8_1|Booleano|Windows versión 8.1 o posterior.|
|v10_0|Booleano|Windows versión 10.0 o posterior.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsMinimumOperatingSystem",
  "v8_0": true,
  "v8_1": true,
  "v10_0": true
}
```



