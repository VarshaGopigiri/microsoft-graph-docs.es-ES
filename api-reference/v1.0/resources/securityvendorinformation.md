---
title: tipo de recurso securityVendorInformation
description: " subProvider = AppLocker)."
localization_priority: Normal
ms.openlocfilehash: e9d8551c085c05007388bf0c6e33143994c6969b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820149"
---
# <a name="securityvendorinformation-resource-type"></a>tipo de recurso securityVendorInformation

Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Description|
|:---------------|:--------|:----------|
|proveedor |Cadena|Proveedor específico (producto o servicio - empresa del proveedor no); Por ejemplo, WindowsDefenderATP.|
|providerVersion|Cadena|Versión del proveedor o subprovider, si existe, que generó la alerta. *Required*|
|subProvider|Cadena|Subprovider específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.|
|proveedor |Cadena|Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye). *Required*|


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación de JSON del recurso.
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.securityVendorInformation"
}-->

```json
{
  "provider": "String",
  "providerVersion": "String",
  "subProvider": "String",
  "vendor": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "securityVendorInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
