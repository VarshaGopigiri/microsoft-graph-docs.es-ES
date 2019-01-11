---
title: tipo de recurso mobileAppIntentAndState
description: La intención de MobileApp y el estado de instalación para un dispositivo dado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 037faeb02f18f304153dbe19fef640cc1183ddcd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819799"
---
# <a name="mobileappintentandstate-resource-type"></a>tipo de recurso mobileAppIntentAndState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La intención de MobileApp y el estado de instalación para un dispositivo dado.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista mobileAppIntentAndStates](../api/intune-troubleshooting-mobileappintentandstate-list.md)|colección de [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md)|Propiedades de la lista y relaciones de los objetos [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .|
|[Obtener mobileAppIntentAndState](../api/intune-troubleshooting-mobileappintentandstate-get.md)|[mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md)|Leer las propiedades y las relaciones del objeto [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .|
|[Crear mobileAppIntentAndState](../api/intune-troubleshooting-mobileappintentandstate-create.md)|[mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md)|Crear un nuevo objeto [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .|
|[Eliminar mobileAppIntentAndState](../api/intune-troubleshooting-mobileappintentandstate-delete.md)|Ninguno|Elimina un [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md).|
|[Actualizar mobileAppIntentAndState](../api/intune-troubleshooting-mobileappintentandstate-update.md)|[mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md)|Actualizar las propiedades de un objeto [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|UUID para el objeto|
|managedDeviceIdentifier|Cadena|Identificador del dispositivo creado o recopilado por Intune.|
|userId|Cadena|Identificador del usuario que intentó inscribir el dispositivo.|
|mobileAppList|colección de [mobileAppIntentAndStateDetail](../resources/intune-troubleshooting-mobileappintentandstatedetail.md)|La lista de calidades de carga y Estados para el inquilino.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppIntentAndState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppIntentAndState",
  "id": "String (identifier)",
  "managedDeviceIdentifier": "String",
  "userId": "String",
  "mobileAppList": [
    {
      "@odata.type": "microsoft.graph.mobileAppIntentAndStateDetail",
      "applicationId": "String",
      "displayName": "String",
      "mobileAppIntent": "String",
      "displayVersion": "String",
      "installState": "String",
      "supportedDeviceTypes": [
        {
          "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType",
          "type": "String",
          "minimumOperatingSystemVersion": "String",
          "maximumOperatingSystemVersion": "String"
        }
      ]
    }
  ]
}
```





