---
title: Tipo de recurso iosHomeScreenPage
description: Una página que contiene aplicaciones y carpetas en la pantalla de inicio
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a59c910f37a82e04a7ccd5050a0a03999ac567b7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961039"
---
# <a name="ioshomescreenpage-resource-type"></a>Tipo de recurso iosHomeScreenPage

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
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





