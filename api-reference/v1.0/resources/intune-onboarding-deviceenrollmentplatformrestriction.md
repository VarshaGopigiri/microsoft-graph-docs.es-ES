---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
author: tfitzmac
ms.openlocfilehash: cccac8240457ffe2b5c27475e8ac9e8fb83200ea
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329389"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="f4afa-103">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="f4afa-103">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="f4afa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4afa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4afa-105">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="f4afa-105">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="f4afa-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4afa-106">Properties</span></span>
|<span data-ttu-id="f4afa-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4afa-107">Property</span></span>|<span data-ttu-id="f4afa-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4afa-108">Type</span></span>|<span data-ttu-id="f4afa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4afa-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4afa-110">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="f4afa-110">platformBlocked</span></span>|<span data-ttu-id="f4afa-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4afa-111">Boolean</span></span>|<span data-ttu-id="f4afa-112">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="f4afa-112">Block the platform from enrolling</span></span>|
|<span data-ttu-id="f4afa-113">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="f4afa-113">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="f4afa-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4afa-114">Boolean</span></span>|<span data-ttu-id="f4afa-115">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="f4afa-115">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="f4afa-116">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="f4afa-116">osMinimumVersion</span></span>|<span data-ttu-id="f4afa-117">cadena</span><span class="sxs-lookup"><span data-stu-id="f4afa-117">String</span></span>|<span data-ttu-id="f4afa-118">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="f4afa-118">Min OS version supported</span></span>|
|<span data-ttu-id="f4afa-119">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="f4afa-119">osMaximumVersion</span></span>|<span data-ttu-id="f4afa-120">cadena</span><span class="sxs-lookup"><span data-stu-id="f4afa-120">String</span></span>|<span data-ttu-id="f4afa-121">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="f4afa-121">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="f4afa-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f4afa-122">Relationships</span></span>
<span data-ttu-id="f4afa-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f4afa-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f4afa-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4afa-124">JSON Representation</span></span>
<span data-ttu-id="f4afa-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f4afa-125">Here is a JSON representation of the resource.</span></span>
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



