---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 15d2d46684d38b57690cc9c12d9c49eccd652e6f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887041"
---
# <a name="windowsupdatetype-enum-type"></a><span data-ttu-id="1cf34-103">tipo de enumeración windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="1cf34-103">windowsUpdateType enum type</span></span>

> <span data-ttu-id="1cf34-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1cf34-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1cf34-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1cf34-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1cf34-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1cf34-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1cf34-107">Qué dispositivos de sucursal recibirá sus actualizaciones desde</span><span class="sxs-lookup"><span data-stu-id="1cf34-107">Which branch devices will receive their updates from</span></span>
## <a name="members"></a><span data-ttu-id="1cf34-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1cf34-108">Members</span></span>
|<span data-ttu-id="1cf34-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="1cf34-109">Member</span></span>|<span data-ttu-id="1cf34-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf34-110">Value</span></span>|<span data-ttu-id="1cf34-111">Description</span><span class="sxs-lookup"><span data-stu-id="1cf34-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1cf34-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="1cf34-112">userDefined</span></span>|<span data-ttu-id="1cf34-113">0</span><span class="sxs-lookup"><span data-stu-id="1cf34-113">0</span></span>|<span data-ttu-id="1cf34-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="1cf34-114">Allow the user to set.</span></span>|
|<span data-ttu-id="1cf34-115">all</span><span class="sxs-lookup"><span data-stu-id="1cf34-115">all</span></span>|<span data-ttu-id="1cf34-116">1</span><span class="sxs-lookup"><span data-stu-id="1cf34-116">1</span></span>|<span data-ttu-id="1cf34-117">Punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="1cf34-117">Semi-annual Channel (Targeted).</span></span> <span data-ttu-id="1cf34-118">Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="1cf34-118">Device gets all applicable feature updates from Semi-annual Channel (Targeted).</span></span>|
|<span data-ttu-id="1cf34-119">businessReadyOnly</span><span class="sxs-lookup"><span data-stu-id="1cf34-119">businessReadyOnly</span></span>|<span data-ttu-id="1cf34-120">2</span><span class="sxs-lookup"><span data-stu-id="1cf34-120">2</span></span>|<span data-ttu-id="1cf34-121">Punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="1cf34-121">Semi-annual Channel.</span></span> <span data-ttu-id="1cf34-122">Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="1cf34-122">Device gets feature updates from Semi-annual Channel.</span></span>|
|<span data-ttu-id="1cf34-123">windowsInsiderBuildFast</span><span class="sxs-lookup"><span data-stu-id="1cf34-123">windowsInsiderBuildFast</span></span>|<span data-ttu-id="1cf34-124">3</span><span class="sxs-lookup"><span data-stu-id="1cf34-124">3</span></span>|<span data-ttu-id="1cf34-125">Compilación de información confidencial de Windows - Fast</span><span class="sxs-lookup"><span data-stu-id="1cf34-125">Windows Insider build - Fast</span></span>|
|<span data-ttu-id="1cf34-126">windowsInsiderBuildSlow</span><span class="sxs-lookup"><span data-stu-id="1cf34-126">windowsInsiderBuildSlow</span></span>|<span data-ttu-id="1cf34-127">4</span><span class="sxs-lookup"><span data-stu-id="1cf34-127">4</span></span>|<span data-ttu-id="1cf34-128">Compilación de información confidencial de Windows - lento</span><span class="sxs-lookup"><span data-stu-id="1cf34-128">Windows Insider build - Slow</span></span>|
|<span data-ttu-id="1cf34-129">windowsInsiderBuildRelease</span><span class="sxs-lookup"><span data-stu-id="1cf34-129">windowsInsiderBuildRelease</span></span>|<span data-ttu-id="1cf34-130">5</span><span class="sxs-lookup"><span data-stu-id="1cf34-130">5</span></span>|<span data-ttu-id="1cf34-131">Versión de lanzamiento de información confidencial de Windows</span><span class="sxs-lookup"><span data-stu-id="1cf34-131">Release Windows Insider build</span></span>|





