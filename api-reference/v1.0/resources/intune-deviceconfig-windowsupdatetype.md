---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 198b5f8db5698d309199964e4cb69f8981ceeb1a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838972"
---
# <a name="windowsupdatetype-enum-type"></a><span data-ttu-id="ef696-103">tipo de enumeración windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="ef696-103">windowsUpdateType enum type</span></span>

> <span data-ttu-id="ef696-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ef696-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ef696-105">Qué dispositivos de sucursal recibirá sus actualizaciones desde</span><span class="sxs-lookup"><span data-stu-id="ef696-105">Which branch devices will receive their updates from</span></span>
## <a name="members"></a><span data-ttu-id="ef696-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef696-106">Members</span></span>
|<span data-ttu-id="ef696-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ef696-107">Member</span></span>|<span data-ttu-id="ef696-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ef696-108">Value</span></span>|<span data-ttu-id="ef696-109">Description</span><span class="sxs-lookup"><span data-stu-id="ef696-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ef696-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="ef696-110">userDefined</span></span>|<span data-ttu-id="ef696-111">0</span><span class="sxs-lookup"><span data-stu-id="ef696-111">0</span></span>|<span data-ttu-id="ef696-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="ef696-112">Allow the user to set.</span></span>|
|<span data-ttu-id="ef696-113">all</span><span class="sxs-lookup"><span data-stu-id="ef696-113">all</span></span>|<span data-ttu-id="ef696-114">1</span><span class="sxs-lookup"><span data-stu-id="ef696-114">1</span></span>|<span data-ttu-id="ef696-115">Punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="ef696-115">Semi-annual Channel (Targeted).</span></span> <span data-ttu-id="ef696-116">Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="ef696-116">Device gets all applicable feature updates from Semi-annual Channel (Targeted).</span></span>|
|<span data-ttu-id="ef696-117">businessReadyOnly</span><span class="sxs-lookup"><span data-stu-id="ef696-117">businessReadyOnly</span></span>|<span data-ttu-id="ef696-118">2</span><span class="sxs-lookup"><span data-stu-id="ef696-118">2</span></span>|<span data-ttu-id="ef696-119">Punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="ef696-119">Semi-annual Channel.</span></span> <span data-ttu-id="ef696-120">Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="ef696-120">Device gets feature updates from Semi-annual Channel.</span></span>|
|<span data-ttu-id="ef696-121">windowsInsiderBuildFast</span><span class="sxs-lookup"><span data-stu-id="ef696-121">windowsInsiderBuildFast</span></span>|<span data-ttu-id="ef696-122">3</span><span class="sxs-lookup"><span data-stu-id="ef696-122">3</span></span>|<span data-ttu-id="ef696-123">Compilación de información confidencial de Windows - Fast</span><span class="sxs-lookup"><span data-stu-id="ef696-123">Windows Insider build - Fast</span></span>|
|<span data-ttu-id="ef696-124">windowsInsiderBuildSlow</span><span class="sxs-lookup"><span data-stu-id="ef696-124">windowsInsiderBuildSlow</span></span>|<span data-ttu-id="ef696-125">4</span><span class="sxs-lookup"><span data-stu-id="ef696-125">4</span></span>|<span data-ttu-id="ef696-126">Compilación de información confidencial de Windows - lento</span><span class="sxs-lookup"><span data-stu-id="ef696-126">Windows Insider build - Slow</span></span>|
|<span data-ttu-id="ef696-127">windowsInsiderBuildRelease</span><span class="sxs-lookup"><span data-stu-id="ef696-127">windowsInsiderBuildRelease</span></span>|<span data-ttu-id="ef696-128">5</span><span class="sxs-lookup"><span data-stu-id="ef696-128">5</span></span>|<span data-ttu-id="ef696-129">Versión de lanzamiento de información confidencial de Windows</span><span class="sxs-lookup"><span data-stu-id="ef696-129">Release Windows Insider build</span></span>|



