---
title: Tipo de recurso deviceOperatingSystemSummary
description: Resumen de sistemas operativos de dispositivos.
ms.openlocfilehash: 1a543f21d1f82b9f2bee0f004d3b8fab88c863b0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030886"
---
# <a name="deviceoperatingsystemsummary-resource-type"></a><span data-ttu-id="7cd7f-103">Tipo de recurso deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="7cd7f-103">deviceOperatingSystemSummary resource type</span></span>

> <span data-ttu-id="7cd7f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7cd7f-105">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-105">Device operating system summary.</span></span>
## <a name="properties"></a><span data-ttu-id="7cd7f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cd7f-106">Properties</span></span>
|<span data-ttu-id="7cd7f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7cd7f-107">Property</span></span>|<span data-ttu-id="7cd7f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cd7f-108">Type</span></span>|<span data-ttu-id="7cd7f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cd7f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7cd7f-110">androidCount</span><span class="sxs-lookup"><span data-stu-id="7cd7f-110">androidCount</span></span>|<span data-ttu-id="7cd7f-111">Int32</span><span class="sxs-lookup"><span data-stu-id="7cd7f-111">Int32</span></span>|<span data-ttu-id="7cd7f-112">Número del recuento de dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-112">Number of android device count.</span></span>|
|<span data-ttu-id="7cd7f-113">iosCount</span><span class="sxs-lookup"><span data-stu-id="7cd7f-113">iosCount</span></span>|<span data-ttu-id="7cd7f-114">Int32</span><span class="sxs-lookup"><span data-stu-id="7cd7f-114">Int32</span></span>|<span data-ttu-id="7cd7f-115">Número del recuento de dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-115">Number of iOS device count.</span></span>|
|<span data-ttu-id="7cd7f-116">macOSCount</span><span class="sxs-lookup"><span data-stu-id="7cd7f-116">macOSCount</span></span>|<span data-ttu-id="7cd7f-117">Int32</span><span class="sxs-lookup"><span data-stu-id="7cd7f-117">Int32</span></span>|<span data-ttu-id="7cd7f-118">Número del recuento de dispositivos Mac OS X.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-118">Number of Mac OS X device count.</span></span>|
|<span data-ttu-id="7cd7f-119">windowsMobileCount</span><span class="sxs-lookup"><span data-stu-id="7cd7f-119">windowsMobileCount</span></span>|<span data-ttu-id="7cd7f-120">Int32</span><span class="sxs-lookup"><span data-stu-id="7cd7f-120">Int32</span></span>|<span data-ttu-id="7cd7f-121">Número del recuento de dispositivos móviles Windows.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-121">Number of Windows mobile device count.</span></span>|
|<span data-ttu-id="7cd7f-122">windowsCount</span><span class="sxs-lookup"><span data-stu-id="7cd7f-122">windowsCount</span></span>|<span data-ttu-id="7cd7f-123">Int32</span><span class="sxs-lookup"><span data-stu-id="7cd7f-123">Int32</span></span>|<span data-ttu-id="7cd7f-124">Número del recuento de dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-124">Number of Windows device count.</span></span>|
|<span data-ttu-id="7cd7f-125">unknownCount</span><span class="sxs-lookup"><span data-stu-id="7cd7f-125">unknownCount</span></span>|<span data-ttu-id="7cd7f-126">Int32</span><span class="sxs-lookup"><span data-stu-id="7cd7f-126">Int32</span></span>|<span data-ttu-id="7cd7f-127">Número del recuento de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-127">Number of unknown device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7cd7f-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7cd7f-128">Relationships</span></span>
<span data-ttu-id="7cd7f-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7cd7f-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7cd7f-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7cd7f-130">JSON Representation</span></span>
<span data-ttu-id="7cd7f-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7cd7f-131">Here is a JSON representation of the resource.</span></span>
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



