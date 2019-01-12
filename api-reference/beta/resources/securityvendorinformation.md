---
title: tipo de recurso securityVendorInformation
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: preetikr
ms.prod: security
ms.openlocfilehash: 0137abd7a9df0df94f73e18d7efa201008031ff6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939927"
---
# <a name="securityvendorinformation-resource-type"></a>tipo de recurso securityVendorInformation

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
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
