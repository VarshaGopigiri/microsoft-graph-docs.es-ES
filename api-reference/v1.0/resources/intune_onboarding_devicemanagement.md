# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune_onboarding_devicemanagement_get.md)|[deviceManagement](../resources/intune_onboarding_devicemanagement.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_onboarding_devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune_onboarding_devicemanagement_update.md)|[deviceManagement](../resources/intune_onboarding_devicemanagement.md)|Actualice las propiedades de un objeto [deviceManagement](../resources/intune_onboarding_devicemanagement.md).|
|[Función verifyWindowsEnrollmentAutoDiscovery](../api/intune_onboarding_devicemanagement_verifywindowsenrollmentautodiscovery.md)|Booleano|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Todavía no documentado|
|intuneBrand|[intuneBrand](../resources/intune_onboarding_intunebrand.md)|intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceCategories|Colección [deviceCategory](../resources/intune_onboarding_devicecategory.md)|La lista de categorías de dispositivo con el espacio empresarial.|
|exchangeConnectors|Colección [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md)|La lista de conectores de Exchange configurados por el espacio empresarial.|
|deviceEnrollmentConfigurations|Colección [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)|La lista de configuraciones de la inscripción de dispositivos|
|conditionalAccessSettings|[onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|La configuración de acceso condicional local de Exchange. El acceso condicional local requiere que los dispositivos estén inscritos y sean compatibles para tener acceso al correo|
|mobileThreatDefenseConnectors|Colección [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|La lista de conectores de Mobile Threat Defense configurados por el espacio empresarial.|
|deviceManagementPartners|Colección [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md)|La lista de partners de administración de dispositivos configurados por el espacio empresarial.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)",
  "intuneBrand": {
    "@odata.type": "microsoft.graph.intuneBrand",
    "displayName": "String",
    "contactITName": "String",
    "contactITPhoneNumber": "String",
    "contactITEmailAddress": "String",
    "contactITNotes": "String",
    "privacyUrl": "String",
    "onlineSupportSiteUrl": "String",
    "onlineSupportSiteName": "String",
    "themeColor": {
      "@odata.type": "microsoft.graph.rgbColor",
      "r": 1024,
      "g": 1024,
      "b": 1024
    },
    "showLogo": true,
    "lightBackgroundLogo": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "String",
      "value": "binary"
    },
    "darkBackgroundLogo": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "String",
      "value": "binary"
    },
    "showNameNextToLogo": true,
    "showDisplayNameNextToLogo": true
  }
}
```



