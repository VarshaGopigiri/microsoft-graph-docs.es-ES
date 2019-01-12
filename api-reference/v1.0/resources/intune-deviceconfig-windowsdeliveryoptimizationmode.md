---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f80c6b5cbe7316c851954154bdb559f370f02b79
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951519"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a><span data-ttu-id="c1c8e-103">tipo de enumeración windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="c1c8e-103">windowsDeliveryOptimizationMode enum type</span></span>

> <span data-ttu-id="c1c8e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c1c8e-105">Modo de optimización de entrega para la distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="c1c8e-105">Delivery optimization mode for peer distribution</span></span>
## <a name="members"></a><span data-ttu-id="c1c8e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1c8e-106">Members</span></span>
|<span data-ttu-id="c1c8e-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="c1c8e-107">Member</span></span>|<span data-ttu-id="c1c8e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c1c8e-108">Value</span></span>|<span data-ttu-id="c1c8e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1c8e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c1c8e-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="c1c8e-110">userDefined</span></span>|<span data-ttu-id="c1c8e-111">0</span><span class="sxs-lookup"><span data-stu-id="c1c8e-111">0</span></span>|<span data-ttu-id="c1c8e-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-112">Allow the user to set.</span></span>|
|<span data-ttu-id="c1c8e-113">httpOnly</span><span class="sxs-lookup"><span data-stu-id="c1c8e-113">httpOnly</span></span>|<span data-ttu-id="c1c8e-114">1</span><span class="sxs-lookup"><span data-stu-id="c1c8e-114">1</span></span>|<span data-ttu-id="c1c8e-115">HTTP sólo, sin interconexión</span><span class="sxs-lookup"><span data-stu-id="c1c8e-115">HTTP only, no peering</span></span>|
|<span data-ttu-id="c1c8e-116">httpWithPeeringNat</span><span class="sxs-lookup"><span data-stu-id="c1c8e-116">httpWithPeeringNat</span></span>|<span data-ttu-id="c1c8e-117">2</span><span class="sxs-lookup"><span data-stu-id="c1c8e-117">2</span></span>|<span data-ttu-id="c1c8e-118">Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red</span><span class="sxs-lookup"><span data-stu-id="c1c8e-118">OS default – Http blended with peering behind the same network address translator</span></span>|
|<span data-ttu-id="c1c8e-119">httpWithPeeringPrivateGroup</span><span class="sxs-lookup"><span data-stu-id="c1c8e-119">httpWithPeeringPrivateGroup</span></span>|<span data-ttu-id="c1c8e-120">3</span><span class="sxs-lookup"><span data-stu-id="c1c8e-120">3</span></span>|<span data-ttu-id="c1c8e-121">Mezcla de HTTP con interconexión a través de un grupo privado</span><span class="sxs-lookup"><span data-stu-id="c1c8e-121">HTTP blended with peering across a private group</span></span>|
|<span data-ttu-id="c1c8e-122">httpWithInternetPeering</span><span class="sxs-lookup"><span data-stu-id="c1c8e-122">httpWithInternetPeering</span></span>|<span data-ttu-id="c1c8e-123">4</span><span class="sxs-lookup"><span data-stu-id="c1c8e-123">4</span></span>|<span data-ttu-id="c1c8e-124">HTTP mezclado con interconexión de Internet</span><span class="sxs-lookup"><span data-stu-id="c1c8e-124">HTTP blended with Internet peering</span></span>|
|<span data-ttu-id="c1c8e-125">simpleDownload</span><span class="sxs-lookup"><span data-stu-id="c1c8e-125">simpleDownload</span></span>|<span data-ttu-id="c1c8e-126">99</span><span class="sxs-lookup"><span data-stu-id="c1c8e-126">99</span></span>|<span data-ttu-id="c1c8e-127">Modo de descarga simple con ningún interconexión</span><span class="sxs-lookup"><span data-stu-id="c1c8e-127">Simple download mode with no peering</span></span>|
|<span data-ttu-id="c1c8e-128">bypassMode</span><span class="sxs-lookup"><span data-stu-id="c1c8e-128">bypassMode</span></span>|<span data-ttu-id="c1c8e-129">100</span><span class="sxs-lookup"><span data-stu-id="c1c8e-129">100</span></span>|<span data-ttu-id="c1c8e-130">Modo de derivación.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-130">Bypass mode.</span></span> <span data-ttu-id="c1c8e-131">No use la optimización de entrega y usar BITS en su lugar</span><span class="sxs-lookup"><span data-stu-id="c1c8e-131">Do not use Delivery Optimization and use BITS instead</span></span>|



