---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
ms.openlocfilehash: 2d393a82f855f3e3a0226c8ccb450fa2dae1a95c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029987"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a><span data-ttu-id="aba36-103">tipo de enumeración windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="aba36-103">windowsDeliveryOptimizationMode enum type</span></span>

> <span data-ttu-id="aba36-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aba36-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aba36-105">Modo de optimización de entrega para la distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="aba36-105">Delivery optimization mode for peer distribution</span></span>
## <a name="members"></a><span data-ttu-id="aba36-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="aba36-106">Members</span></span>
|<span data-ttu-id="aba36-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="aba36-107">Member</span></span>|<span data-ttu-id="aba36-108">Valor</span><span class="sxs-lookup"><span data-stu-id="aba36-108">Value</span></span>|<span data-ttu-id="aba36-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="aba36-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aba36-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="aba36-110">userDefined</span></span>|<span data-ttu-id="aba36-111">0</span><span class="sxs-lookup"><span data-stu-id="aba36-111">0</span></span>|<span data-ttu-id="aba36-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="aba36-112">Allow the user to set.</span></span>|
|<span data-ttu-id="aba36-113">httpOnly</span><span class="sxs-lookup"><span data-stu-id="aba36-113">httpOnly</span></span>|<span data-ttu-id="aba36-114">1</span><span class="sxs-lookup"><span data-stu-id="aba36-114">1</span></span>|<span data-ttu-id="aba36-115">HTTP sólo, sin interconexión</span><span class="sxs-lookup"><span data-stu-id="aba36-115">HTTP only, no peering</span></span>|
|<span data-ttu-id="aba36-116">httpWithPeeringNat</span><span class="sxs-lookup"><span data-stu-id="aba36-116">httpWithPeeringNat</span></span>|<span data-ttu-id="aba36-117">2</span><span class="sxs-lookup"><span data-stu-id="aba36-117">2</span></span>|<span data-ttu-id="aba36-118">Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red</span><span class="sxs-lookup"><span data-stu-id="aba36-118">OS default – Http blended with peering behind the same network address translator</span></span>|
|<span data-ttu-id="aba36-119">httpWithPeeringPrivateGroup</span><span class="sxs-lookup"><span data-stu-id="aba36-119">httpWithPeeringPrivateGroup</span></span>|<span data-ttu-id="aba36-120">3</span><span class="sxs-lookup"><span data-stu-id="aba36-120">3</span></span>|<span data-ttu-id="aba36-121">Mezcla de HTTP con interconexión a través de un grupo privado</span><span class="sxs-lookup"><span data-stu-id="aba36-121">HTTP blended with peering across a private group</span></span>|
|<span data-ttu-id="aba36-122">httpWithInternetPeering</span><span class="sxs-lookup"><span data-stu-id="aba36-122">httpWithInternetPeering</span></span>|<span data-ttu-id="aba36-123">4</span><span class="sxs-lookup"><span data-stu-id="aba36-123">4</span></span>|<span data-ttu-id="aba36-124">HTTP mezclado con interconexión de Internet</span><span class="sxs-lookup"><span data-stu-id="aba36-124">HTTP blended with Internet peering</span></span>|
|<span data-ttu-id="aba36-125">simpleDownload</span><span class="sxs-lookup"><span data-stu-id="aba36-125">simpleDownload</span></span>|<span data-ttu-id="aba36-126">99</span><span class="sxs-lookup"><span data-stu-id="aba36-126">99</span></span>|<span data-ttu-id="aba36-127">Modo de descarga simple con ningún interconexión</span><span class="sxs-lookup"><span data-stu-id="aba36-127">Simple download mode with no peering</span></span>|
|<span data-ttu-id="aba36-128">bypassMode</span><span class="sxs-lookup"><span data-stu-id="aba36-128">bypassMode</span></span>|<span data-ttu-id="aba36-129">100</span><span class="sxs-lookup"><span data-stu-id="aba36-129">100</span></span>|<span data-ttu-id="aba36-130">Modo de derivación.</span><span class="sxs-lookup"><span data-stu-id="aba36-130">Bypass mode.</span></span> <span data-ttu-id="aba36-131">No use la optimización de entrega y usar BITS en su lugar</span><span class="sxs-lookup"><span data-stu-id="aba36-131">Do not use Delivery Optimization and use BITS instead</span></span>|



