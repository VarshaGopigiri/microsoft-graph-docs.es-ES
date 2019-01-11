---
title: tipo de enumeración actionState
description: Estado de la acción en el dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c0c05e283b94473a5c8c43498ff5bf1dd82da7a5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871942"
---
# <a name="actionstate-enum-type"></a><span data-ttu-id="4a99a-103">tipo de enumeración actionState</span><span class="sxs-lookup"><span data-stu-id="4a99a-103">actionState enum type</span></span>

> <span data-ttu-id="4a99a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a99a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a99a-105">Estado de la acción en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="4a99a-105">State of the action on the device</span></span>
## <a name="members"></a><span data-ttu-id="4a99a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a99a-106">Members</span></span>
|<span data-ttu-id="4a99a-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="4a99a-107">Member</span></span>|<span data-ttu-id="4a99a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4a99a-108">Value</span></span>|<span data-ttu-id="4a99a-109">Description</span><span class="sxs-lookup"><span data-stu-id="4a99a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a99a-110">none</span><span class="sxs-lookup"><span data-stu-id="4a99a-110">none</span></span>|<span data-ttu-id="4a99a-111">0</span><span class="sxs-lookup"><span data-stu-id="4a99a-111">0</span></span>|<span data-ttu-id="4a99a-112">No es un estado de acción válido</span><span class="sxs-lookup"><span data-stu-id="4a99a-112">Not a valid action state</span></span>|
|<span data-ttu-id="4a99a-113">pendiente</span><span class="sxs-lookup"><span data-stu-id="4a99a-113">pending</span></span>|<span data-ttu-id="4a99a-114">1</span><span class="sxs-lookup"><span data-stu-id="4a99a-114">1</span></span>|<span data-ttu-id="4a99a-115">La acción es pendiente</span><span class="sxs-lookup"><span data-stu-id="4a99a-115">Action is pending</span></span>|
|<span data-ttu-id="4a99a-116">Cancelar</span><span class="sxs-lookup"><span data-stu-id="4a99a-116">canceled</span></span>|<span data-ttu-id="4a99a-117">2</span><span class="sxs-lookup"><span data-stu-id="4a99a-117">2</span></span>|<span data-ttu-id="4a99a-118">Se ha cancelado la acción.</span><span class="sxs-lookup"><span data-stu-id="4a99a-118">Action has been cancelled.</span></span>|
|<span data-ttu-id="4a99a-119">activo</span><span class="sxs-lookup"><span data-stu-id="4a99a-119">active</span></span>|<span data-ttu-id="4a99a-120">3</span><span class="sxs-lookup"><span data-stu-id="4a99a-120">3</span></span>|<span data-ttu-id="4a99a-121">Acción está activa.</span><span class="sxs-lookup"><span data-stu-id="4a99a-121">Action is active.</span></span>|
|<span data-ttu-id="4a99a-122">done</span><span class="sxs-lookup"><span data-stu-id="4a99a-122">done</span></span>|<span data-ttu-id="4a99a-123">4</span><span class="sxs-lookup"><span data-stu-id="4a99a-123">4</span></span>|<span data-ttu-id="4a99a-124">Acción realizada sin errores.</span><span class="sxs-lookup"><span data-stu-id="4a99a-124">Action completed without errors.</span></span>|
|<span data-ttu-id="4a99a-125">failed</span><span class="sxs-lookup"><span data-stu-id="4a99a-125">failed</span></span>|<span data-ttu-id="4a99a-126">5</span><span class="sxs-lookup"><span data-stu-id="4a99a-126">5</span></span>|<span data-ttu-id="4a99a-127">Error en la acción</span><span class="sxs-lookup"><span data-stu-id="4a99a-127">Action failed</span></span>|
|<span data-ttu-id="4a99a-128">notSupported</span><span class="sxs-lookup"><span data-stu-id="4a99a-128">notSupported</span></span>|<span data-ttu-id="4a99a-129">6</span><span class="sxs-lookup"><span data-stu-id="4a99a-129">6</span></span>|<span data-ttu-id="4a99a-130">No se admite la acción.</span><span class="sxs-lookup"><span data-stu-id="4a99a-130">Action is not supported.</span></span>|



