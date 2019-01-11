---
title: tipo de recurso userAppInstallStatus
description: Contiene las propiedades para el estado de instalación para un usuario.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f4d848a4fe4cd742df8a83184d539d7ff27290b0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885207"
---
# <a name="userappinstallstatus-resource-type"></a>tipo de recurso userAppInstallStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para el estado de instalación para un usuario.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista userAppInstallStatuses](../api/intune-apps-userappinstallstatus-list.md)|colección de [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|Propiedades de la lista y relaciones de los objetos [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .|
|[Obtener userAppInstallStatus](../api/intune-apps-userappinstallstatus-get.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|Leer las propiedades y las relaciones del objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .|
|[Crear userAppInstallStatus](../api/intune-apps-userappinstallstatus-create.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|Crear un nuevo objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .|
|[Eliminar userAppInstallStatus](../api/intune-apps-userappinstallstatus-delete.md)|Ninguno|Elimina un [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md).|
|[Actualizar userAppInstallStatus](../api/intune-apps-userappinstallstatus-update.md)|[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)|Actualizar las propiedades de un objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|userName|String|Nombre de usuario.|
|userPrincipalName|Cadena|Nombre Principal de usuario.|
|installedDeviceCount|Int32|Número de dispositivos instalados.|
|failedDeviceCount|Int32|Número de dispositivos erróneos.|
|notInstalledDeviceCount|Int32|Número de dispositivos no instalados.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|aplicación|[mobileApp](../resources/intune-apps-mobileapp.md)|El vínculo de navegación a la aplicación móvil.|
|deviceStatuses|colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)|El estado de instalación de la aplicación en los dispositivos.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userAppInstallStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userAppInstallStatus",
  "id": "String (identifier)",
  "userName": "String",
  "userPrincipalName": "String",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024
}
```





