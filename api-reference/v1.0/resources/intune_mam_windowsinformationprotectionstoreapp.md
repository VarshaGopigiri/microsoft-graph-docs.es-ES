# <a name="windowsinformationprotectionstoreapp-resource-type"></a>Tipo de recurso windowsInformationProtectionStoreApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Aplicación de la tienda de Windows Information Protection

Hereda de [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar de la aplicación. Heredado de [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|
|descripción|cadena|La descripción de la aplicación. Heredado de [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|
|publisherName|cadena|Nombre del publicador. Heredado de [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|
|productName|cadena|El nombre del producto. Heredado de [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|
|denegado|Booleano|Si es true, se deniega la protección o la exención a la aplicación. Heredado de [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionStoreApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true
}
```



