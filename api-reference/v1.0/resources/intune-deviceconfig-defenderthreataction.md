---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 51aa26483ac6b79d48567f7e5950733def31f01e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976649"
---
# <a name="defenderthreataction-enum-type"></a><span data-ttu-id="5a75a-103">tipo de enumeración defenderThreatAction</span><span class="sxs-lookup"><span data-stu-id="5a75a-103">defenderThreatAction enum type</span></span>

> <span data-ttu-id="5a75a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5a75a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5a75a-105">Acción de predeterminada del Defender tomar detecta las amenazas de Malware.</span><span class="sxs-lookup"><span data-stu-id="5a75a-105">Defender’s default action to take on detected Malware threats.</span></span>
## <a name="members"></a><span data-ttu-id="5a75a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a75a-106">Members</span></span>
|<span data-ttu-id="5a75a-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5a75a-107">Member</span></span>|<span data-ttu-id="5a75a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5a75a-108">Value</span></span>|<span data-ttu-id="5a75a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a75a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5a75a-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="5a75a-110">deviceDefault</span></span>|<span data-ttu-id="5a75a-111">0</span><span class="sxs-lookup"><span data-stu-id="5a75a-111">0</span></span>|<span data-ttu-id="5a75a-112">Aplicar la acción en función de la definición de actualización.</span><span class="sxs-lookup"><span data-stu-id="5a75a-112">Apply action based on the update definition.</span></span>|
|<span data-ttu-id="5a75a-113">clean</span><span class="sxs-lookup"><span data-stu-id="5a75a-113">clean</span></span>|<span data-ttu-id="5a75a-114">1</span><span class="sxs-lookup"><span data-stu-id="5a75a-114">1</span></span>|<span data-ttu-id="5a75a-115">Limpiar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="5a75a-115">Clean the detected threat.</span></span>|
|<span data-ttu-id="5a75a-116">cuarentena</span><span class="sxs-lookup"><span data-stu-id="5a75a-116">quarantine</span></span>|<span data-ttu-id="5a75a-117">2</span><span class="sxs-lookup"><span data-stu-id="5a75a-117">2</span></span>|<span data-ttu-id="5a75a-118">La amenaza detectada en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="5a75a-118">Quarantine the detected threat.</span></span>|
|<span data-ttu-id="5a75a-119">remove</span><span class="sxs-lookup"><span data-stu-id="5a75a-119">remove</span></span>|<span data-ttu-id="5a75a-120">3</span><span class="sxs-lookup"><span data-stu-id="5a75a-120">3</span></span>|<span data-ttu-id="5a75a-121">Quitar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="5a75a-121">Remove the detected threat.</span></span>|
|<span data-ttu-id="5a75a-122">Permitir</span><span class="sxs-lookup"><span data-stu-id="5a75a-122">allow</span></span>|<span data-ttu-id="5a75a-123">4</span><span class="sxs-lookup"><span data-stu-id="5a75a-123">4</span></span>|<span data-ttu-id="5a75a-124">Permitir la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="5a75a-124">Allow the detected threat.</span></span>|
|<span data-ttu-id="5a75a-125">userDefined</span><span class="sxs-lookup"><span data-stu-id="5a75a-125">userDefined</span></span>|<span data-ttu-id="5a75a-126">5</span><span class="sxs-lookup"><span data-stu-id="5a75a-126">5</span></span>|<span data-ttu-id="5a75a-127">Permitir que el usuario determinar la acción que se realizará con la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="5a75a-127">Allow the user to determine the action to take with the detected threat.</span></span>|
|<span data-ttu-id="5a75a-128">bloque</span><span class="sxs-lookup"><span data-stu-id="5a75a-128">block</span></span>|<span data-ttu-id="5a75a-129">6</span><span class="sxs-lookup"><span data-stu-id="5a75a-129">6</span></span>|<span data-ttu-id="5a75a-130">Bloquear la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="5a75a-130">Block the detected threat.</span></span>|



