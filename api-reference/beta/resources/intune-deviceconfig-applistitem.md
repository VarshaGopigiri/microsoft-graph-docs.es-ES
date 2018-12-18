---
title: Tipo de recurso appListItem
description: Representa una aplicación en la lista de aplicaciones administradas
author: tfitzmac
ms.openlocfilehash: 825e88dd5bd32cadfd9a8bfa291ab67036c8180b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343229"
---
# <a name="applistitem-resource-type"></a>Tipo de recurso appListItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa una aplicación en la lista de aplicaciones administradas
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|name|cadena|Nombre de la aplicación|
|publicador|cadena|Publicador de la aplicación|
|appStoreUrl|cadena|Dirección URL de la tienda de la aplicación|
|appId|cadena|El identificador de la aplicación o de la agrupación de la aplicación|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appListItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appListItem",
  "name": "String",
  "publisher": "String",
  "appStoreUrl": "String",
  "appId": "String"
}
```





