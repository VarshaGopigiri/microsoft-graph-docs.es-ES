---
title: tipo de recurso securityVendorInformation
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 34e565a69f716f0d167240ab753e5d192758508a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884388"
---
# <a name="securityvendorinformation-resource-type"></a><span data-ttu-id="e5c38-104">tipo de recurso securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="e5c38-104">securityVendorInformation resource type</span></span>

 > <span data-ttu-id="e5c38-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5c38-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5c38-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5c38-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5c38-107">Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="e5c38-107">Contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span>

## <a name="properties"></a><span data-ttu-id="e5c38-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5c38-108">Properties</span></span>

| <span data-ttu-id="e5c38-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5c38-109">Property</span></span>   | <span data-ttu-id="e5c38-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5c38-110">Type</span></span>|<span data-ttu-id="e5c38-111">Description</span><span class="sxs-lookup"><span data-stu-id="e5c38-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e5c38-112">proveedor</span><span class="sxs-lookup"><span data-stu-id="e5c38-112">provider</span></span> |<span data-ttu-id="e5c38-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5c38-113">String</span></span>|<span data-ttu-id="e5c38-114">Proveedor específico (producto o servicio - empresa del proveedor no); Por ejemplo, WindowsDefenderATP.</span><span class="sxs-lookup"><span data-stu-id="e5c38-114">Specific provider (product/service - not vendor company); for example, WindowsDefenderATP.</span></span>|
|<span data-ttu-id="e5c38-115">providerVersion</span><span class="sxs-lookup"><span data-stu-id="e5c38-115">providerVersion</span></span>|<span data-ttu-id="e5c38-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5c38-116">String</span></span>|<span data-ttu-id="e5c38-117">Versión del proveedor o subprovider, si existe, que generó la alerta.</span><span class="sxs-lookup"><span data-stu-id="e5c38-117">Version of the provider or subprovider, if it exists, that generated the alert.</span></span> <span data-ttu-id="e5c38-118">*Required*</span><span class="sxs-lookup"><span data-stu-id="e5c38-118">*Required*</span></span>|
|<span data-ttu-id="e5c38-119">subProvider</span><span class="sxs-lookup"><span data-stu-id="e5c38-119">subProvider</span></span>|<span data-ttu-id="e5c38-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5c38-120">String</span></span>|<span data-ttu-id="e5c38-121">Subprovider específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="e5c38-121">Specific subprovider (under aggregating provider); for example, WindowsDefenderATP.SmartScreen.</span></span>|
|<span data-ttu-id="e5c38-122">proveedor</span><span class="sxs-lookup"><span data-stu-id="e5c38-122">vendor</span></span> |<span data-ttu-id="e5c38-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="e5c38-123">String</span></span>|<span data-ttu-id="e5c38-124">Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).</span><span class="sxs-lookup"><span data-stu-id="e5c38-124">Name of the alert vendor (for example, Microsoft, Dell, FireEye).</span></span> <span data-ttu-id="e5c38-125">*Required*</span><span class="sxs-lookup"><span data-stu-id="e5c38-125">*Required*</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e5c38-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5c38-126">JSON representation</span></span>

<span data-ttu-id="e5c38-127">La siguiente es una representación de JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e5c38-127">The folllowing is a JSON representation of the resource.</span></span>
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
