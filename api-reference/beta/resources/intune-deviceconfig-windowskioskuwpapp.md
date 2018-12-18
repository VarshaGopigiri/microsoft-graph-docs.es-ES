---
title: tipo de recurso windowsKioskUWPApp
description: La clase base para un tipo de aplicaciones
author: tfitzmac
ms.openlocfilehash: 328a91065692a7b315ade5dae86c15d6def320eb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305183"
---
# <a name="windowskioskuwpapp-resource-type"></a>tipo de recurso windowsKioskUWPApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase base para un tipo de aplicaciones

Hereda de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|startLayoutTileSize|[windowsAppStartLayoutTileSize](../resources/intune-deviceconfig-windowsappstartlayouttilesize.md)|El tamaño del mosaico de aplicación para el diseño de inicio Inherited desde [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md). Los valores posibles son: `hidden`, `small`, `medium`, `wide` y `large`.|
|name|String|Representa el nombre descriptivo de una aplicación heredada de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)|
|appUserModelId|String|Esta es la única aplicación de usuario modelo de identificador (AUMID) que estará disponible para iniciar el uso en el modo de pantalla completa|
|appId|cadena|Esto hace referencia a un App Intune que será destino para las mismas asignaciones de configuración de quiosco|
|containedAppId|String|Esto hace referencia a una aplicación contenida desde un App Intune|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskUWPApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskUWPApp",
  "startLayoutTileSize": "String",
  "name": "String",
  "appUserModelId": "String",
  "appId": "String",
  "containedAppId": "String"
}
```





