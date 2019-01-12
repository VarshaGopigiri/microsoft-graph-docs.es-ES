---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: fb54523f2817da328854e57a6672045e46ceb266
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938086"
---
# <a name="defenderthreataction-enum-type"></a><span data-ttu-id="1d982-103">tipo de enumeración defenderThreatAction</span><span class="sxs-lookup"><span data-stu-id="1d982-103">defenderThreatAction enum type</span></span>

> <span data-ttu-id="1d982-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d982-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d982-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d982-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d982-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d982-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d982-107">Acción de predeterminada del Defender tomar detecta las amenazas de Malware.</span><span class="sxs-lookup"><span data-stu-id="1d982-107">Defender’s default action to take on detected Malware threats.</span></span>
## <a name="members"></a><span data-ttu-id="1d982-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d982-108">Members</span></span>
|<span data-ttu-id="1d982-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="1d982-109">Member</span></span>|<span data-ttu-id="1d982-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1d982-110">Value</span></span>|<span data-ttu-id="1d982-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d982-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d982-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="1d982-112">deviceDefault</span></span>|<span data-ttu-id="1d982-113">0</span><span class="sxs-lookup"><span data-stu-id="1d982-113">0</span></span>|<span data-ttu-id="1d982-114">Aplicar la acción en función de la definición de actualización.</span><span class="sxs-lookup"><span data-stu-id="1d982-114">Apply action based on the update definition.</span></span>|
|<span data-ttu-id="1d982-115">clean</span><span class="sxs-lookup"><span data-stu-id="1d982-115">clean</span></span>|<span data-ttu-id="1d982-116">1</span><span class="sxs-lookup"><span data-stu-id="1d982-116">1</span></span>|<span data-ttu-id="1d982-117">Limpiar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="1d982-117">Clean the detected threat.</span></span>|
|<span data-ttu-id="1d982-118">cuarentena</span><span class="sxs-lookup"><span data-stu-id="1d982-118">quarantine</span></span>|<span data-ttu-id="1d982-119">2</span><span class="sxs-lookup"><span data-stu-id="1d982-119">2</span></span>|<span data-ttu-id="1d982-120">La amenaza detectada en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="1d982-120">Quarantine the detected threat.</span></span>|
|<span data-ttu-id="1d982-121">remove</span><span class="sxs-lookup"><span data-stu-id="1d982-121">remove</span></span>|<span data-ttu-id="1d982-122">3</span><span class="sxs-lookup"><span data-stu-id="1d982-122">3</span></span>|<span data-ttu-id="1d982-123">Quitar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="1d982-123">Remove the detected threat.</span></span>|
|<span data-ttu-id="1d982-124">Permitir</span><span class="sxs-lookup"><span data-stu-id="1d982-124">allow</span></span>|<span data-ttu-id="1d982-125">4</span><span class="sxs-lookup"><span data-stu-id="1d982-125">4</span></span>|<span data-ttu-id="1d982-126">Permitir la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="1d982-126">Allow the detected threat.</span></span>|
|<span data-ttu-id="1d982-127">userDefined</span><span class="sxs-lookup"><span data-stu-id="1d982-127">userDefined</span></span>|<span data-ttu-id="1d982-128">5</span><span class="sxs-lookup"><span data-stu-id="1d982-128">5</span></span>|<span data-ttu-id="1d982-129">Permitir que el usuario determinar la acción que se realizará con la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="1d982-129">Allow the user to determine the action to take with the detected threat.</span></span>|
|<span data-ttu-id="1d982-130">bloque</span><span class="sxs-lookup"><span data-stu-id="1d982-130">block</span></span>|<span data-ttu-id="1d982-131">6</span><span class="sxs-lookup"><span data-stu-id="1d982-131">6</span></span>|<span data-ttu-id="1d982-132">Bloquear la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="1d982-132">Block the detected threat.</span></span>|





