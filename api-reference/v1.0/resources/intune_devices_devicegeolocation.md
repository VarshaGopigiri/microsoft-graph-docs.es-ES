# <a name="devicegeolocation-resource-type"></a>Tipo de recurso deviceGeoLocation

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Ubicación del dispositivo
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|lastCollectedDateTime|DateTimeOffset|Hora en la que se registró la ubicación, con respecto a UTC|
|longitude|Doble|Coordenadas de longitud de la ubicación del dispositivo|
|latitude|Doble|Coordenadas de latitud de la ubicación del dispositivo|
|altitude|Doble|Altitud, en metros por encima del nivel del mar|
|horizontalAccuracy|Doble|Precisión de longitud y latitud en metros|
|verticalAccuracy|Doble|Precisión de altitud en metros|
|rumbo|Doble|Rumbo en grados desde el norte geográfico|
|velocidad|Doble|La velocidad a la que se desplaza el dispositivo en metros por segundo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceGeoLocation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceGeoLocation",
  "lastCollectedDateTime": "String (timestamp)",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "altitude": "<Unknown Primitive Type Edm.Double>",
  "horizontalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "verticalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "heading": "<Unknown Primitive Type Edm.Double>",
  "speed": "<Unknown Primitive Type Edm.Double>"
}
```



