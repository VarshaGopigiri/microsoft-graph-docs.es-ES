---
title: tipo de recurso excludedApps
description: Contiene las propiedades para las aplicaciones de Office365 excluidos.
ms.openlocfilehash: 05c1ed7f4789e1a27ddacf92dbd773b2f5a21847
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085568"
---
# <a name="excludedapps-resource-type"></a><span data-ttu-id="a1c24-103">tipo de recurso excludedApps</span><span class="sxs-lookup"><span data-stu-id="a1c24-103">excludedApps resource type</span></span>

> <span data-ttu-id="a1c24-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a1c24-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a1c24-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a1c24-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a1c24-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a1c24-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a1c24-107">Contiene las propiedades para las aplicaciones de Office365 excluidos.</span><span class="sxs-lookup"><span data-stu-id="a1c24-107">Contains properties for Excluded Office365 Apps.</span></span>
## <a name="properties"></a><span data-ttu-id="a1c24-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1c24-108">Properties</span></span>
|<span data-ttu-id="a1c24-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1c24-109">Property</span></span>|<span data-ttu-id="a1c24-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1c24-110">Type</span></span>|<span data-ttu-id="a1c24-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1c24-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a1c24-112">Access</span><span class="sxs-lookup"><span data-stu-id="a1c24-112">access</span></span>|<span data-ttu-id="a1c24-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-113">Boolean</span></span>|<span data-ttu-id="a1c24-114">El valor de if MS Office Access debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-114">The value for if MS Office Access should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-115">de Excel</span><span class="sxs-lookup"><span data-stu-id="a1c24-115">excel</span></span>|<span data-ttu-id="a1c24-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-116">Boolean</span></span>|<span data-ttu-id="a1c24-117">El valor de if MS Office Excel debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-117">The value for if MS Office Excel should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-118">Groove</span><span class="sxs-lookup"><span data-stu-id="a1c24-118">groove</span></span>|<span data-ttu-id="a1c24-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-119">Boolean</span></span>|<span data-ttu-id="a1c24-120">El valor de if MS Office OneDrive para la empresa - Groove se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-120">The value for if MS Office OneDrive for Business - Groove should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-121">infoPath</span><span class="sxs-lookup"><span data-stu-id="a1c24-121">infoPath</span></span>|<span data-ttu-id="a1c24-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-122">Boolean</span></span>|<span data-ttu-id="a1c24-123">El valor de if MS Office InfoPath se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-123">The value for if MS Office InfoPath should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-124">Lync</span><span class="sxs-lookup"><span data-stu-id="a1c24-124">lync</span></span>|<span data-ttu-id="a1c24-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-125">Boolean</span></span>|<span data-ttu-id="a1c24-126">El valor de if MS Office Skype para la empresa - Lync se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-126">The value for if MS Office Skype for Business - Lync should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-127">oneDrive</span><span class="sxs-lookup"><span data-stu-id="a1c24-127">oneDrive</span></span>|<span data-ttu-id="a1c24-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-128">Boolean</span></span>|<span data-ttu-id="a1c24-129">El valor de if se deben excluir MS Office OneDrive o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-129">The value for if MS Office OneDrive should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-130">oneNote</span><span class="sxs-lookup"><span data-stu-id="a1c24-130">oneNote</span></span>|<span data-ttu-id="a1c24-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-131">Boolean</span></span>|<span data-ttu-id="a1c24-132">El valor de if MS Office OneNote debe excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-132">The value for if MS Office OneNote should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-133">Outlook</span><span class="sxs-lookup"><span data-stu-id="a1c24-133">outlook</span></span>|<span data-ttu-id="a1c24-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-134">Boolean</span></span>|<span data-ttu-id="a1c24-135">El valor de if MS Office Outlook debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-135">The value for if MS Office Outlook should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-136">powerPoint</span><span class="sxs-lookup"><span data-stu-id="a1c24-136">powerPoint</span></span>|<span data-ttu-id="a1c24-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-137">Boolean</span></span>|<span data-ttu-id="a1c24-138">El valor de if MS Office PowerPoint se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-138">The value for if MS Office PowerPoint should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-139">publicador</span><span class="sxs-lookup"><span data-stu-id="a1c24-139">publisher</span></span>|<span data-ttu-id="a1c24-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-140">Boolean</span></span>|<span data-ttu-id="a1c24-141">El valor de if MS Office Publisher se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-141">The value for if MS Office Publisher should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-142">SharePoint Designer</span><span class="sxs-lookup"><span data-stu-id="a1c24-142">sharePointDesigner</span></span>|<span data-ttu-id="a1c24-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-143">Boolean</span></span>|<span data-ttu-id="a1c24-144">El valor de if SharePoint Designer de MS Office debería excluirse o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-144">The value for if MS Office SharePointDesigner should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-145">Visio</span><span class="sxs-lookup"><span data-stu-id="a1c24-145">visio</span></span>|<span data-ttu-id="a1c24-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-146">Boolean</span></span>|<span data-ttu-id="a1c24-147">El valor de if MS Office Visio se deben excluir o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-147">The value for if MS Office Visio should be excluded or not.</span></span>|
|<span data-ttu-id="a1c24-148">Word</span><span class="sxs-lookup"><span data-stu-id="a1c24-148">word</span></span>|<span data-ttu-id="a1c24-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="a1c24-149">Boolean</span></span>|<span data-ttu-id="a1c24-150">El valor de if se deben excluir MS Office Word o no.</span><span class="sxs-lookup"><span data-stu-id="a1c24-150">The value for if MS Office Word should be excluded or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a1c24-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a1c24-151">Relationships</span></span>
<span data-ttu-id="a1c24-152">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a1c24-152">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a1c24-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a1c24-153">JSON Representation</span></span>
<span data-ttu-id="a1c24-154">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a1c24-154">Here is a JSON representation of the resource.</span></span>
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





