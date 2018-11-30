---
title: tipo de enumeración actionState
description: Estado de la acción en el dispositivo
ms.openlocfilehash: 1a18eb87cb4c9162777d16dc866de5f5766c87b1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032120"
---
# <a name="actionstate-enum-type"></a><span data-ttu-id="9505b-103">tipo de enumeración actionState</span><span class="sxs-lookup"><span data-stu-id="9505b-103">actionState enum type</span></span>

> <span data-ttu-id="9505b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9505b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9505b-105">Estado de la acción en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="9505b-105">State of the action on the device</span></span>
## <a name="members"></a><span data-ttu-id="9505b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9505b-106">Members</span></span>
|<span data-ttu-id="9505b-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="9505b-107">Member</span></span>|<span data-ttu-id="9505b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="9505b-108">Value</span></span>|<span data-ttu-id="9505b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9505b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9505b-110">ninguno</span><span class="sxs-lookup"><span data-stu-id="9505b-110">none</span></span>|<span data-ttu-id="9505b-111">0</span><span class="sxs-lookup"><span data-stu-id="9505b-111">0</span></span>|<span data-ttu-id="9505b-112">No es un estado de acción válido</span><span class="sxs-lookup"><span data-stu-id="9505b-112">Not a valid action state</span></span>|
|<span data-ttu-id="9505b-113">pendiente</span><span class="sxs-lookup"><span data-stu-id="9505b-113">pending</span></span>|<span data-ttu-id="9505b-114">1</span><span class="sxs-lookup"><span data-stu-id="9505b-114">1</span></span>|<span data-ttu-id="9505b-115">La acción es pendiente</span><span class="sxs-lookup"><span data-stu-id="9505b-115">Action is pending</span></span>|
|<span data-ttu-id="9505b-116">Cancelar</span><span class="sxs-lookup"><span data-stu-id="9505b-116">canceled</span></span>|<span data-ttu-id="9505b-117">2</span><span class="sxs-lookup"><span data-stu-id="9505b-117">2</span></span>|<span data-ttu-id="9505b-118">Se ha cancelado la acción.</span><span class="sxs-lookup"><span data-stu-id="9505b-118">Action has been cancelled.</span></span>|
|<span data-ttu-id="9505b-119">activo</span><span class="sxs-lookup"><span data-stu-id="9505b-119">active</span></span>|<span data-ttu-id="9505b-120">3</span><span class="sxs-lookup"><span data-stu-id="9505b-120">3</span></span>|<span data-ttu-id="9505b-121">Acción está activa.</span><span class="sxs-lookup"><span data-stu-id="9505b-121">Action is active.</span></span>|
|<span data-ttu-id="9505b-122">done</span><span class="sxs-lookup"><span data-stu-id="9505b-122">done</span></span>|<span data-ttu-id="9505b-123">4</span><span class="sxs-lookup"><span data-stu-id="9505b-123">4</span></span>|<span data-ttu-id="9505b-124">Acción realizada sin errores.</span><span class="sxs-lookup"><span data-stu-id="9505b-124">Action completed without errors.</span></span>|
|<span data-ttu-id="9505b-125">failed</span><span class="sxs-lookup"><span data-stu-id="9505b-125">failed</span></span>|<span data-ttu-id="9505b-126">5</span><span class="sxs-lookup"><span data-stu-id="9505b-126">5</span></span>|<span data-ttu-id="9505b-127">Error en la acción</span><span class="sxs-lookup"><span data-stu-id="9505b-127">Action failed</span></span>|
|<span data-ttu-id="9505b-128">notSupported</span><span class="sxs-lookup"><span data-stu-id="9505b-128">notSupported</span></span>|<span data-ttu-id="9505b-129">6</span><span class="sxs-lookup"><span data-stu-id="9505b-129">6</span></span>|<span data-ttu-id="9505b-130">No se admite la acción.</span><span class="sxs-lookup"><span data-stu-id="9505b-130">Action is not supported.</span></span>|


