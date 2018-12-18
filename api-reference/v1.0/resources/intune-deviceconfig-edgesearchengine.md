---
title: Tipo de recurso edgeSearchEngine
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.
author: tfitzmac
ms.openlocfilehash: 0c49780ddd7d2174116f7a0821fa98681d3e5d2a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339735"
---
# <a name="edgesearchengine-resource-type"></a>Tipo de recurso edgeSearchEngine

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.

Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|edgeSearchEngineType|[edgeSearchEngineType](../resources/intune-deviceconfig-edgesearchenginetype.md)|Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM. Los valores posibles son: `default` y `bing`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.edgeSearchEngine"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngine",
  "edgeSearchEngineType": "String"
}
```



