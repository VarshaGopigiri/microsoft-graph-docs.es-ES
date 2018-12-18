---
title: tipo de enumeración windowsDeliveryOptimizationMode
description: Modo de optimización de entrega para la distribución del mismo nivel
author: tfitzmac
ms.openlocfilehash: ae61d7dde5fc02ff329eaf9cc970ee7078c3a254
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360161"
---
# <a name="windowsdeliveryoptimizationmode-enum-type"></a><span data-ttu-id="77157-103">tipo de enumeración windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="77157-103">windowsDeliveryOptimizationMode enum type</span></span>

> <span data-ttu-id="77157-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="77157-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="77157-105">Modo de optimización de entrega para la distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="77157-105">Delivery optimization mode for peer distribution</span></span>
## <a name="members"></a><span data-ttu-id="77157-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="77157-106">Members</span></span>
|<span data-ttu-id="77157-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="77157-107">Member</span></span>|<span data-ttu-id="77157-108">Valor</span><span class="sxs-lookup"><span data-stu-id="77157-108">Value</span></span>|<span data-ttu-id="77157-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="77157-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="77157-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="77157-110">userDefined</span></span>|<span data-ttu-id="77157-111">0</span><span class="sxs-lookup"><span data-stu-id="77157-111">0</span></span>|<span data-ttu-id="77157-112">Permitir al usuario que establezca.</span><span class="sxs-lookup"><span data-stu-id="77157-112">Allow the user to set.</span></span>|
|<span data-ttu-id="77157-113">httpOnly</span><span class="sxs-lookup"><span data-stu-id="77157-113">httpOnly</span></span>|<span data-ttu-id="77157-114">1</span><span class="sxs-lookup"><span data-stu-id="77157-114">1</span></span>|<span data-ttu-id="77157-115">HTTP sólo, sin interconexión</span><span class="sxs-lookup"><span data-stu-id="77157-115">HTTP only, no peering</span></span>|
|<span data-ttu-id="77157-116">httpWithPeeringNat</span><span class="sxs-lookup"><span data-stu-id="77157-116">httpWithPeeringNat</span></span>|<span data-ttu-id="77157-117">2</span><span class="sxs-lookup"><span data-stu-id="77157-117">2</span></span>|<span data-ttu-id="77157-118">Predeterminado del sistema operativo – Http mezcla con interconexión detrás de la misma traductor de direcciones de red</span><span class="sxs-lookup"><span data-stu-id="77157-118">OS default – Http blended with peering behind the same network address translator</span></span>|
|<span data-ttu-id="77157-119">httpWithPeeringPrivateGroup</span><span class="sxs-lookup"><span data-stu-id="77157-119">httpWithPeeringPrivateGroup</span></span>|<span data-ttu-id="77157-120">3</span><span class="sxs-lookup"><span data-stu-id="77157-120">3</span></span>|<span data-ttu-id="77157-121">Mezcla de HTTP con interconexión a través de un grupo privado</span><span class="sxs-lookup"><span data-stu-id="77157-121">HTTP blended with peering across a private group</span></span>|
|<span data-ttu-id="77157-122">httpWithInternetPeering</span><span class="sxs-lookup"><span data-stu-id="77157-122">httpWithInternetPeering</span></span>|<span data-ttu-id="77157-123">4</span><span class="sxs-lookup"><span data-stu-id="77157-123">4</span></span>|<span data-ttu-id="77157-124">HTTP mezclado con interconexión de Internet</span><span class="sxs-lookup"><span data-stu-id="77157-124">HTTP blended with Internet peering</span></span>|
|<span data-ttu-id="77157-125">simpleDownload</span><span class="sxs-lookup"><span data-stu-id="77157-125">simpleDownload</span></span>|<span data-ttu-id="77157-126">99</span><span class="sxs-lookup"><span data-stu-id="77157-126">99</span></span>|<span data-ttu-id="77157-127">Modo de descarga simple con ningún interconexión</span><span class="sxs-lookup"><span data-stu-id="77157-127">Simple download mode with no peering</span></span>|
|<span data-ttu-id="77157-128">bypassMode</span><span class="sxs-lookup"><span data-stu-id="77157-128">bypassMode</span></span>|<span data-ttu-id="77157-129">100</span><span class="sxs-lookup"><span data-stu-id="77157-129">100</span></span>|<span data-ttu-id="77157-130">Modo de derivación.</span><span class="sxs-lookup"><span data-stu-id="77157-130">Bypass mode.</span></span> <span data-ttu-id="77157-131">No use la optimización de entrega y usar BITS en su lugar</span><span class="sxs-lookup"><span data-stu-id="77157-131">Do not use Delivery Optimization and use BITS instead</span></span>|



