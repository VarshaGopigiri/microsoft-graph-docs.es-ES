---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7879b7f6585908aa760c3169e950cc5257bf49a7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929070"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="e20df-103">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="e20df-103">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="e20df-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e20df-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e20df-105">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="e20df-105">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="e20df-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e20df-106">Properties</span></span>
|<span data-ttu-id="e20df-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e20df-107">Property</span></span>|<span data-ttu-id="e20df-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e20df-108">Type</span></span>|<span data-ttu-id="e20df-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e20df-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e20df-110">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="e20df-110">platformBlocked</span></span>|<span data-ttu-id="e20df-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="e20df-111">Boolean</span></span>|<span data-ttu-id="e20df-112">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="e20df-112">Block the platform from enrolling</span></span>|
|<span data-ttu-id="e20df-113">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="e20df-113">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="e20df-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="e20df-114">Boolean</span></span>|<span data-ttu-id="e20df-115">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="e20df-115">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="e20df-116">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="e20df-116">osMinimumVersion</span></span>|<span data-ttu-id="e20df-117">cadena</span><span class="sxs-lookup"><span data-stu-id="e20df-117">String</span></span>|<span data-ttu-id="e20df-118">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="e20df-118">Min OS version supported</span></span>|
|<span data-ttu-id="e20df-119">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="e20df-119">osMaximumVersion</span></span>|<span data-ttu-id="e20df-120">cadena</span><span class="sxs-lookup"><span data-stu-id="e20df-120">String</span></span>|<span data-ttu-id="e20df-121">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="e20df-121">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="e20df-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e20df-122">Relationships</span></span>
<span data-ttu-id="e20df-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e20df-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e20df-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e20df-124">JSON Representation</span></span>
<span data-ttu-id="e20df-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e20df-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestriction",
  "platformBlocked": true,
  "personalDeviceEnrollmentBlocked": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String"
}
```



