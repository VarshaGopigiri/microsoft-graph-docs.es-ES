---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
localization_priority: Normal
ms.openlocfilehash: ed84a16dbac493a3e962e37ba246d8d418782a91
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852825"
---
# <a name="defenderthreataction-enum-type"></a><span data-ttu-id="30b26-103">tipo de enumeración defenderThreatAction</span><span class="sxs-lookup"><span data-stu-id="30b26-103">defenderThreatAction enum type</span></span>

> <span data-ttu-id="30b26-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30b26-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30b26-105">Acción de predeterminada del Defender tomar detecta las amenazas de Malware.</span><span class="sxs-lookup"><span data-stu-id="30b26-105">Defender’s default action to take on detected Malware threats.</span></span>
## <a name="members"></a><span data-ttu-id="30b26-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="30b26-106">Members</span></span>
|<span data-ttu-id="30b26-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="30b26-107">Member</span></span>|<span data-ttu-id="30b26-108">Valor</span><span class="sxs-lookup"><span data-stu-id="30b26-108">Value</span></span>|<span data-ttu-id="30b26-109">Description</span><span class="sxs-lookup"><span data-stu-id="30b26-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="30b26-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="30b26-110">deviceDefault</span></span>|<span data-ttu-id="30b26-111">0</span><span class="sxs-lookup"><span data-stu-id="30b26-111">0</span></span>|<span data-ttu-id="30b26-112">Aplicar la acción en función de la definición de actualización.</span><span class="sxs-lookup"><span data-stu-id="30b26-112">Apply action based on the update definition.</span></span>|
|<span data-ttu-id="30b26-113">clean</span><span class="sxs-lookup"><span data-stu-id="30b26-113">clean</span></span>|<span data-ttu-id="30b26-114">1</span><span class="sxs-lookup"><span data-stu-id="30b26-114">1</span></span>|<span data-ttu-id="30b26-115">Limpiar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="30b26-115">Clean the detected threat.</span></span>|
|<span data-ttu-id="30b26-116">cuarentena</span><span class="sxs-lookup"><span data-stu-id="30b26-116">quarantine</span></span>|<span data-ttu-id="30b26-117">2</span><span class="sxs-lookup"><span data-stu-id="30b26-117">2</span></span>|<span data-ttu-id="30b26-118">La amenaza detectada en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="30b26-118">Quarantine the detected threat.</span></span>|
|<span data-ttu-id="30b26-119">remove</span><span class="sxs-lookup"><span data-stu-id="30b26-119">remove</span></span>|<span data-ttu-id="30b26-120">3</span><span class="sxs-lookup"><span data-stu-id="30b26-120">3</span></span>|<span data-ttu-id="30b26-121">Quitar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="30b26-121">Remove the detected threat.</span></span>|
|<span data-ttu-id="30b26-122">Permitir</span><span class="sxs-lookup"><span data-stu-id="30b26-122">allow</span></span>|<span data-ttu-id="30b26-123">4</span><span class="sxs-lookup"><span data-stu-id="30b26-123">4</span></span>|<span data-ttu-id="30b26-124">Permitir la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="30b26-124">Allow the detected threat.</span></span>|
|<span data-ttu-id="30b26-125">userDefined</span><span class="sxs-lookup"><span data-stu-id="30b26-125">userDefined</span></span>|<span data-ttu-id="30b26-126">5</span><span class="sxs-lookup"><span data-stu-id="30b26-126">5</span></span>|<span data-ttu-id="30b26-127">Permitir que el usuario determinar la acción que se realizará con la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="30b26-127">Allow the user to determine the action to take with the detected threat.</span></span>|
|<span data-ttu-id="30b26-128">bloque</span><span class="sxs-lookup"><span data-stu-id="30b26-128">block</span></span>|<span data-ttu-id="30b26-129">6</span><span class="sxs-lookup"><span data-stu-id="30b26-129">6</span></span>|<span data-ttu-id="30b26-130">Bloquear la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="30b26-130">Block the detected threat.</span></span>|



