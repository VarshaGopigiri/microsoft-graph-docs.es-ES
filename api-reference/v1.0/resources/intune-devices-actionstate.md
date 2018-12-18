---
title: tipo de enumeración actionState
description: Estado de la acción en el dispositivo
author: tfitzmac
ms.openlocfilehash: 53ee72430ac646bf978a3167b87feaf398c8ac37
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333386"
---
# <a name="actionstate-enum-type"></a><span data-ttu-id="d6aa0-103">tipo de enumeración actionState</span><span class="sxs-lookup"><span data-stu-id="d6aa0-103">actionState enum type</span></span>

> <span data-ttu-id="d6aa0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d6aa0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d6aa0-105">Estado de la acción en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="d6aa0-105">State of the action on the device</span></span>
## <a name="members"></a><span data-ttu-id="d6aa0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6aa0-106">Members</span></span>
|<span data-ttu-id="d6aa0-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d6aa0-107">Member</span></span>|<span data-ttu-id="d6aa0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d6aa0-108">Value</span></span>|<span data-ttu-id="d6aa0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6aa0-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d6aa0-110">ninguno</span><span class="sxs-lookup"><span data-stu-id="d6aa0-110">none</span></span>|<span data-ttu-id="d6aa0-111">0</span><span class="sxs-lookup"><span data-stu-id="d6aa0-111">0</span></span>|<span data-ttu-id="d6aa0-112">No es un estado de acción válido</span><span class="sxs-lookup"><span data-stu-id="d6aa0-112">Not a valid action state</span></span>|
|<span data-ttu-id="d6aa0-113">pendiente</span><span class="sxs-lookup"><span data-stu-id="d6aa0-113">pending</span></span>|<span data-ttu-id="d6aa0-114">1</span><span class="sxs-lookup"><span data-stu-id="d6aa0-114">1</span></span>|<span data-ttu-id="d6aa0-115">La acción es pendiente</span><span class="sxs-lookup"><span data-stu-id="d6aa0-115">Action is pending</span></span>|
|<span data-ttu-id="d6aa0-116">Cancelar</span><span class="sxs-lookup"><span data-stu-id="d6aa0-116">canceled</span></span>|<span data-ttu-id="d6aa0-117">2</span><span class="sxs-lookup"><span data-stu-id="d6aa0-117">2</span></span>|<span data-ttu-id="d6aa0-118">Se ha cancelado la acción.</span><span class="sxs-lookup"><span data-stu-id="d6aa0-118">Action has been cancelled.</span></span>|
|<span data-ttu-id="d6aa0-119">activo</span><span class="sxs-lookup"><span data-stu-id="d6aa0-119">active</span></span>|<span data-ttu-id="d6aa0-120">3</span><span class="sxs-lookup"><span data-stu-id="d6aa0-120">3</span></span>|<span data-ttu-id="d6aa0-121">Acción está activa.</span><span class="sxs-lookup"><span data-stu-id="d6aa0-121">Action is active.</span></span>|
|<span data-ttu-id="d6aa0-122">done</span><span class="sxs-lookup"><span data-stu-id="d6aa0-122">done</span></span>|<span data-ttu-id="d6aa0-123">4</span><span class="sxs-lookup"><span data-stu-id="d6aa0-123">4</span></span>|<span data-ttu-id="d6aa0-124">Acción realizada sin errores.</span><span class="sxs-lookup"><span data-stu-id="d6aa0-124">Action completed without errors.</span></span>|
|<span data-ttu-id="d6aa0-125">failed</span><span class="sxs-lookup"><span data-stu-id="d6aa0-125">failed</span></span>|<span data-ttu-id="d6aa0-126">5</span><span class="sxs-lookup"><span data-stu-id="d6aa0-126">5</span></span>|<span data-ttu-id="d6aa0-127">Error en la acción</span><span class="sxs-lookup"><span data-stu-id="d6aa0-127">Action failed</span></span>|
|<span data-ttu-id="d6aa0-128">notSupported</span><span class="sxs-lookup"><span data-stu-id="d6aa0-128">notSupported</span></span>|<span data-ttu-id="d6aa0-129">6</span><span class="sxs-lookup"><span data-stu-id="d6aa0-129">6</span></span>|<span data-ttu-id="d6aa0-130">No se admite la acción.</span><span class="sxs-lookup"><span data-stu-id="d6aa0-130">Action is not supported.</span></span>|



