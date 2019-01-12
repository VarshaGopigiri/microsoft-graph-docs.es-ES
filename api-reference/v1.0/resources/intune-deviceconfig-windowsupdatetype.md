---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 90d1f946dd497e650df5eb07004560dda028e14f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930344"
---
# <a name="windowsupdatetype-enum-type"></a><span data-ttu-id="31360-103">tipo de enumeración windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="31360-103">windowsUpdateType enum type</span></span>

> <span data-ttu-id="31360-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31360-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31360-105">Qué dispositivos de sucursal recibirá sus actualizaciones desde</span><span class="sxs-lookup"><span data-stu-id="31360-105">Which branch devices will receive their updates from</span></span>
## <a name="members"></a><span data-ttu-id="31360-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="31360-106">Members</span></span>
|<span data-ttu-id="31360-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="31360-107">Member</span></span>|<span data-ttu-id="31360-108">Valor</span><span class="sxs-lookup"><span data-stu-id="31360-108">Value</span></span>|<span data-ttu-id="31360-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="31360-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31360-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="31360-110">userDefined</span></span>|<span data-ttu-id="31360-111">0</span><span class="sxs-lookup"><span data-stu-id="31360-111">0</span></span>|<span data-ttu-id="31360-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="31360-112">Allow the user to set.</span></span>|
|<span data-ttu-id="31360-113">all</span><span class="sxs-lookup"><span data-stu-id="31360-113">all</span></span>|<span data-ttu-id="31360-114">1</span><span class="sxs-lookup"><span data-stu-id="31360-114">1</span></span>|<span data-ttu-id="31360-115">Punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="31360-115">Semi-annual Channel (Targeted).</span></span> <span data-ttu-id="31360-116">Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="31360-116">Device gets all applicable feature updates from Semi-annual Channel (Targeted).</span></span>|
|<span data-ttu-id="31360-117">businessReadyOnly</span><span class="sxs-lookup"><span data-stu-id="31360-117">businessReadyOnly</span></span>|<span data-ttu-id="31360-118">2</span><span class="sxs-lookup"><span data-stu-id="31360-118">2</span></span>|<span data-ttu-id="31360-119">Punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="31360-119">Semi-annual Channel.</span></span> <span data-ttu-id="31360-120">Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="31360-120">Device gets feature updates from Semi-annual Channel.</span></span>|
|<span data-ttu-id="31360-121">windowsInsiderBuildFast</span><span class="sxs-lookup"><span data-stu-id="31360-121">windowsInsiderBuildFast</span></span>|<span data-ttu-id="31360-122">3</span><span class="sxs-lookup"><span data-stu-id="31360-122">3</span></span>|<span data-ttu-id="31360-123">Compilación de información confidencial de Windows - Fast</span><span class="sxs-lookup"><span data-stu-id="31360-123">Windows Insider build - Fast</span></span>|
|<span data-ttu-id="31360-124">windowsInsiderBuildSlow</span><span class="sxs-lookup"><span data-stu-id="31360-124">windowsInsiderBuildSlow</span></span>|<span data-ttu-id="31360-125">4</span><span class="sxs-lookup"><span data-stu-id="31360-125">4</span></span>|<span data-ttu-id="31360-126">Compilación de información confidencial de Windows - lento</span><span class="sxs-lookup"><span data-stu-id="31360-126">Windows Insider build - Slow</span></span>|
|<span data-ttu-id="31360-127">windowsInsiderBuildRelease</span><span class="sxs-lookup"><span data-stu-id="31360-127">windowsInsiderBuildRelease</span></span>|<span data-ttu-id="31360-128">5</span><span class="sxs-lookup"><span data-stu-id="31360-128">5</span></span>|<span data-ttu-id="31360-129">Versión de lanzamiento de información confidencial de Windows</span><span class="sxs-lookup"><span data-stu-id="31360-129">Release Windows Insider build</span></span>|



