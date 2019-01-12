---
title: tipo de enumeración actionState
description: Estado de la acción en el dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5579d8de986a764cd96e42dff30c007449130b0b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922448"
---
# <a name="actionstate-enum-type"></a><span data-ttu-id="a190c-103">tipo de enumeración actionState</span><span class="sxs-lookup"><span data-stu-id="a190c-103">actionState enum type</span></span>

> <span data-ttu-id="a190c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a190c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a190c-105">Estado de la acción en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="a190c-105">State of the action on the device</span></span>
## <a name="members"></a><span data-ttu-id="a190c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a190c-106">Members</span></span>
|<span data-ttu-id="a190c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a190c-107">Member</span></span>|<span data-ttu-id="a190c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a190c-108">Value</span></span>|<span data-ttu-id="a190c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a190c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a190c-110">none</span><span class="sxs-lookup"><span data-stu-id="a190c-110">none</span></span>|<span data-ttu-id="a190c-111">0</span><span class="sxs-lookup"><span data-stu-id="a190c-111">0</span></span>|<span data-ttu-id="a190c-112">No es un estado de acción válido</span><span class="sxs-lookup"><span data-stu-id="a190c-112">Not a valid action state</span></span>|
|<span data-ttu-id="a190c-113">pendiente</span><span class="sxs-lookup"><span data-stu-id="a190c-113">pending</span></span>|<span data-ttu-id="a190c-114">1</span><span class="sxs-lookup"><span data-stu-id="a190c-114">1</span></span>|<span data-ttu-id="a190c-115">La acción es pendiente</span><span class="sxs-lookup"><span data-stu-id="a190c-115">Action is pending</span></span>|
|<span data-ttu-id="a190c-116">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a190c-116">canceled</span></span>|<span data-ttu-id="a190c-117">2</span><span class="sxs-lookup"><span data-stu-id="a190c-117">2</span></span>|<span data-ttu-id="a190c-118">Se ha cancelado la acción.</span><span class="sxs-lookup"><span data-stu-id="a190c-118">Action has been cancelled.</span></span>|
|<span data-ttu-id="a190c-119">activo</span><span class="sxs-lookup"><span data-stu-id="a190c-119">active</span></span>|<span data-ttu-id="a190c-120">3</span><span class="sxs-lookup"><span data-stu-id="a190c-120">3</span></span>|<span data-ttu-id="a190c-121">Acción está activa.</span><span class="sxs-lookup"><span data-stu-id="a190c-121">Action is active.</span></span>|
|<span data-ttu-id="a190c-122">done</span><span class="sxs-lookup"><span data-stu-id="a190c-122">done</span></span>|<span data-ttu-id="a190c-123">4</span><span class="sxs-lookup"><span data-stu-id="a190c-123">4</span></span>|<span data-ttu-id="a190c-124">Acción realizada sin errores.</span><span class="sxs-lookup"><span data-stu-id="a190c-124">Action completed without errors.</span></span>|
|<span data-ttu-id="a190c-125">failed</span><span class="sxs-lookup"><span data-stu-id="a190c-125">failed</span></span>|<span data-ttu-id="a190c-126">5</span><span class="sxs-lookup"><span data-stu-id="a190c-126">5</span></span>|<span data-ttu-id="a190c-127">Error en la acción</span><span class="sxs-lookup"><span data-stu-id="a190c-127">Action failed</span></span>|
|<span data-ttu-id="a190c-128">notSupported</span><span class="sxs-lookup"><span data-stu-id="a190c-128">notSupported</span></span>|<span data-ttu-id="a190c-129">6</span><span class="sxs-lookup"><span data-stu-id="a190c-129">6</span></span>|<span data-ttu-id="a190c-130">No se admite la acción.</span><span class="sxs-lookup"><span data-stu-id="a190c-130">Action is not supported.</span></span>|



