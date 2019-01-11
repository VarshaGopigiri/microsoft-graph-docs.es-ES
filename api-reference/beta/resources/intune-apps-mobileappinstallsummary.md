---
title: tipo de recurso mobileAppInstallSummary
description: Contiene las propiedades para el resumen de la instalación de una aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3b730f73b8a86c8acba531ab0d30a67b2f8e7a7f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820359"
---
# <a name="mobileappinstallsummary-resource-type"></a>tipo de recurso mobileAppInstallSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para el resumen de la instalación de una aplicación móvil.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener mobileAppInstallSummary](../api/intune-apps-mobileappinstallsummary-get.md)|[mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md)|Leer las propiedades y las relaciones del objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .|
|[Actualizar mobileAppInstallSummary](../api/intune-apps-mobileappinstallsummary-update.md)|[mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md)|Actualizar las propiedades de un objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|installedDeviceCount|Int32|Número de dispositivos que haya instalado correctamente esta aplicación.|
|failedDeviceCount|Int32|Número de dispositivos que no haya podido instalar esta aplicación.|
|notApplicableDeviceCount|Int32|Número de dispositivos que no son aplicables para esta aplicación.|
|notInstalledDeviceCount|Int32|Número de dispositivos que no tienen esta aplicación instalada.|
|pendingInstallDeviceCount|Int32|Número de dispositivos que hayan sido notificados para instalar esta aplicación.|
|installedUserCount|Int32|Número de usuarios cuyos dispositivos han correctas para instalar esta aplicación.|
|failedUserCount|Int32|Número de usuarios que tienen 1 o más dispositivos que no se pudo instalar esta aplicación.|
|notApplicableUserCount|Int32|Número de usuarios cuyos dispositivos no eran aplicables para esta aplicación.|
|notInstalledUserCount|Int32|Número de usuarios que tienen 1 o más dispositivos que no se han instalado esta aplicación.|
|pendingInstallUserCount|Int32|Número de usuarios que tienen 1 o más dispositivos que han sido notificados a instalar esta aplicación y de tener 0 dispositivos con errores.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppInstallSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppInstallSummary",
  "id": "String (identifier)",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "notInstalledDeviceCount": 1024,
  "pendingInstallDeviceCount": 1024,
  "installedUserCount": 1024,
  "failedUserCount": 1024,
  "notApplicableUserCount": 1024,
  "notInstalledUserCount": 1024,
  "pendingInstallUserCount": 1024
}
```





