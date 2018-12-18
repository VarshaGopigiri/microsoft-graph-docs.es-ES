---
title: Tipo de recurso iosHomeScreenPage
description: Una página que contiene aplicaciones y carpetas en la pantalla de inicio
author: tfitzmac
ms.openlocfilehash: b8aca5c671d0c8521cdf8a870a2f0ad3cd35ba1b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321465"
---
# <a name="ioshomescreenpage-resource-type"></a>Tipo de recurso iosHomeScreenPage

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una página que contiene aplicaciones y carpetas en la pantalla de inicio
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre de la página|
|iconos|Colección [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)|Una lista de aplicaciones y carpetas que aparecen en una página. Esta colección puede contener un máximo de 500 elementos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenPage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenPage",
  "displayName": "String",
  "icons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenItem",
      "displayName": "String",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "String",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "String",
              "bundleID": "String"
            }
          ]
        }
      ]
    }
  ]
}
```



