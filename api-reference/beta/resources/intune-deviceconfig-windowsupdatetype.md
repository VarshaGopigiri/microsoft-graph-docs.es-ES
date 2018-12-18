---
title: tipo de enumeración windowsUpdateType
description: Qué dispositivos de sucursal recibirá sus actualizaciones desde
author: tfitzmac
ms.openlocfilehash: b41fea0254cbbb6a590d240c2db9e4fb7aa0e6eb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309628"
---
# <a name="windowsupdatetype-enum-type"></a><span data-ttu-id="abe08-103">tipo de enumeración windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="abe08-103">windowsUpdateType enum type</span></span>

> <span data-ttu-id="abe08-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="abe08-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="abe08-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="abe08-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="abe08-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abe08-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abe08-107">Qué dispositivos de sucursal recibirá sus actualizaciones desde</span><span class="sxs-lookup"><span data-stu-id="abe08-107">Which branch devices will receive their updates from</span></span>
## <a name="members"></a><span data-ttu-id="abe08-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="abe08-108">Members</span></span>
|<span data-ttu-id="abe08-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="abe08-109">Member</span></span>|<span data-ttu-id="abe08-110">Valor</span><span class="sxs-lookup"><span data-stu-id="abe08-110">Value</span></span>|<span data-ttu-id="abe08-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="abe08-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abe08-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="abe08-112">userDefined</span></span>|<span data-ttu-id="abe08-113">0</span><span class="sxs-lookup"><span data-stu-id="abe08-113">0</span></span>|<span data-ttu-id="abe08-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="abe08-114">Allow the user to set.</span></span>|
|<span data-ttu-id="abe08-115">all</span><span class="sxs-lookup"><span data-stu-id="abe08-115">all</span></span>|<span data-ttu-id="abe08-116">1</span><span class="sxs-lookup"><span data-stu-id="abe08-116">1</span></span>|<span data-ttu-id="abe08-117">Punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="abe08-117">Semi-annual Channel (Targeted).</span></span> <span data-ttu-id="abe08-118">Dispositivo Obtiene todas las actualizaciones aplicables característica de punto y anuales del canal (destino).</span><span class="sxs-lookup"><span data-stu-id="abe08-118">Device gets all applicable feature updates from Semi-annual Channel (Targeted).</span></span>|
|<span data-ttu-id="abe08-119">businessReadyOnly</span><span class="sxs-lookup"><span data-stu-id="abe08-119">businessReadyOnly</span></span>|<span data-ttu-id="abe08-120">2</span><span class="sxs-lookup"><span data-stu-id="abe08-120">2</span></span>|<span data-ttu-id="abe08-121">Punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="abe08-121">Semi-annual Channel.</span></span> <span data-ttu-id="abe08-122">Dispositivo Obtiene las actualizaciones de la característica de punto y anuales del canal.</span><span class="sxs-lookup"><span data-stu-id="abe08-122">Device gets feature updates from Semi-annual Channel.</span></span>|
|<span data-ttu-id="abe08-123">windowsInsiderBuildFast</span><span class="sxs-lookup"><span data-stu-id="abe08-123">windowsInsiderBuildFast</span></span>|<span data-ttu-id="abe08-124">3</span><span class="sxs-lookup"><span data-stu-id="abe08-124">3</span></span>|<span data-ttu-id="abe08-125">Compilación de información confidencial de Windows - Fast</span><span class="sxs-lookup"><span data-stu-id="abe08-125">Windows Insider build - Fast</span></span>|
|<span data-ttu-id="abe08-126">windowsInsiderBuildSlow</span><span class="sxs-lookup"><span data-stu-id="abe08-126">windowsInsiderBuildSlow</span></span>|<span data-ttu-id="abe08-127">4</span><span class="sxs-lookup"><span data-stu-id="abe08-127">4</span></span>|<span data-ttu-id="abe08-128">Compilación de información confidencial de Windows - lento</span><span class="sxs-lookup"><span data-stu-id="abe08-128">Windows Insider build - Slow</span></span>|
|<span data-ttu-id="abe08-129">windowsInsiderBuildRelease</span><span class="sxs-lookup"><span data-stu-id="abe08-129">windowsInsiderBuildRelease</span></span>|<span data-ttu-id="abe08-130">5</span><span class="sxs-lookup"><span data-stu-id="abe08-130">5</span></span>|<span data-ttu-id="abe08-131">Versión de lanzamiento de información confidencial de Windows</span><span class="sxs-lookup"><span data-stu-id="abe08-131">Release Windows Insider build</span></span>|





