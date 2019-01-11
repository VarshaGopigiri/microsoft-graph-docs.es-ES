---
title: Tipo de recurso deviceOperatingSystemSummary
description: Resumen de sistemas operativos de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b4b53d7c7260e58458995093bbea17df5464e704
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846078"
---
# <a name="deviceoperatingsystemsummary-resource-type"></a><span data-ttu-id="ddce8-103">Tipo de recurso deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="ddce8-103">deviceOperatingSystemSummary resource type</span></span>

> <span data-ttu-id="ddce8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ddce8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ddce8-105">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ddce8-105">Device operating system summary.</span></span>
## <a name="properties"></a><span data-ttu-id="ddce8-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddce8-106">Properties</span></span>
|<span data-ttu-id="ddce8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ddce8-107">Property</span></span>|<span data-ttu-id="ddce8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddce8-108">Type</span></span>|<span data-ttu-id="ddce8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddce8-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ddce8-110">androidCount</span><span class="sxs-lookup"><span data-stu-id="ddce8-110">androidCount</span></span>|<span data-ttu-id="ddce8-111">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce8-111">Int32</span></span>|<span data-ttu-id="ddce8-112">Número del recuento de dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="ddce8-112">Number of android device count.</span></span>|
|<span data-ttu-id="ddce8-113">iosCount</span><span class="sxs-lookup"><span data-stu-id="ddce8-113">iosCount</span></span>|<span data-ttu-id="ddce8-114">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce8-114">Int32</span></span>|<span data-ttu-id="ddce8-115">Número del recuento de dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="ddce8-115">Number of iOS device count.</span></span>|
|<span data-ttu-id="ddce8-116">macOSCount</span><span class="sxs-lookup"><span data-stu-id="ddce8-116">macOSCount</span></span>|<span data-ttu-id="ddce8-117">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce8-117">Int32</span></span>|<span data-ttu-id="ddce8-118">Número del recuento de dispositivos Mac OS X.</span><span class="sxs-lookup"><span data-stu-id="ddce8-118">Number of Mac OS X device count.</span></span>|
|<span data-ttu-id="ddce8-119">windowsMobileCount</span><span class="sxs-lookup"><span data-stu-id="ddce8-119">windowsMobileCount</span></span>|<span data-ttu-id="ddce8-120">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce8-120">Int32</span></span>|<span data-ttu-id="ddce8-121">Número del recuento de dispositivos móviles Windows.</span><span class="sxs-lookup"><span data-stu-id="ddce8-121">Number of Windows mobile device count.</span></span>|
|<span data-ttu-id="ddce8-122">windowsCount</span><span class="sxs-lookup"><span data-stu-id="ddce8-122">windowsCount</span></span>|<span data-ttu-id="ddce8-123">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce8-123">Int32</span></span>|<span data-ttu-id="ddce8-124">Número del recuento de dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="ddce8-124">Number of Windows device count.</span></span>|
|<span data-ttu-id="ddce8-125">unknownCount</span><span class="sxs-lookup"><span data-stu-id="ddce8-125">unknownCount</span></span>|<span data-ttu-id="ddce8-126">Int32</span><span class="sxs-lookup"><span data-stu-id="ddce8-126">Int32</span></span>|<span data-ttu-id="ddce8-127">Número del recuento de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="ddce8-127">Number of unknown device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ddce8-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ddce8-128">Relationships</span></span>
<span data-ttu-id="ddce8-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ddce8-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ddce8-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ddce8-130">JSON Representation</span></span>
<span data-ttu-id="ddce8-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ddce8-131">Here is a JSON representation of the resource.</span></span>
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



