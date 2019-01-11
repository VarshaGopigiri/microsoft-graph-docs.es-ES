---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: af266b55fd58f788965d33d0d807511d263f6195
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888182"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a><span data-ttu-id="b48b0-103">tipo de enumeración windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="b48b0-103">windowsDeliveryOptimizationMode enum type</span></span>

> <span data-ttu-id="b48b0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b48b0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b48b0-105">Modo de optimización de entrega para la distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="b48b0-105">Delivery optimization mode for peer distribution</span></span>
## <a name="members"></a><span data-ttu-id="b48b0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b48b0-106">Members</span></span>
|<span data-ttu-id="b48b0-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b48b0-107">Member</span></span>|<span data-ttu-id="b48b0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b48b0-108">Value</span></span>|<span data-ttu-id="b48b0-109">Description</span><span class="sxs-lookup"><span data-stu-id="b48b0-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b48b0-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="b48b0-110">userDefined</span></span>|<span data-ttu-id="b48b0-111">0</span><span class="sxs-lookup"><span data-stu-id="b48b0-111">0</span></span>|<span data-ttu-id="b48b0-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="b48b0-112">Allow the user to set.</span></span>|
|<span data-ttu-id="b48b0-113">httpOnly</span><span class="sxs-lookup"><span data-stu-id="b48b0-113">httpOnly</span></span>|<span data-ttu-id="b48b0-114">1</span><span class="sxs-lookup"><span data-stu-id="b48b0-114">1</span></span>|<span data-ttu-id="b48b0-115">HTTP sólo, sin interconexión</span><span class="sxs-lookup"><span data-stu-id="b48b0-115">HTTP only, no peering</span></span>|
|<span data-ttu-id="b48b0-116">httpWithPeeringNat</span><span class="sxs-lookup"><span data-stu-id="b48b0-116">httpWithPeeringNat</span></span>|<span data-ttu-id="b48b0-117">2</span><span class="sxs-lookup"><span data-stu-id="b48b0-117">2</span></span>|<span data-ttu-id="b48b0-118">Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red</span><span class="sxs-lookup"><span data-stu-id="b48b0-118">OS default – Http blended with peering behind the same network address translator</span></span>|
|<span data-ttu-id="b48b0-119">httpWithPeeringPrivateGroup</span><span class="sxs-lookup"><span data-stu-id="b48b0-119">httpWithPeeringPrivateGroup</span></span>|<span data-ttu-id="b48b0-120">3</span><span class="sxs-lookup"><span data-stu-id="b48b0-120">3</span></span>|<span data-ttu-id="b48b0-121">Mezcla de HTTP con interconexión a través de un grupo privado</span><span class="sxs-lookup"><span data-stu-id="b48b0-121">HTTP blended with peering across a private group</span></span>|
|<span data-ttu-id="b48b0-122">httpWithInternetPeering</span><span class="sxs-lookup"><span data-stu-id="b48b0-122">httpWithInternetPeering</span></span>|<span data-ttu-id="b48b0-123">4</span><span class="sxs-lookup"><span data-stu-id="b48b0-123">4</span></span>|<span data-ttu-id="b48b0-124">HTTP mezclado con interconexión de Internet</span><span class="sxs-lookup"><span data-stu-id="b48b0-124">HTTP blended with Internet peering</span></span>|
|<span data-ttu-id="b48b0-125">simpleDownload</span><span class="sxs-lookup"><span data-stu-id="b48b0-125">simpleDownload</span></span>|<span data-ttu-id="b48b0-126">99</span><span class="sxs-lookup"><span data-stu-id="b48b0-126">99</span></span>|<span data-ttu-id="b48b0-127">Modo de descarga simple con ningún interconexión</span><span class="sxs-lookup"><span data-stu-id="b48b0-127">Simple download mode with no peering</span></span>|
|<span data-ttu-id="b48b0-128">bypassMode</span><span class="sxs-lookup"><span data-stu-id="b48b0-128">bypassMode</span></span>|<span data-ttu-id="b48b0-129">100</span><span class="sxs-lookup"><span data-stu-id="b48b0-129">100</span></span>|<span data-ttu-id="b48b0-130">Modo de derivación.</span><span class="sxs-lookup"><span data-stu-id="b48b0-130">Bypass mode.</span></span> <span data-ttu-id="b48b0-131">No use la optimización de entrega y usar BITS en su lugar</span><span class="sxs-lookup"><span data-stu-id="b48b0-131">Do not use Delivery Optimization and use BITS instead</span></span>|



