---
title: tipo de enumeración managementState
description: Estado de administración de dispositivos en Microsoft Intune.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7d9d083c56df366b9f896432328d51c295f62190
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961949"
---
# <a name="managementstate-enum-type"></a><span data-ttu-id="c2f3d-103">tipo de enumeración managementState</span><span class="sxs-lookup"><span data-stu-id="c2f3d-103">managementState enum type</span></span>

> <span data-ttu-id="c2f3d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2f3d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2f3d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2f3d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c2f3d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2f3d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2f3d-107">Estado de administración de dispositivos en Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="c2f3d-107">Management state of device in Microsoft Intune.</span></span>
## <a name="members"></a><span data-ttu-id="c2f3d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2f3d-108">Members</span></span>
|<span data-ttu-id="c2f3d-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="c2f3d-109">Member</span></span>|<span data-ttu-id="c2f3d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c2f3d-110">Value</span></span>|<span data-ttu-id="c2f3d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2f3d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2f3d-112">administrado</span><span class="sxs-lookup"><span data-stu-id="c2f3d-112">managed</span></span>|<span data-ttu-id="c2f3d-113">0</span><span class="sxs-lookup"><span data-stu-id="c2f3d-113">0</span></span>|<span data-ttu-id="c2f3d-114">El dispositivo está bajo administración</span><span class="sxs-lookup"><span data-stu-id="c2f3d-114">The device is under management</span></span>|
|<span data-ttu-id="c2f3d-115">retirePending</span><span class="sxs-lookup"><span data-stu-id="c2f3d-115">retirePending</span></span>|<span data-ttu-id="c2f3d-116">1</span><span class="sxs-lookup"><span data-stu-id="c2f3d-116">1</span></span>|<span data-ttu-id="c2f3d-117">Un comando de retirada se está produciendo en el dispositivo y en el proceso de unenrolling de administración</span><span class="sxs-lookup"><span data-stu-id="c2f3d-117">A retire command is occuring on the device and in the process of unenrolling from management</span></span>|
|<span data-ttu-id="c2f3d-118">retireFailed</span><span class="sxs-lookup"><span data-stu-id="c2f3d-118">retireFailed</span></span>|<span data-ttu-id="c2f3d-119">2</span><span class="sxs-lookup"><span data-stu-id="c2f3d-119">2</span></span>|<span data-ttu-id="c2f3d-120">Error en el dispositivo en el comando de retirada</span><span class="sxs-lookup"><span data-stu-id="c2f3d-120">Retire command failed on the device</span></span>|
|<span data-ttu-id="c2f3d-121">wipePending</span><span class="sxs-lookup"><span data-stu-id="c2f3d-121">wipePending</span></span>|<span data-ttu-id="c2f3d-122">3</span><span class="sxs-lookup"><span data-stu-id="c2f3d-122">3</span></span>|<span data-ttu-id="c2f3d-123">Un comando de barrido se está produciendo en el dispositivo y en el proceso de unenrolling de administración</span><span class="sxs-lookup"><span data-stu-id="c2f3d-123">A wipe command is occuring on the device and in the process of unenrolling from management</span></span>|
|<span data-ttu-id="c2f3d-124">wipeFailed</span><span class="sxs-lookup"><span data-stu-id="c2f3d-124">wipeFailed</span></span>|<span data-ttu-id="c2f3d-125">4</span><span class="sxs-lookup"><span data-stu-id="c2f3d-125">4</span></span>|<span data-ttu-id="c2f3d-126">Error en el comando de barrido en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2f3d-126">Wipe command failed on the device</span></span>|
|<span data-ttu-id="c2f3d-127">mal estado</span><span class="sxs-lookup"><span data-stu-id="c2f3d-127">unhealthy</span></span>|<span data-ttu-id="c2f3d-128">5</span><span class="sxs-lookup"><span data-stu-id="c2f3d-128">5</span></span>|<span data-ttu-id="c2f3d-129">El dispositivo tiene un estado incorrecto.</span><span class="sxs-lookup"><span data-stu-id="c2f3d-129">The device is unhealthy.</span></span>|
|<span data-ttu-id="c2f3d-130">deletePending</span><span class="sxs-lookup"><span data-stu-id="c2f3d-130">deletePending</span></span>|<span data-ttu-id="c2f3d-131">6</span><span class="sxs-lookup"><span data-stu-id="c2f3d-131">6</span></span>|<span data-ttu-id="c2f3d-132">Un comando de eliminación se está produciendo en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2f3d-132">A delete command is occuring on the device</span></span> |
|<span data-ttu-id="c2f3d-133">retireIssued</span><span class="sxs-lookup"><span data-stu-id="c2f3d-133">retireIssued</span></span>|<span data-ttu-id="c2f3d-134">7</span><span class="sxs-lookup"><span data-stu-id="c2f3d-134">7</span></span>|<span data-ttu-id="c2f3d-135">Un comando de retirada se ha emitido para el dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2f3d-135">A retire command was issued for the device</span></span>|
|<span data-ttu-id="c2f3d-136">wipeIssued</span><span class="sxs-lookup"><span data-stu-id="c2f3d-136">wipeIssued</span></span>|<span data-ttu-id="c2f3d-137">8</span><span class="sxs-lookup"><span data-stu-id="c2f3d-137">8</span></span>|<span data-ttu-id="c2f3d-138">Se emitió un comando de barrido del dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2f3d-138">A wipe command was issued for the device</span></span>|
|<span data-ttu-id="c2f3d-139">wipeCanceled</span><span class="sxs-lookup"><span data-stu-id="c2f3d-139">wipeCanceled</span></span>|<span data-ttu-id="c2f3d-140">9</span><span class="sxs-lookup"><span data-stu-id="c2f3d-140">9</span></span>|<span data-ttu-id="c2f3d-141">Se ha cancelado un comando de barrido para este dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2f3d-141">A wipe command for this device has been canceled</span></span>|
|<span data-ttu-id="c2f3d-142">retireCanceled</span><span class="sxs-lookup"><span data-stu-id="c2f3d-142">retireCanceled</span></span>|<span data-ttu-id="c2f3d-143">10</span><span class="sxs-lookup"><span data-stu-id="c2f3d-143">10</span></span>|<span data-ttu-id="c2f3d-144">Se ha cancelado un comando de retirada para este dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2f3d-144">A retire command for this device has been canceled</span></span>|
|<span data-ttu-id="c2f3d-145">detectado</span><span class="sxs-lookup"><span data-stu-id="c2f3d-145">discovered</span></span>|<span data-ttu-id="c2f3d-146">11</span><span class="sxs-lookup"><span data-stu-id="c2f3d-146">11</span></span>|<span data-ttu-id="c2f3d-147">El dispositivo es detectado pero suscrito no completamente.</span><span class="sxs-lookup"><span data-stu-id="c2f3d-147">The device is discovered but not fully enrolled.</span></span>|





