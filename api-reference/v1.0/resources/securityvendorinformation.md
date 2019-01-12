---
title: tipo de recurso securityVendorInformation
description: " subProvider = AppLocker)."
localization_priority: Normal
author: preetikr
ms.prod: security
ms.openlocfilehash: fb5dee36da08332fd5c36f7ee4e578cc9fb7deaa
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945940"
---
# <a name="securityvendorinformation-resource-type"></a><span data-ttu-id="03605-103">tipo de recurso securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="03605-103">securityVendorInformation resource type</span></span>

<span data-ttu-id="03605-104">Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="03605-104">Contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span>

## <a name="properties"></a><span data-ttu-id="03605-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03605-105">Properties</span></span>

| <span data-ttu-id="03605-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="03605-106">Property</span></span>   | <span data-ttu-id="03605-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="03605-107">Type</span></span>|<span data-ttu-id="03605-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="03605-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="03605-109">proveedor</span><span class="sxs-lookup"><span data-stu-id="03605-109">provider</span></span> |<span data-ttu-id="03605-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="03605-110">String</span></span>|<span data-ttu-id="03605-111">Proveedor específico (producto o servicio - empresa del proveedor no); Por ejemplo, WindowsDefenderATP.</span><span class="sxs-lookup"><span data-stu-id="03605-111">Specific provider (product/service - not vendor company); for example, WindowsDefenderATP.</span></span>|
|<span data-ttu-id="03605-112">providerVersion</span><span class="sxs-lookup"><span data-stu-id="03605-112">providerVersion</span></span>|<span data-ttu-id="03605-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="03605-113">String</span></span>|<span data-ttu-id="03605-114">Versión del proveedor o subprovider, si existe, que generó la alerta.</span><span class="sxs-lookup"><span data-stu-id="03605-114">Version of the provider or subprovider, if it exists, that generated the alert.</span></span> <span data-ttu-id="03605-115">*Required*</span><span class="sxs-lookup"><span data-stu-id="03605-115">*Required*</span></span>|
|<span data-ttu-id="03605-116">subProvider</span><span class="sxs-lookup"><span data-stu-id="03605-116">subProvider</span></span>|<span data-ttu-id="03605-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="03605-117">String</span></span>|<span data-ttu-id="03605-118">Subprovider específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="03605-118">Specific subprovider (under aggregating provider); for example, WindowsDefenderATP.SmartScreen.</span></span>|
|<span data-ttu-id="03605-119">proveedor</span><span class="sxs-lookup"><span data-stu-id="03605-119">vendor</span></span> |<span data-ttu-id="03605-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="03605-120">String</span></span>|<span data-ttu-id="03605-121">Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).</span><span class="sxs-lookup"><span data-stu-id="03605-121">Name of the alert vendor (for example, Microsoft, Dell, FireEye).</span></span> <span data-ttu-id="03605-122">*Required*</span><span class="sxs-lookup"><span data-stu-id="03605-122">*Required*</span></span>|


## <a name="json-representation"></a><span data-ttu-id="03605-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="03605-123">JSON representation</span></span>

<span data-ttu-id="03605-124">La siguiente es una representación de JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="03605-124">The folllowing is a JSON representation of the resource.</span></span>
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
