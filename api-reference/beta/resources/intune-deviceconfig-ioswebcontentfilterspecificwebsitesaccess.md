---
title: tipo de recurso iosWebContentFilterSpecificWebsitesAccess
description: Representa un tipo de configuración de filtro de contenido Web, que instala marcadores de dirección URL en el explorador integrado de iOS iOS. Un escenario de ejemplo se encuentra en el aula donde los profesores gustaría a los alumnos para navegar por los sitios Web a través de marcadores de explorador configurados en sus dispositivos iOS y no hay acceso a otros sitios.
ms.openlocfilehash: c5e23905ab9e5b692500544161fc052dd606da5d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087439"
---
# <a name="ioswebcontentfilterspecificwebsitesaccess-resource-type"></a>tipo de recurso iosWebContentFilterSpecificWebsitesAccess

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un tipo de configuración de filtro de contenido Web, que instala marcadores de dirección URL en el explorador integrado de iOS iOS. Un escenario de ejemplo se encuentra en el aula donde los profesores gustaría a los alumnos para navegar por los sitios Web a través de marcadores de explorador configurados en sus dispositivos iOS y no hay acceso a otros sitios.

Hereda de [iosWebContentFilterBase](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|specificWebsitesOnly|colección de [iosBookmark](../resources/intune-deviceconfig-iosbookmark.md)|Marcadores de dirección URL que se va a instalar en el explorador integrado y el usuario sólo se permite tener acceso a sitios Web a través de marcadores. Esta colección puede contener un máximo de 500 elementos.|
|websiteList|colección de [iosBookmark](../resources/intune-deviceconfig-iosbookmark.md)|Marcadores de dirección URL que se va a instalar en el explorador integrado y el usuario sólo se permite tener acceso a sitios Web a través de marcadores. Esta colección puede contener un máximo de 500 elementos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosWebContentFilterSpecificWebsitesAccess"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosWebContentFilterSpecificWebsitesAccess",
  "specificWebsitesOnly": [
    {
      "@odata.type": "microsoft.graph.iosBookmark",
      "url": "String",
      "bookmarkFolder": "String",
      "displayName": "String"
    }
  ],
  "websiteList": [
    {
      "@odata.type": "microsoft.graph.iosBookmark",
      "url": "String",
      "bookmarkFolder": "String",
      "displayName": "String"
    }
  ]
}
```





