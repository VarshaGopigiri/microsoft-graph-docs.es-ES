---
title: tipo de recurso windowsKioskDesktopApp
description: La clase base para un tipo de aplicaciones
ms.openlocfilehash: 8b3a3cd8bfc7c35fa2a730c85adafc3ae6dceba2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085480"
---
# <a name="windowskioskdesktopapp-resource-type"></a>tipo de recurso windowsKioskDesktopApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase base para un tipo de aplicaciones

Hereda de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|startLayoutTileSize|[windowsAppStartLayoutTileSize](../resources/intune-deviceconfig-windowsappstartlayouttilesize.md)|El tamaño del mosaico de aplicación para el diseño de inicio Inherited desde [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md). Los valores posibles son: `hidden`, `small`, `medium`, `wide` y `large`.|
|name|String|Representa el nombre descriptivo de una aplicación heredada de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)|
|ruta de acceso|String|Definir la ruta de acceso de una aplicación de escritorio|
|desktopApplicationId|String|Definir la DesktopApplicationID de la aplicación|
|desktopApplicationLinkPath|String|Definir la DesktopApplicationLinkPath de la aplicación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskDesktopApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskDesktopApp",
  "startLayoutTileSize": "String",
  "name": "String",
  "path": "String",
  "desktopApplicationId": "String",
  "desktopApplicationLinkPath": "String"
}
```





