---
title: Tipo de recurso vppLicensingType
description: Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5d4b7983d20f22be5f8cce24a5c362926d00de55
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851600"
---
# <a name="vpplicensingtype-resource-type"></a><span data-ttu-id="4fc0c-103">Tipo de recurso vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="4fc0c-103">vppLicensingType resource type</span></span>

> <span data-ttu-id="4fc0c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4fc0c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4fc0c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4fc0c-107">Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-107">Contains properties for iOS Volume-Purchased Program (Vpp) Licensing Type.</span></span>
## <a name="properties"></a><span data-ttu-id="4fc0c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fc0c-108">Properties</span></span>
|<span data-ttu-id="4fc0c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4fc0c-109">Property</span></span>|<span data-ttu-id="4fc0c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fc0c-110">Type</span></span>|<span data-ttu-id="4fc0c-111">Description</span><span class="sxs-lookup"><span data-stu-id="4fc0c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4fc0c-112">supportUserLicensing</span><span class="sxs-lookup"><span data-stu-id="4fc0c-112">supportUserLicensing</span></span>|<span data-ttu-id="4fc0c-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fc0c-113">Boolean</span></span>|<span data-ttu-id="4fc0c-114">Si el programa es compatible con el tipo de licencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-114">Whether the program supports the user licensing type.</span></span>|
|<span data-ttu-id="4fc0c-115">supportDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="4fc0c-115">supportDeviceLicensing</span></span>|<span data-ttu-id="4fc0c-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fc0c-116">Boolean</span></span>|<span data-ttu-id="4fc0c-117">Si el programa es compatible con el tipo de licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-117">Whether the program supports the device licensing type.</span></span>|
|<span data-ttu-id="4fc0c-118">supportsUserLicensing</span><span class="sxs-lookup"><span data-stu-id="4fc0c-118">supportsUserLicensing</span></span>|<span data-ttu-id="4fc0c-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fc0c-119">Boolean</span></span>|<span data-ttu-id="4fc0c-120">Si el programa es compatible con el tipo de licencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-120">Whether the program supports the user licensing type.</span></span>|
|<span data-ttu-id="4fc0c-121">supportsDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="4fc0c-121">supportsDeviceLicensing</span></span>|<span data-ttu-id="4fc0c-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fc0c-122">Boolean</span></span>|<span data-ttu-id="4fc0c-123">Si el programa es compatible con el tipo de licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-123">Whether the program supports the device licensing type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4fc0c-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4fc0c-124">Relationships</span></span>
<span data-ttu-id="4fc0c-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4fc0c-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4fc0c-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4fc0c-126">JSON Representation</span></span>
<span data-ttu-id="4fc0c-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4fc0c-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppLicensingType"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppLicensingType",
  "supportUserLicensing": true,
  "supportDeviceLicensing": true,
  "supportsUserLicensing": true,
  "supportsDeviceLicensing": true
}
```





