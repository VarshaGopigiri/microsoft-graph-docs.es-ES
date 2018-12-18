---
title: Tipo de recurso deviceOperatingSystemSummary
description: Resumen de sistemas operativos de dispositivos.
author: tfitzmac
ms.openlocfilehash: 73615964d0c2b187c36b57956d534fa08d60684f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346623"
---
# <a name="deviceoperatingsystemsummary-resource-type"></a><span data-ttu-id="ecb92-103">Tipo de recurso deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="ecb92-103">deviceOperatingSystemSummary resource type</span></span>

> <span data-ttu-id="ecb92-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ecb92-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ecb92-105">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ecb92-105">Device operating system summary.</span></span>
## <a name="properties"></a><span data-ttu-id="ecb92-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ecb92-106">Properties</span></span>
|<span data-ttu-id="ecb92-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ecb92-107">Property</span></span>|<span data-ttu-id="ecb92-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ecb92-108">Type</span></span>|<span data-ttu-id="ecb92-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecb92-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ecb92-110">androidCount</span><span class="sxs-lookup"><span data-stu-id="ecb92-110">androidCount</span></span>|<span data-ttu-id="ecb92-111">Int32</span><span class="sxs-lookup"><span data-stu-id="ecb92-111">Int32</span></span>|<span data-ttu-id="ecb92-112">Número del recuento de dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="ecb92-112">Number of android device count.</span></span>|
|<span data-ttu-id="ecb92-113">iosCount</span><span class="sxs-lookup"><span data-stu-id="ecb92-113">iosCount</span></span>|<span data-ttu-id="ecb92-114">Int32</span><span class="sxs-lookup"><span data-stu-id="ecb92-114">Int32</span></span>|<span data-ttu-id="ecb92-115">Número del recuento de dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="ecb92-115">Number of iOS device count.</span></span>|
|<span data-ttu-id="ecb92-116">macOSCount</span><span class="sxs-lookup"><span data-stu-id="ecb92-116">macOSCount</span></span>|<span data-ttu-id="ecb92-117">Int32</span><span class="sxs-lookup"><span data-stu-id="ecb92-117">Int32</span></span>|<span data-ttu-id="ecb92-118">Número del recuento de dispositivos Mac OS X.</span><span class="sxs-lookup"><span data-stu-id="ecb92-118">Number of Mac OS X device count.</span></span>|
|<span data-ttu-id="ecb92-119">windowsMobileCount</span><span class="sxs-lookup"><span data-stu-id="ecb92-119">windowsMobileCount</span></span>|<span data-ttu-id="ecb92-120">Int32</span><span class="sxs-lookup"><span data-stu-id="ecb92-120">Int32</span></span>|<span data-ttu-id="ecb92-121">Número del recuento de dispositivos móviles Windows.</span><span class="sxs-lookup"><span data-stu-id="ecb92-121">Number of Windows mobile device count.</span></span>|
|<span data-ttu-id="ecb92-122">windowsCount</span><span class="sxs-lookup"><span data-stu-id="ecb92-122">windowsCount</span></span>|<span data-ttu-id="ecb92-123">Int32</span><span class="sxs-lookup"><span data-stu-id="ecb92-123">Int32</span></span>|<span data-ttu-id="ecb92-124">Número del recuento de dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="ecb92-124">Number of Windows device count.</span></span>|
|<span data-ttu-id="ecb92-125">unknownCount</span><span class="sxs-lookup"><span data-stu-id="ecb92-125">unknownCount</span></span>|<span data-ttu-id="ecb92-126">Int32</span><span class="sxs-lookup"><span data-stu-id="ecb92-126">Int32</span></span>|<span data-ttu-id="ecb92-127">Número del recuento de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="ecb92-127">Number of unknown device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ecb92-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ecb92-128">Relationships</span></span>
<span data-ttu-id="ecb92-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ecb92-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ecb92-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ecb92-130">JSON Representation</span></span>
<span data-ttu-id="ecb92-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ecb92-131">Here is a JSON representation of the resource.</span></span>
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



