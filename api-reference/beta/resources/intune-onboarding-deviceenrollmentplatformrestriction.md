---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 009485c2051c47209074ae8b938e6b1b06de9eac
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843865"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="c9964-103">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="c9964-103">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="c9964-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c9964-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c9964-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c9964-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c9964-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c9964-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c9964-107">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="c9964-107">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="c9964-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9964-108">Properties</span></span>
|<span data-ttu-id="c9964-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c9964-109">Property</span></span>|<span data-ttu-id="c9964-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9964-110">Type</span></span>|<span data-ttu-id="c9964-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9964-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c9964-112">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="c9964-112">platformBlocked</span></span>|<span data-ttu-id="c9964-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="c9964-113">Boolean</span></span>|<span data-ttu-id="c9964-114">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="c9964-114">Block the platform from enrolling</span></span>|
|<span data-ttu-id="c9964-115">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="c9964-115">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="c9964-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="c9964-116">Boolean</span></span>|<span data-ttu-id="c9964-117">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="c9964-117">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="c9964-118">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="c9964-118">osMinimumVersion</span></span>|<span data-ttu-id="c9964-119">cadena</span><span class="sxs-lookup"><span data-stu-id="c9964-119">String</span></span>|<span data-ttu-id="c9964-120">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="c9964-120">Min OS version supported</span></span>|
|<span data-ttu-id="c9964-121">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="c9964-121">osMaximumVersion</span></span>|<span data-ttu-id="c9964-122">cadena</span><span class="sxs-lookup"><span data-stu-id="c9964-122">String</span></span>|<span data-ttu-id="c9964-123">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="c9964-123">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="c9964-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c9964-124">Relationships</span></span>
<span data-ttu-id="c9964-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c9964-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c9964-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c9964-126">JSON Representation</span></span>
<span data-ttu-id="c9964-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9964-127">Here is a JSON representation of the resource.</span></span>
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





