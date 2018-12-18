---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
author: tfitzmac
ms.openlocfilehash: 22401c83b3e68d66a2bd7a39359602e2aca0a932
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304126"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="84de4-103">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="84de4-103">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="84de4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="84de4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="84de4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="84de4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="84de4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84de4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84de4-107">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="84de4-107">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="84de4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84de4-108">Properties</span></span>
|<span data-ttu-id="84de4-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84de4-109">Property</span></span>|<span data-ttu-id="84de4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="84de4-110">Type</span></span>|<span data-ttu-id="84de4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="84de4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84de4-112">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="84de4-112">platformBlocked</span></span>|<span data-ttu-id="84de4-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="84de4-113">Boolean</span></span>|<span data-ttu-id="84de4-114">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="84de4-114">Block the platform from enrolling</span></span>|
|<span data-ttu-id="84de4-115">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="84de4-115">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="84de4-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="84de4-116">Boolean</span></span>|<span data-ttu-id="84de4-117">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="84de4-117">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="84de4-118">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="84de4-118">osMinimumVersion</span></span>|<span data-ttu-id="84de4-119">cadena</span><span class="sxs-lookup"><span data-stu-id="84de4-119">String</span></span>|<span data-ttu-id="84de4-120">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="84de4-120">Min OS version supported</span></span>|
|<span data-ttu-id="84de4-121">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="84de4-121">osMaximumVersion</span></span>|<span data-ttu-id="84de4-122">cadena</span><span class="sxs-lookup"><span data-stu-id="84de4-122">String</span></span>|<span data-ttu-id="84de4-123">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="84de4-123">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="84de4-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="84de4-124">Relationships</span></span>
<span data-ttu-id="84de4-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="84de4-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="84de4-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84de4-126">JSON Representation</span></span>
<span data-ttu-id="84de4-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="84de4-127">Here is a JSON representation of the resource.</span></span>
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





