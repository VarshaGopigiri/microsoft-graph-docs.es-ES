---
title: tipo de recurso vppTokenLicenseSummary
description: Resumen de la licencia de una aplicación determinada en un símbolo (token).
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e5972341aa3b390ae226d19f7d85fe918345c627
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824867"
---
# <a name="vpptokenlicensesummary-resource-type"></a>tipo de recurso vppTokenLicenseSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resumen de la licencia de una aplicación determinada en un símbolo (token).
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|vppTokenId|Cadena|Identificador del token VPP.|
|Id. de Apple|Cadena|Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.|
|organizationName|Cadena|La organización asociada con el Token de programa de compra de Apple por volumen.|
|availableLicenseCount|Int32|El número de licencias VPP disponibles.|
|usedLicenseCount|Int32|Número de licencias VPP en uso.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppTokenLicenseSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppTokenLicenseSummary",
  "vppTokenId": "String",
  "appleId": "String",
  "organizationName": "String",
  "availableLicenseCount": 1024,
  "usedLicenseCount": 1024
}
```





