---
title: tipo de enumeración defenderThreatAction
description: Acción de predeterminada del Defender tomar detecta las amenazas de Malware.
ms.openlocfilehash: a5eb108a3ab26596eec9abe838e3bbfe853d96d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031483"
---
# <a name="defenderthreataction-enum-type"></a><span data-ttu-id="77815-103">tipo de enumeración defenderThreatAction</span><span class="sxs-lookup"><span data-stu-id="77815-103">defenderThreatAction enum type</span></span>

> <span data-ttu-id="77815-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="77815-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="77815-105">Acción de predeterminada del Defender tomar detecta las amenazas de Malware.</span><span class="sxs-lookup"><span data-stu-id="77815-105">Defender’s default action to take on detected Malware threats.</span></span>
## <a name="members"></a><span data-ttu-id="77815-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="77815-106">Members</span></span>
|<span data-ttu-id="77815-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="77815-107">Member</span></span>|<span data-ttu-id="77815-108">Valor</span><span class="sxs-lookup"><span data-stu-id="77815-108">Value</span></span>|<span data-ttu-id="77815-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="77815-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="77815-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="77815-110">deviceDefault</span></span>|<span data-ttu-id="77815-111">0</span><span class="sxs-lookup"><span data-stu-id="77815-111">0</span></span>|<span data-ttu-id="77815-112">Aplicar la acción en función de la definición de actualización.</span><span class="sxs-lookup"><span data-stu-id="77815-112">Apply action based on the update definition.</span></span>|
|<span data-ttu-id="77815-113">clean</span><span class="sxs-lookup"><span data-stu-id="77815-113">clean</span></span>|<span data-ttu-id="77815-114">1</span><span class="sxs-lookup"><span data-stu-id="77815-114">1</span></span>|<span data-ttu-id="77815-115">Limpiar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="77815-115">Clean the detected threat.</span></span>|
|<span data-ttu-id="77815-116">cuarentena</span><span class="sxs-lookup"><span data-stu-id="77815-116">quarantine</span></span>|<span data-ttu-id="77815-117">2</span><span class="sxs-lookup"><span data-stu-id="77815-117">2</span></span>|<span data-ttu-id="77815-118">La amenaza detectada en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="77815-118">Quarantine the detected threat.</span></span>|
|<span data-ttu-id="77815-119">remove</span><span class="sxs-lookup"><span data-stu-id="77815-119">remove</span></span>|<span data-ttu-id="77815-120">3</span><span class="sxs-lookup"><span data-stu-id="77815-120">3</span></span>|<span data-ttu-id="77815-121">Quitar la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="77815-121">Remove the detected threat.</span></span>|
|<span data-ttu-id="77815-122">Permitir</span><span class="sxs-lookup"><span data-stu-id="77815-122">allow</span></span>|<span data-ttu-id="77815-123">4</span><span class="sxs-lookup"><span data-stu-id="77815-123">4</span></span>|<span data-ttu-id="77815-124">Permitir la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="77815-124">Allow the detected threat.</span></span>|
|<span data-ttu-id="77815-125">userDefined</span><span class="sxs-lookup"><span data-stu-id="77815-125">userDefined</span></span>|<span data-ttu-id="77815-126">5</span><span class="sxs-lookup"><span data-stu-id="77815-126">5</span></span>|<span data-ttu-id="77815-127">Permitir que el usuario determinar la acción que se realizará con la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="77815-127">Allow the user to determine the action to take with the detected threat.</span></span>|
|<span data-ttu-id="77815-128">bloque</span><span class="sxs-lookup"><span data-stu-id="77815-128">block</span></span>|<span data-ttu-id="77815-129">6</span><span class="sxs-lookup"><span data-stu-id="77815-129">6</span></span>|<span data-ttu-id="77815-130">Bloquear la amenaza detectada.</span><span class="sxs-lookup"><span data-stu-id="77815-130">Block the detected threat.</span></span>|



