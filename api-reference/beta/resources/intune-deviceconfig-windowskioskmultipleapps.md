---
title: tipo de recurso windowsKioskMultipleApps
description: La clase que se usa para identificar la configuración de la aplicación de varios modos para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 01758c66a466b66fcba6b443f80d0350d308756d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851208"
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
|showTaskBar|Booleano|Esta opción le permite al administrador especificar si se muestra la barra de tareas o no.|
|disallowDesktopApps|Booleano|Esta opción indica que se permiten aplicaciones de escritorio. De forma predeterminada en true.|
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





