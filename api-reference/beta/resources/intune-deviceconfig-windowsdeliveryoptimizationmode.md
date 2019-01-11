---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e62416328e596737c36d920d6877773c905680c5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807724"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a><span data-ttu-id="eec74-103">tipo de enumeración windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="eec74-103">windowsDeliveryOptimizationMode enum type</span></span>

> <span data-ttu-id="eec74-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eec74-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eec74-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eec74-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eec74-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eec74-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eec74-107">Modo de optimización de entrega para la distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="eec74-107">Delivery optimization mode for peer distribution</span></span>
## <a name="members"></a><span data-ttu-id="eec74-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="eec74-108">Members</span></span>
|<span data-ttu-id="eec74-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="eec74-109">Member</span></span>|<span data-ttu-id="eec74-110">Valor</span><span class="sxs-lookup"><span data-stu-id="eec74-110">Value</span></span>|<span data-ttu-id="eec74-111">Description</span><span class="sxs-lookup"><span data-stu-id="eec74-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eec74-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="eec74-112">userDefined</span></span>|<span data-ttu-id="eec74-113">0</span><span class="sxs-lookup"><span data-stu-id="eec74-113">0</span></span>|<span data-ttu-id="eec74-114">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="eec74-114">Allow the user to set.</span></span>|
|<span data-ttu-id="eec74-115">httpOnly</span><span class="sxs-lookup"><span data-stu-id="eec74-115">httpOnly</span></span>|<span data-ttu-id="eec74-116">1</span><span class="sxs-lookup"><span data-stu-id="eec74-116">1</span></span>|<span data-ttu-id="eec74-117">HTTP sólo, sin interconexión</span><span class="sxs-lookup"><span data-stu-id="eec74-117">HTTP only, no peering</span></span>|
|<span data-ttu-id="eec74-118">httpWithPeeringNat</span><span class="sxs-lookup"><span data-stu-id="eec74-118">httpWithPeeringNat</span></span>|<span data-ttu-id="eec74-119">2</span><span class="sxs-lookup"><span data-stu-id="eec74-119">2</span></span>|<span data-ttu-id="eec74-120">Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red</span><span class="sxs-lookup"><span data-stu-id="eec74-120">OS default – Http blended with peering behind the same network address translator</span></span>|
|<span data-ttu-id="eec74-121">httpWithPeeringPrivateGroup</span><span class="sxs-lookup"><span data-stu-id="eec74-121">httpWithPeeringPrivateGroup</span></span>|<span data-ttu-id="eec74-122">3</span><span class="sxs-lookup"><span data-stu-id="eec74-122">3</span></span>|<span data-ttu-id="eec74-123">Mezcla de HTTP con interconexión a través de un grupo privado</span><span class="sxs-lookup"><span data-stu-id="eec74-123">HTTP blended with peering across a private group</span></span>|
|<span data-ttu-id="eec74-124">httpWithInternetPeering</span><span class="sxs-lookup"><span data-stu-id="eec74-124">httpWithInternetPeering</span></span>|<span data-ttu-id="eec74-125">4</span><span class="sxs-lookup"><span data-stu-id="eec74-125">4</span></span>|<span data-ttu-id="eec74-126">HTTP mezclado con interconexión de Internet</span><span class="sxs-lookup"><span data-stu-id="eec74-126">HTTP blended with Internet peering</span></span>|
|<span data-ttu-id="eec74-127">simpleDownload</span><span class="sxs-lookup"><span data-stu-id="eec74-127">simpleDownload</span></span>|<span data-ttu-id="eec74-128">99</span><span class="sxs-lookup"><span data-stu-id="eec74-128">99</span></span>|<span data-ttu-id="eec74-129">Modo de descarga simple con ningún interconexión</span><span class="sxs-lookup"><span data-stu-id="eec74-129">Simple download mode with no peering</span></span>|
|<span data-ttu-id="eec74-130">bypassMode</span><span class="sxs-lookup"><span data-stu-id="eec74-130">bypassMode</span></span>|<span data-ttu-id="eec74-131">100</span><span class="sxs-lookup"><span data-stu-id="eec74-131">100</span></span>|<span data-ttu-id="eec74-132">Modo de derivación.</span><span class="sxs-lookup"><span data-stu-id="eec74-132">Bypass mode.</span></span> <span data-ttu-id="eec74-133">No use la optimización de entrega y usar BITS en su lugar</span><span class="sxs-lookup"><span data-stu-id="eec74-133">Do not use Delivery Optimization and use BITS instead</span></span>|





