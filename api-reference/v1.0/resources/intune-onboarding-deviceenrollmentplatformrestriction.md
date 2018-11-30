---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
ms.openlocfilehash: b6d4ea3acf4995548fce7f2c86b3c95c444b59b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032623"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="d68b9-103">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d68b9-103">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="d68b9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d68b9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d68b9-105">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="d68b9-105">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="d68b9-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d68b9-106">Properties</span></span>
|<span data-ttu-id="d68b9-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d68b9-107">Property</span></span>|<span data-ttu-id="d68b9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d68b9-108">Type</span></span>|<span data-ttu-id="d68b9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d68b9-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d68b9-110">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="d68b9-110">platformBlocked</span></span>|<span data-ttu-id="d68b9-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="d68b9-111">Boolean</span></span>|<span data-ttu-id="d68b9-112">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="d68b9-112">Block the platform from enrolling</span></span>|
|<span data-ttu-id="d68b9-113">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="d68b9-113">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="d68b9-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="d68b9-114">Boolean</span></span>|<span data-ttu-id="d68b9-115">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="d68b9-115">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="d68b9-116">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="d68b9-116">osMinimumVersion</span></span>|<span data-ttu-id="d68b9-117">cadena</span><span class="sxs-lookup"><span data-stu-id="d68b9-117">String</span></span>|<span data-ttu-id="d68b9-118">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="d68b9-118">Min OS version supported</span></span>|
|<span data-ttu-id="d68b9-119">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="d68b9-119">osMaximumVersion</span></span>|<span data-ttu-id="d68b9-120">cadena</span><span class="sxs-lookup"><span data-stu-id="d68b9-120">String</span></span>|<span data-ttu-id="d68b9-121">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="d68b9-121">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="d68b9-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d68b9-122">Relationships</span></span>
<span data-ttu-id="d68b9-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d68b9-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d68b9-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d68b9-124">JSON Representation</span></span>
<span data-ttu-id="d68b9-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d68b9-125">Here is a JSON representation of the resource.</span></span>
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



