---
title: tipo de recurso excludedApps
description: Contiene las propiedades para las aplicaciones de Office365 excluidos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 90216c639d36a989b2fad5dbdc1adbd11fe46ede
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943952"
---
# <a name="excludedapps-resource-type"></a><span data-ttu-id="0b6d2-103">tipo de recurso excludedApps</span><span class="sxs-lookup"><span data-stu-id="0b6d2-103">excludedApps resource type</span></span>

> <span data-ttu-id="0b6d2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b6d2-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0b6d2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0b6d2-107">Contiene las propiedades para las aplicaciones de Office365 excluidos.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-107">Contains properties for Excluded Office365 Apps.</span></span>
## <a name="properties"></a><span data-ttu-id="0b6d2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b6d2-108">Properties</span></span>
|<span data-ttu-id="0b6d2-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b6d2-109">Property</span></span>|<span data-ttu-id="0b6d2-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b6d2-110">Type</span></span>|<span data-ttu-id="0b6d2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b6d2-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0b6d2-112">Access</span><span class="sxs-lookup"><span data-stu-id="0b6d2-112">access</span></span>|<span data-ttu-id="0b6d2-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-113">Boolean</span></span>|<span data-ttu-id="0b6d2-114">El valor de if MS Office Access debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-114">The value for if MS Office Access should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-115">de Excel</span><span class="sxs-lookup"><span data-stu-id="0b6d2-115">excel</span></span>|<span data-ttu-id="0b6d2-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-116">Boolean</span></span>|<span data-ttu-id="0b6d2-117">El valor de if MS Office Excel debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-117">The value for if MS Office Excel should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-118">Groove</span><span class="sxs-lookup"><span data-stu-id="0b6d2-118">groove</span></span>|<span data-ttu-id="0b6d2-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-119">Boolean</span></span>|<span data-ttu-id="0b6d2-120">El valor de if MS Office OneDrive para la empresa - Groove se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-120">The value for if MS Office OneDrive for Business - Groove should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-121">infoPath</span><span class="sxs-lookup"><span data-stu-id="0b6d2-121">infoPath</span></span>|<span data-ttu-id="0b6d2-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-122">Boolean</span></span>|<span data-ttu-id="0b6d2-123">El valor de if MS Office InfoPath se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-123">The value for if MS Office InfoPath should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-124">Lync</span><span class="sxs-lookup"><span data-stu-id="0b6d2-124">lync</span></span>|<span data-ttu-id="0b6d2-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-125">Boolean</span></span>|<span data-ttu-id="0b6d2-126">El valor de if MS Office Skype para la empresa - Lync se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-126">The value for if MS Office Skype for Business - Lync should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-127">oneDrive</span><span class="sxs-lookup"><span data-stu-id="0b6d2-127">oneDrive</span></span>|<span data-ttu-id="0b6d2-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-128">Boolean</span></span>|<span data-ttu-id="0b6d2-129">El valor de if se deben excluir MS Office OneDrive o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-129">The value for if MS Office OneDrive should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-130">oneNote</span><span class="sxs-lookup"><span data-stu-id="0b6d2-130">oneNote</span></span>|<span data-ttu-id="0b6d2-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-131">Boolean</span></span>|<span data-ttu-id="0b6d2-132">El valor de if MS Office OneNote debe excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-132">The value for if MS Office OneNote should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-133">Outlook</span><span class="sxs-lookup"><span data-stu-id="0b6d2-133">outlook</span></span>|<span data-ttu-id="0b6d2-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-134">Boolean</span></span>|<span data-ttu-id="0b6d2-135">El valor de if MS Office Outlook debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-135">The value for if MS Office Outlook should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-136">powerPoint</span><span class="sxs-lookup"><span data-stu-id="0b6d2-136">powerPoint</span></span>|<span data-ttu-id="0b6d2-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-137">Boolean</span></span>|<span data-ttu-id="0b6d2-138">El valor de if MS Office PowerPoint se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-138">The value for if MS Office PowerPoint should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-139">publicador</span><span class="sxs-lookup"><span data-stu-id="0b6d2-139">publisher</span></span>|<span data-ttu-id="0b6d2-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-140">Boolean</span></span>|<span data-ttu-id="0b6d2-141">El valor de if MS Office Publisher se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-141">The value for if MS Office Publisher should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-142">SharePoint Designer</span><span class="sxs-lookup"><span data-stu-id="0b6d2-142">sharePointDesigner</span></span>|<span data-ttu-id="0b6d2-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-143">Boolean</span></span>|<span data-ttu-id="0b6d2-144">El valor de if SharePoint Designer de MS Office debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-144">The value for if MS Office SharePointDesigner should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-145">Visio</span><span class="sxs-lookup"><span data-stu-id="0b6d2-145">visio</span></span>|<span data-ttu-id="0b6d2-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-146">Boolean</span></span>|<span data-ttu-id="0b6d2-147">El valor de if MS Office Visio se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-147">The value for if MS Office Visio should be excluded or not.</span></span>|
|<span data-ttu-id="0b6d2-148">Word</span><span class="sxs-lookup"><span data-stu-id="0b6d2-148">word</span></span>|<span data-ttu-id="0b6d2-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b6d2-149">Boolean</span></span>|<span data-ttu-id="0b6d2-150">El valor de if se deben excluir MS Office Word o no.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-150">The value for if MS Office Word should be excluded or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0b6d2-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0b6d2-151">Relationships</span></span>
<span data-ttu-id="0b6d2-152">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0b6d2-152">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0b6d2-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b6d2-153">JSON Representation</span></span>
<span data-ttu-id="0b6d2-154">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-154">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.excludedApps"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.excludedApps",
  "access": true,
  "excel": true,
  "groove": true,
  "infoPath": true,
  "lync": true,
  "oneDrive": true,
  "oneNote": true,
  "outlook": true,
  "powerPoint": true,
  "publisher": true,
  "sharePointDesigner": true,
  "visio": true,
  "word": true
}
```





