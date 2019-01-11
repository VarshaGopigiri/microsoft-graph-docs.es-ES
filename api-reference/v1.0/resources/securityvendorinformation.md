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
# <a name="securityvendorinformation-resource-type"></a><span data-ttu-id="fcc45-103">tipo de recurso securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="fcc45-103">securityVendorInformation resource type</span></span>

<span data-ttu-id="fcc45-104">Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="fcc45-104">Contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span>

## <a name="properties"></a><span data-ttu-id="fcc45-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fcc45-105">Properties</span></span>

| <span data-ttu-id="fcc45-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fcc45-106">Property</span></span>   | <span data-ttu-id="fcc45-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fcc45-107">Type</span></span>|<span data-ttu-id="fcc45-108">Description</span><span class="sxs-lookup"><span data-stu-id="fcc45-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fcc45-109">proveedor</span><span class="sxs-lookup"><span data-stu-id="fcc45-109">provider</span></span> |<span data-ttu-id="fcc45-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="fcc45-110">String</span></span>|<span data-ttu-id="fcc45-111">Proveedor específico (producto o servicio - empresa del proveedor no); Por ejemplo, WindowsDefenderATP.</span><span class="sxs-lookup"><span data-stu-id="fcc45-111">Specific provider (product/service - not vendor company); for example, WindowsDefenderATP.</span></span>|
|<span data-ttu-id="fcc45-112">providerVersion</span><span class="sxs-lookup"><span data-stu-id="fcc45-112">providerVersion</span></span>|<span data-ttu-id="fcc45-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="fcc45-113">String</span></span>|<span data-ttu-id="fcc45-114">Versión del proveedor o subprovider, si existe, que generó la alerta.</span><span class="sxs-lookup"><span data-stu-id="fcc45-114">Version of the provider or subprovider, if it exists, that generated the alert.</span></span> <span data-ttu-id="fcc45-115">*Required*</span><span class="sxs-lookup"><span data-stu-id="fcc45-115">*Required*</span></span>|
|<span data-ttu-id="fcc45-116">subProvider</span><span class="sxs-lookup"><span data-stu-id="fcc45-116">subProvider</span></span>|<span data-ttu-id="fcc45-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="fcc45-117">String</span></span>|<span data-ttu-id="fcc45-118">Subprovider específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="fcc45-118">Specific subprovider (under aggregating provider); for example, WindowsDefenderATP.SmartScreen.</span></span>|
|<span data-ttu-id="fcc45-119">proveedor</span><span class="sxs-lookup"><span data-stu-id="fcc45-119">vendor</span></span> |<span data-ttu-id="fcc45-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="fcc45-120">String</span></span>|<span data-ttu-id="fcc45-121">Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).</span><span class="sxs-lookup"><span data-stu-id="fcc45-121">Name of the alert vendor (for example, Microsoft, Dell, FireEye).</span></span> <span data-ttu-id="fcc45-122">*Required*</span><span class="sxs-lookup"><span data-stu-id="fcc45-122">*Required*</span></span>|


## <a name="json-representation"></a><span data-ttu-id="fcc45-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fcc45-123">JSON representation</span></span>

<span data-ttu-id="fcc45-124">La siguiente es una representación de JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fcc45-124">The folllowing is a JSON representation of the resource.</span></span>
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
