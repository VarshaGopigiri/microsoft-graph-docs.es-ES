---
title: Tipo de recurso edgeSearchEngineCustom
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.
author: tfitzmac
ms.openlocfilehash: f648f41bafcbaa37c972500139ecc8d3e70113ca
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357977"
---
# <a name="edgesearchenginecustom-resource-type"></a>Tipo de recurso edgeSearchEngineCustom

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.

Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|edgeSearchEngineOpenSearchXmlUrl|cadena|Apunta a un vínculo HTTPS que contiene el archivo XML OpenSearch, que incluye, como mínimo, el nombre corto y la dirección URL del motor de búsqueda.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.edgeSearchEngineCustom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngineCustom",
  "edgeSearchEngineOpenSearchXmlUrl": "String"
}
```



