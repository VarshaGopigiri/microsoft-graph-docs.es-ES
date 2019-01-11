---
title: Tipo de recurso detectedApp
description: Una aplicación administrada o no administrada que está instalada en un dispositivo administrado. Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8b28965cb506075c8caf7d983ddf41eafcdda78d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881427"
---
# <a name="detectedapp-resource-type"></a>Tipo de recurso detectedApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una aplicación administrada o no administrada que está instalada en un dispositivo administrado. Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar detectedApps](../api/intune-devices-detectedapp-list.md)|Colección [detectedApp](../resources/intune-devices-detectedapp.md)|Enumere las propiedades y las relaciones de los objetos [detectedApp](../resources/intune-devices-detectedapp.md).|
|[Obtener detectedApp](../api/intune-devices-detectedapp-get.md)|[detectedApp](../resources/intune-devices-detectedapp.md)|Lea las propiedades y las relaciones del objeto [detectedApp](../resources/intune-devices-detectedapp.md).|
|[Crear detectedApp](../api/intune-devices-detectedapp-create.md)|[detectedApp](../resources/intune-devices-detectedapp.md)|Cree un objeto [detectedApp](../resources/intune-devices-detectedapp.md).|
|[Eliminar detectedApp](../api/intune-devices-detectedapp-delete.md)|Ninguna|Elimina un [detectedApp](../resources/intune-devices-detectedapp.md).|
|[Actualizar detectedApp](../api/intune-devices-detectedapp-update.md)|[detectedApp](../resources/intune-devices-detectedapp.md)|Actualice las propiedades de un objeto [detectedApp](../resources/intune-devices-detectedapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El identificador único de la aplicación detectada. Intune lo genera automáticamente en el momento en que se crea la aplicación. Solo lectura.|
|displayName|Cadena|Nombre de la aplicación detectada. Solo lectura|
|version|Cadena|Versión de la aplicación detectada. Solo lectura|
|sizeInByte|Int64|Tamaño en bytes de la aplicación detectada. Solo lectura|
|deviceCount|Int32|El número de dispositivos que han instalado esta aplicación.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managedDevices|Colección [managedDevice](../resources/intune-devices-manageddevice.md)|Los dispositivos que tienen instalada la aplicación detectada|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.detectedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.detectedApp",
  "id": "String (identifier)",
  "displayName": "String",
  "version": "String",
  "sizeInByte": 1024,
  "deviceCount": 1024
}
```



