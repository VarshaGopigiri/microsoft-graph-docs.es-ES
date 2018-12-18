---
title: tipo de recurso windowsKioskMultipleApps
description: La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco
author: tfitzmac
ms.openlocfilehash: 30591e15d29b06ffb807c8b435d0e3c8a6a1b0fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330145"
---
# <a name="windowskioskmultipleapps-resource-type"></a>tipo de recurso windowsKioskMultipleApps

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco

Hereda de [windowsKioskAppConfiguration](../resources/intune-deviceconfig-windowskioskappconfiguration.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|aplicaciones|colección de [windowsKioskAppBase](../resources/intune-deviceconfig-windowskioskappbase.md)|Estos son el único almacén de aplicaciones de Windows que estará disponible para iniciar desde el menú Inicio.|
|showTaskBar|Boolean|Esta opción le permite al administrador especificar si se muestra la barra de tareas o no.|
|disallowDesktopApps|Boolean|Esta opción indica que se permiten aplicaciones de escritorio. De forma predeterminada en true.|
|startMenuLayoutXml|Binario|Permite a los administradores invalidar el diseño de inicio predeterminado y se evita que el usuario que lo modifique.Para modificar el diseño, se especifica un archivo XML basado en el esquema de modificación del diseño. XML debe estar en formato binario.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskMultipleApps"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskMultipleApps",
  "apps": [
    {
      "@odata.type": "microsoft.graph.windowsKioskUWPApp",
      "startLayoutTileSize": "String",
      "name": "String",
      "appUserModelId": "String",
      "appId": "String",
      "containedAppId": "String"
    }
  ],
  "showTaskBar": true,
  "disallowDesktopApps": true,
  "startMenuLayoutXml": "binary"
}
```





