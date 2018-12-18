---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
author: tfitzmac
ms.openlocfilehash: 9fdd5cd3a63472e841f0d97f8cbee3a0f548380d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320094"
---
# <a name="deviceregistrationstate-enum-type"></a><span data-ttu-id="c2117-103">tipo de enumeración deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="c2117-103">deviceRegistrationState enum type</span></span>

> <span data-ttu-id="c2117-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2117-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2117-105">Estado de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2117-105">Device registration status.</span></span>
## <a name="members"></a><span data-ttu-id="c2117-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2117-106">Members</span></span>
|<span data-ttu-id="c2117-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="c2117-107">Member</span></span>|<span data-ttu-id="c2117-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c2117-108">Value</span></span>|<span data-ttu-id="c2117-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2117-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2117-110">no registradas</span><span class="sxs-lookup"><span data-stu-id="c2117-110">notRegistered</span></span>|<span data-ttu-id="c2117-111">0</span><span class="sxs-lookup"><span data-stu-id="c2117-111">0</span></span>|<span data-ttu-id="c2117-112">El dispositivo no está registrado.</span><span class="sxs-lookup"><span data-stu-id="c2117-112">The device is not registered.</span></span>|
|<span data-ttu-id="c2117-113">registrado</span><span class="sxs-lookup"><span data-stu-id="c2117-113">registered</span></span>|<span data-ttu-id="c2117-114">2</span><span class="sxs-lookup"><span data-stu-id="c2117-114">2</span></span>|<span data-ttu-id="c2117-115">El dispositivo está registrado.</span><span class="sxs-lookup"><span data-stu-id="c2117-115">The device is registered.</span></span>|
|<span data-ttu-id="c2117-116">revocado</span><span class="sxs-lookup"><span data-stu-id="c2117-116">revoked</span></span>|<span data-ttu-id="c2117-117">3</span><span class="sxs-lookup"><span data-stu-id="c2117-117">3</span></span>|<span data-ttu-id="c2117-118">El dispositivo se ha bloqueado, borre o retirado.</span><span class="sxs-lookup"><span data-stu-id="c2117-118">The device has been blocked, wiped or retired.</span></span>|
|<span data-ttu-id="c2117-119">keyConflict</span><span class="sxs-lookup"><span data-stu-id="c2117-119">keyConflict</span></span>|<span data-ttu-id="c2117-120">4</span><span class="sxs-lookup"><span data-stu-id="c2117-120">4</span></span>|<span data-ttu-id="c2117-121">El dispositivo tiene un conflicto de clave.</span><span class="sxs-lookup"><span data-stu-id="c2117-121">The device has a key conflict.</span></span>|
|<span data-ttu-id="c2117-122">approvalPending</span><span class="sxs-lookup"><span data-stu-id="c2117-122">approvalPending</span></span>|<span data-ttu-id="c2117-123">5</span><span class="sxs-lookup"><span data-stu-id="c2117-123">5</span></span>|<span data-ttu-id="c2117-124">El dispositivo está pendiente de aprobación.</span><span class="sxs-lookup"><span data-stu-id="c2117-124">The device is pending approval.</span></span>|
|<span data-ttu-id="c2117-125">certificateReset</span><span class="sxs-lookup"><span data-stu-id="c2117-125">certificateReset</span></span>|<span data-ttu-id="c2117-126">6</span><span class="sxs-lookup"><span data-stu-id="c2117-126">6</span></span>|<span data-ttu-id="c2117-127">Se ha restablecido el certificado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2117-127">The device certificate has been reset.</span></span>|
|<span data-ttu-id="c2117-128">notRegisteredPendingEnrollment</span><span class="sxs-lookup"><span data-stu-id="c2117-128">notRegisteredPendingEnrollment</span></span>|<span data-ttu-id="c2117-129">7</span><span class="sxs-lookup"><span data-stu-id="c2117-129">7</span></span>|<span data-ttu-id="c2117-130">El dispositivo no está registrado y las pendientes de inscripción.</span><span class="sxs-lookup"><span data-stu-id="c2117-130">The device is not registered and pending enrollment.</span></span>|
|<span data-ttu-id="c2117-131">desconocido</span><span class="sxs-lookup"><span data-stu-id="c2117-131">unknown</span></span>|<span data-ttu-id="c2117-132">8</span><span class="sxs-lookup"><span data-stu-id="c2117-132">8</span></span>|<span data-ttu-id="c2117-133">El estado de registro de dispositivo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="c2117-133">The device registration status is unknown.</span></span>|



