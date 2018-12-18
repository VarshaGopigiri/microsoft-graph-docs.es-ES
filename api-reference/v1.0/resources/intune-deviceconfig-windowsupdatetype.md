---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
ms.openlocfilehash: 415dde619529ffa9bb40ab2cea36665558bb0ee9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340841"
---
# <a name="windowsupdatetype-enum-type"></a><span data-ttu-id="34070-103">tipo de enumeración windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="34070-103">windowsUpdateType enum type</span></span>

> <span data-ttu-id="34070-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="34070-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="34070-105">Qué dispositivos de sucursal recibirá sus actualizaciones desde</span><span class="sxs-lookup"><span data-stu-id="34070-105">Which branch devices will receive their updates from</span></span>
## <a name="members"></a><span data-ttu-id="34070-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="34070-106">Members</span></span>
|<span data-ttu-id="34070-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="34070-107">Member</span></span>|<span data-ttu-id="34070-108">Valor</span><span class="sxs-lookup"><span data-stu-id="34070-108">Value</span></span>|<span data-ttu-id="34070-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="34070-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="34070-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="34070-110">userDefined</span></span>|<span data-ttu-id="34070-111">0</span><span class="sxs-lookup"><span data-stu-id="34070-111">0</span></span>|<span data-ttu-id="34070-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="34070-112">Allow the user to set.</span></span>|
|<span data-ttu-id="34070-113">all</span><span class="sxs-lookup"><span data-stu-id="34070-113">all</span></span>|<span data-ttu-id="34070-114">1</span><span class="sxs-lookup"><span data-stu-id="34070-114">1</span></span>|<span data-ttu-id="34070-115">Punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="34070-115">Semi-annual Channel (Targeted).</span></span> <span data-ttu-id="34070-116">Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="34070-116">Device gets all applicable feature updates from Semi-annual Channel (Targeted).</span></span>|
|<span data-ttu-id="34070-117">businessReadyOnly</span><span class="sxs-lookup"><span data-stu-id="34070-117">businessReadyOnly</span></span>|<span data-ttu-id="34070-118">2</span><span class="sxs-lookup"><span data-stu-id="34070-118">2</span></span>|<span data-ttu-id="34070-119">Punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="34070-119">Semi-annual Channel.</span></span> <span data-ttu-id="34070-120">Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="34070-120">Device gets feature updates from Semi-annual Channel.</span></span>|
|<span data-ttu-id="34070-121">windowsInsiderBuildFast</span><span class="sxs-lookup"><span data-stu-id="34070-121">windowsInsiderBuildFast</span></span>|<span data-ttu-id="34070-122">3</span><span class="sxs-lookup"><span data-stu-id="34070-122">3</span></span>|<span data-ttu-id="34070-123">Compilación de información confidencial de Windows - Fast</span><span class="sxs-lookup"><span data-stu-id="34070-123">Windows Insider build - Fast</span></span>|
|<span data-ttu-id="34070-124">windowsInsiderBuildSlow</span><span class="sxs-lookup"><span data-stu-id="34070-124">windowsInsiderBuildSlow</span></span>|<span data-ttu-id="34070-125">4</span><span class="sxs-lookup"><span data-stu-id="34070-125">4</span></span>|<span data-ttu-id="34070-126">Compilación de información confidencial de Windows - lento</span><span class="sxs-lookup"><span data-stu-id="34070-126">Windows Insider build - Slow</span></span>|
|<span data-ttu-id="34070-127">windowsInsiderBuildRelease</span><span class="sxs-lookup"><span data-stu-id="34070-127">windowsInsiderBuildRelease</span></span>|<span data-ttu-id="34070-128">5</span><span class="sxs-lookup"><span data-stu-id="34070-128">5</span></span>|<span data-ttu-id="34070-129">Versión de lanzamiento de información confidencial de Windows</span><span class="sxs-lookup"><span data-stu-id="34070-129">Release Windows Insider build</span></span>|



