---
title: tipo de enumeración actionState
description: Estado de la acción en el dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: af8bb3869171faee5907b4a3f1921bcb70044aec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829907"
---
# <a name="actionstate-enum-type"></a><span data-ttu-id="37965-103">tipo de enumeración actionState</span><span class="sxs-lookup"><span data-stu-id="37965-103">actionState enum type</span></span>

> <span data-ttu-id="37965-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37965-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37965-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37965-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37965-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37965-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37965-107">Estado de la acción en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="37965-107">State of the action on the device</span></span>
## <a name="members"></a><span data-ttu-id="37965-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="37965-108">Members</span></span>
|<span data-ttu-id="37965-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="37965-109">Member</span></span>|<span data-ttu-id="37965-110">Valor</span><span class="sxs-lookup"><span data-stu-id="37965-110">Value</span></span>|<span data-ttu-id="37965-111">Description</span><span class="sxs-lookup"><span data-stu-id="37965-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37965-112">none</span><span class="sxs-lookup"><span data-stu-id="37965-112">none</span></span>|<span data-ttu-id="37965-113">0</span><span class="sxs-lookup"><span data-stu-id="37965-113">0</span></span>|<span data-ttu-id="37965-114">No es un estado de acción válido</span><span class="sxs-lookup"><span data-stu-id="37965-114">Not a valid action state</span></span>|
|<span data-ttu-id="37965-115">pendiente</span><span class="sxs-lookup"><span data-stu-id="37965-115">pending</span></span>|<span data-ttu-id="37965-116">1</span><span class="sxs-lookup"><span data-stu-id="37965-116">1</span></span>|<span data-ttu-id="37965-117">La acción es pendiente</span><span class="sxs-lookup"><span data-stu-id="37965-117">Action is pending</span></span>|
|<span data-ttu-id="37965-118">Cancelar</span><span class="sxs-lookup"><span data-stu-id="37965-118">canceled</span></span>|<span data-ttu-id="37965-119">2</span><span class="sxs-lookup"><span data-stu-id="37965-119">2</span></span>|<span data-ttu-id="37965-120">Se ha cancelado la acción.</span><span class="sxs-lookup"><span data-stu-id="37965-120">Action has been cancelled.</span></span>|
|<span data-ttu-id="37965-121">activo</span><span class="sxs-lookup"><span data-stu-id="37965-121">active</span></span>|<span data-ttu-id="37965-122">3</span><span class="sxs-lookup"><span data-stu-id="37965-122">3</span></span>|<span data-ttu-id="37965-123">Acción está activa.</span><span class="sxs-lookup"><span data-stu-id="37965-123">Action is active.</span></span>|
|<span data-ttu-id="37965-124">done</span><span class="sxs-lookup"><span data-stu-id="37965-124">done</span></span>|<span data-ttu-id="37965-125">4</span><span class="sxs-lookup"><span data-stu-id="37965-125">4</span></span>|<span data-ttu-id="37965-126">Acción realizada sin errores.</span><span class="sxs-lookup"><span data-stu-id="37965-126">Action completed without errors.</span></span>|
|<span data-ttu-id="37965-127">failed</span><span class="sxs-lookup"><span data-stu-id="37965-127">failed</span></span>|<span data-ttu-id="37965-128">5</span><span class="sxs-lookup"><span data-stu-id="37965-128">5</span></span>|<span data-ttu-id="37965-129">Error en la acción</span><span class="sxs-lookup"><span data-stu-id="37965-129">Action failed</span></span>|
|<span data-ttu-id="37965-130">notSupported</span><span class="sxs-lookup"><span data-stu-id="37965-130">notSupported</span></span>|<span data-ttu-id="37965-131">6</span><span class="sxs-lookup"><span data-stu-id="37965-131">6</span></span>|<span data-ttu-id="37965-132">No se admite la acción.</span><span class="sxs-lookup"><span data-stu-id="37965-132">Action is not supported.</span></span>|





