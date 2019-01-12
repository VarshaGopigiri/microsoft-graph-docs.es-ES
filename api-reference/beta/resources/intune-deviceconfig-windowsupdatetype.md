---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1444af64043ac38685ca022b56b8856be77a0b70
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944351"
---
# <a name="windowsupdatetype-enum-type"></a><span data-ttu-id="5272a-103">tipo de enumeración windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="5272a-103">windowsUpdateType enum type</span></span>

> <span data-ttu-id="5272a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5272a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5272a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5272a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5272a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5272a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5272a-107">Qué dispositivos de sucursal recibirá sus actualizaciones desde</span><span class="sxs-lookup"><span data-stu-id="5272a-107">Which branch devices will receive their updates from</span></span>
## <a name="members"></a><span data-ttu-id="5272a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5272a-108">Members</span></span>
|<span data-ttu-id="5272a-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5272a-109">Member</span></span>|<span data-ttu-id="5272a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5272a-110">Value</span></span>|<span data-ttu-id="5272a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5272a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5272a-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="5272a-112">userDefined</span></span>|<span data-ttu-id="5272a-113">0</span><span class="sxs-lookup"><span data-stu-id="5272a-113">0</span></span>|<span data-ttu-id="5272a-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="5272a-114">Allow the user to set.</span></span>|
|<span data-ttu-id="5272a-115">all</span><span class="sxs-lookup"><span data-stu-id="5272a-115">all</span></span>|<span data-ttu-id="5272a-116">1</span><span class="sxs-lookup"><span data-stu-id="5272a-116">1</span></span>|<span data-ttu-id="5272a-117">Punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="5272a-117">Semi-annual Channel (Targeted).</span></span> <span data-ttu-id="5272a-118">Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="5272a-118">Device gets all applicable feature updates from Semi-annual Channel (Targeted).</span></span>|
|<span data-ttu-id="5272a-119">businessReadyOnly</span><span class="sxs-lookup"><span data-stu-id="5272a-119">businessReadyOnly</span></span>|<span data-ttu-id="5272a-120">2</span><span class="sxs-lookup"><span data-stu-id="5272a-120">2</span></span>|<span data-ttu-id="5272a-121">Punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="5272a-121">Semi-annual Channel.</span></span> <span data-ttu-id="5272a-122">Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="5272a-122">Device gets feature updates from Semi-annual Channel.</span></span>|
|<span data-ttu-id="5272a-123">windowsInsiderBuildFast</span><span class="sxs-lookup"><span data-stu-id="5272a-123">windowsInsiderBuildFast</span></span>|<span data-ttu-id="5272a-124">3</span><span class="sxs-lookup"><span data-stu-id="5272a-124">3</span></span>|<span data-ttu-id="5272a-125">Compilación de información confidencial de Windows - Fast</span><span class="sxs-lookup"><span data-stu-id="5272a-125">Windows Insider build - Fast</span></span>|
|<span data-ttu-id="5272a-126">windowsInsiderBuildSlow</span><span class="sxs-lookup"><span data-stu-id="5272a-126">windowsInsiderBuildSlow</span></span>|<span data-ttu-id="5272a-127">4</span><span class="sxs-lookup"><span data-stu-id="5272a-127">4</span></span>|<span data-ttu-id="5272a-128">Compilación de información confidencial de Windows - lento</span><span class="sxs-lookup"><span data-stu-id="5272a-128">Windows Insider build - Slow</span></span>|
|<span data-ttu-id="5272a-129">windowsInsiderBuildRelease</span><span class="sxs-lookup"><span data-stu-id="5272a-129">windowsInsiderBuildRelease</span></span>|<span data-ttu-id="5272a-130">5</span><span class="sxs-lookup"><span data-stu-id="5272a-130">5</span></span>|<span data-ttu-id="5272a-131">Versión de lanzamiento de información confidencial de Windows</span><span class="sxs-lookup"><span data-stu-id="5272a-131">Release Windows Insider build</span></span>|





