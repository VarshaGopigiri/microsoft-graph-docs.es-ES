---
title: tipo de recurso securityVendorInformation
description: " subProvider = AppLocker)."
ms.openlocfilehash: 0eef5b1d53f4b7b61af0ccede6e02ffc7bdf76ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031523"
---
# <a name="securityvendorinformation-resource-type"></a><span data-ttu-id="75758-103">tipo de recurso securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="75758-103">securityVendorInformation resource type</span></span>

<span data-ttu-id="75758-104">Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="75758-104">Contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span>

## <a name="properties"></a><span data-ttu-id="75758-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75758-105">Properties</span></span>

| <span data-ttu-id="75758-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75758-106">Property</span></span>   | <span data-ttu-id="75758-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="75758-107">Type</span></span>|<span data-ttu-id="75758-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="75758-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="75758-109">proveedor</span><span class="sxs-lookup"><span data-stu-id="75758-109">provider</span></span> |<span data-ttu-id="75758-110">String</span><span class="sxs-lookup"><span data-stu-id="75758-110">String</span></span>|<span data-ttu-id="75758-111">Proveedor específico (producto o servicio - empresa del proveedor no); Por ejemplo, WindowsDefenderATP.</span><span class="sxs-lookup"><span data-stu-id="75758-111">Specific provider (product/service - not vendor company); for example, WindowsDefenderATP.</span></span>|
|<span data-ttu-id="75758-112">providerVersion</span><span class="sxs-lookup"><span data-stu-id="75758-112">providerVersion</span></span>|<span data-ttu-id="75758-113">String</span><span class="sxs-lookup"><span data-stu-id="75758-113">String</span></span>|<span data-ttu-id="75758-114">Versión del proveedor o subprovider, si existe, que generó la alerta.</span><span class="sxs-lookup"><span data-stu-id="75758-114">Version of the provider or subprovider, if it exists, that generated the alert.</span></span> <span data-ttu-id="75758-115">*Required*</span><span class="sxs-lookup"><span data-stu-id="75758-115">*Required*</span></span>|
|<span data-ttu-id="75758-116">subProvider</span><span class="sxs-lookup"><span data-stu-id="75758-116">subProvider</span></span>|<span data-ttu-id="75758-117">String</span><span class="sxs-lookup"><span data-stu-id="75758-117">String</span></span>|<span data-ttu-id="75758-118">Subprovider específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="75758-118">Specific subprovider (under aggregating provider); for example, WindowsDefenderATP.SmartScreen.</span></span>|
|<span data-ttu-id="75758-119">proveedor</span><span class="sxs-lookup"><span data-stu-id="75758-119">vendor</span></span> |<span data-ttu-id="75758-120">String</span><span class="sxs-lookup"><span data-stu-id="75758-120">String</span></span>|<span data-ttu-id="75758-121">Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).</span><span class="sxs-lookup"><span data-stu-id="75758-121">Name of the alert vendor (for example, Microsoft, Dell, FireEye).</span></span> <span data-ttu-id="75758-122">*Required*</span><span class="sxs-lookup"><span data-stu-id="75758-122">*Required*</span></span>|


## <a name="json-representation"></a><span data-ttu-id="75758-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75758-123">JSON representation</span></span>

<span data-ttu-id="75758-124">La siguiente es una representación de JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75758-124">The folllowing is a JSON representation of the resource.</span></span>
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
