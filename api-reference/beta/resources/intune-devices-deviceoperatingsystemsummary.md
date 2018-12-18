---
title: Tipo de recurso deviceOperatingSystemSummary
description: Resumen de sistemas operativos de dispositivos.
author: tfitzmac
ms.openlocfilehash: 8dd3bf85a75d5acf6ae4bb0cecb8fd360c4e0459
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341863"
---
# <a name="deviceoperatingsystemsummary-resource-type"></a><span data-ttu-id="dd740-103">Tipo de recurso deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="dd740-103">deviceOperatingSystemSummary resource type</span></span>

> <span data-ttu-id="dd740-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dd740-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dd740-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dd740-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dd740-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dd740-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dd740-107">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd740-107">Device operating system summary.</span></span>
## <a name="properties"></a><span data-ttu-id="dd740-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd740-108">Properties</span></span>
|<span data-ttu-id="dd740-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd740-109">Property</span></span>|<span data-ttu-id="dd740-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd740-110">Type</span></span>|<span data-ttu-id="dd740-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd740-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dd740-112">androidCount</span><span class="sxs-lookup"><span data-stu-id="dd740-112">androidCount</span></span>|<span data-ttu-id="dd740-113">Int32</span><span class="sxs-lookup"><span data-stu-id="dd740-113">Int32</span></span>|<span data-ttu-id="dd740-114">Número del recuento de dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="dd740-114">Number of android device count.</span></span>|
|<span data-ttu-id="dd740-115">iosCount</span><span class="sxs-lookup"><span data-stu-id="dd740-115">iosCount</span></span>|<span data-ttu-id="dd740-116">Int32</span><span class="sxs-lookup"><span data-stu-id="dd740-116">Int32</span></span>|<span data-ttu-id="dd740-117">Número del recuento de dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="dd740-117">Number of iOS device count.</span></span>|
|<span data-ttu-id="dd740-118">macOSCount</span><span class="sxs-lookup"><span data-stu-id="dd740-118">macOSCount</span></span>|<span data-ttu-id="dd740-119">Int32</span><span class="sxs-lookup"><span data-stu-id="dd740-119">Int32</span></span>|<span data-ttu-id="dd740-120">Número del recuento de dispositivos Mac OS X.</span><span class="sxs-lookup"><span data-stu-id="dd740-120">Number of Mac OS X device count.</span></span>|
|<span data-ttu-id="dd740-121">windowsMobileCount</span><span class="sxs-lookup"><span data-stu-id="dd740-121">windowsMobileCount</span></span>|<span data-ttu-id="dd740-122">Int32</span><span class="sxs-lookup"><span data-stu-id="dd740-122">Int32</span></span>|<span data-ttu-id="dd740-123">Número del recuento de dispositivos móviles Windows.</span><span class="sxs-lookup"><span data-stu-id="dd740-123">Number of Windows mobile device count.</span></span>|
|<span data-ttu-id="dd740-124">windowsCount</span><span class="sxs-lookup"><span data-stu-id="dd740-124">windowsCount</span></span>|<span data-ttu-id="dd740-125">Int32</span><span class="sxs-lookup"><span data-stu-id="dd740-125">Int32</span></span>|<span data-ttu-id="dd740-126">Número del recuento de dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="dd740-126">Number of Windows device count.</span></span>|
|<span data-ttu-id="dd740-127">unknownCount</span><span class="sxs-lookup"><span data-stu-id="dd740-127">unknownCount</span></span>|<span data-ttu-id="dd740-128">Int32</span><span class="sxs-lookup"><span data-stu-id="dd740-128">Int32</span></span>|<span data-ttu-id="dd740-129">Número del recuento de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="dd740-129">Number of unknown device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dd740-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dd740-130">Relationships</span></span>
<span data-ttu-id="dd740-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="dd740-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="dd740-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dd740-132">JSON Representation</span></span>
<span data-ttu-id="dd740-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dd740-133">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceOperatingSystemSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceOperatingSystemSummary",
  "androidCount": 1024,
  "iosCount": 1024,
  "macOSCount": 1024,
  "windowsMobileCount": 1024,
  "windowsCount": 1024,
  "unknownCount": 1024
}
```





