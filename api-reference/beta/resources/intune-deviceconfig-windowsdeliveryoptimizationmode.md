---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
ms.openlocfilehash: 99795f3d901b538990d4dfec7a426e66794c5946
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085579"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a><span data-ttu-id="87c4b-103">tipo de enumeración windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="87c4b-103">windowsDeliveryOptimizationMode enum type</span></span>

> <span data-ttu-id="87c4b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="87c4b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="87c4b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="87c4b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="87c4b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="87c4b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="87c4b-107">Modo de optimización de entrega para la distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="87c4b-107">Delivery optimization mode for peer distribution</span></span>
## <a name="members"></a><span data-ttu-id="87c4b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="87c4b-108">Members</span></span>
|<span data-ttu-id="87c4b-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="87c4b-109">Member</span></span>|<span data-ttu-id="87c4b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="87c4b-110">Value</span></span>|<span data-ttu-id="87c4b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="87c4b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="87c4b-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="87c4b-112">userDefined</span></span>|<span data-ttu-id="87c4b-113">0</span><span class="sxs-lookup"><span data-stu-id="87c4b-113">0</span></span>|<span data-ttu-id="87c4b-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="87c4b-114">Allow the user to set.</span></span>|
|<span data-ttu-id="87c4b-115">httpOnly</span><span class="sxs-lookup"><span data-stu-id="87c4b-115">httpOnly</span></span>|<span data-ttu-id="87c4b-116">1</span><span class="sxs-lookup"><span data-stu-id="87c4b-116">1</span></span>|<span data-ttu-id="87c4b-117">HTTP sólo, sin interconexión</span><span class="sxs-lookup"><span data-stu-id="87c4b-117">HTTP only, no peering</span></span>|
|<span data-ttu-id="87c4b-118">httpWithPeeringNat</span><span class="sxs-lookup"><span data-stu-id="87c4b-118">httpWithPeeringNat</span></span>|<span data-ttu-id="87c4b-119">2</span><span class="sxs-lookup"><span data-stu-id="87c4b-119">2</span></span>|<span data-ttu-id="87c4b-120">Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red</span><span class="sxs-lookup"><span data-stu-id="87c4b-120">OS default – Http blended with peering behind the same network address translator</span></span>|
|<span data-ttu-id="87c4b-121">httpWithPeeringPrivateGroup</span><span class="sxs-lookup"><span data-stu-id="87c4b-121">httpWithPeeringPrivateGroup</span></span>|<span data-ttu-id="87c4b-122">3</span><span class="sxs-lookup"><span data-stu-id="87c4b-122">3</span></span>|<span data-ttu-id="87c4b-123">Mezcla de HTTP con interconexión a través de un grupo privado</span><span class="sxs-lookup"><span data-stu-id="87c4b-123">HTTP blended with peering across a private group</span></span>|
|<span data-ttu-id="87c4b-124">httpWithInternetPeering</span><span class="sxs-lookup"><span data-stu-id="87c4b-124">httpWithInternetPeering</span></span>|<span data-ttu-id="87c4b-125">4</span><span class="sxs-lookup"><span data-stu-id="87c4b-125">4</span></span>|<span data-ttu-id="87c4b-126">HTTP mezclado con interconexión de Internet</span><span class="sxs-lookup"><span data-stu-id="87c4b-126">HTTP blended with Internet peering</span></span>|
|<span data-ttu-id="87c4b-127">simpleDownload</span><span class="sxs-lookup"><span data-stu-id="87c4b-127">simpleDownload</span></span>|<span data-ttu-id="87c4b-128">99</span><span class="sxs-lookup"><span data-stu-id="87c4b-128">99</span></span>|<span data-ttu-id="87c4b-129">Modo de descarga simple con ningún interconexión</span><span class="sxs-lookup"><span data-stu-id="87c4b-129">Simple download mode with no peering</span></span>|
|<span data-ttu-id="87c4b-130">bypassMode</span><span class="sxs-lookup"><span data-stu-id="87c4b-130">bypassMode</span></span>|<span data-ttu-id="87c4b-131">100</span><span class="sxs-lookup"><span data-stu-id="87c4b-131">100</span></span>|<span data-ttu-id="87c4b-132">Modo de derivación.</span><span class="sxs-lookup"><span data-stu-id="87c4b-132">Bypass mode.</span></span> <span data-ttu-id="87c4b-133">No use la optimización de entrega y usar BITS en su lugar</span><span class="sxs-lookup"><span data-stu-id="87c4b-133">Do not use Delivery Optimization and use BITS instead</span></span>|





