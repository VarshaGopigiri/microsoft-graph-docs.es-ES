---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ce30b9ff24067fb2bfec17ad85d3c8827cc6b798
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816005"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="8d61b-103">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="8d61b-103">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="8d61b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d61b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d61b-105">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="8d61b-105">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="8d61b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d61b-106">Properties</span></span>
|<span data-ttu-id="8d61b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d61b-107">Property</span></span>|<span data-ttu-id="8d61b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d61b-108">Type</span></span>|<span data-ttu-id="8d61b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d61b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d61b-110">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="8d61b-110">platformBlocked</span></span>|<span data-ttu-id="8d61b-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d61b-111">Boolean</span></span>|<span data-ttu-id="8d61b-112">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="8d61b-112">Block the platform from enrolling</span></span>|
|<span data-ttu-id="8d61b-113">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="8d61b-113">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="8d61b-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d61b-114">Boolean</span></span>|<span data-ttu-id="8d61b-115">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="8d61b-115">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="8d61b-116">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="8d61b-116">osMinimumVersion</span></span>|<span data-ttu-id="8d61b-117">cadena</span><span class="sxs-lookup"><span data-stu-id="8d61b-117">String</span></span>|<span data-ttu-id="8d61b-118">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="8d61b-118">Min OS version supported</span></span>|
|<span data-ttu-id="8d61b-119">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="8d61b-119">osMaximumVersion</span></span>|<span data-ttu-id="8d61b-120">cadena</span><span class="sxs-lookup"><span data-stu-id="8d61b-120">String</span></span>|<span data-ttu-id="8d61b-121">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="8d61b-121">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d61b-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d61b-122">Relationships</span></span>
<span data-ttu-id="8d61b-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d61b-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d61b-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d61b-124">JSON Representation</span></span>
<span data-ttu-id="8d61b-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d61b-125">Here is a JSON representation of the resource.</span></span>
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



