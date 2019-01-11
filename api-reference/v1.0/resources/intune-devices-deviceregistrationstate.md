---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e2b755d213d39beb228afe603b2066b55416f14c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857326"
---
# <a name="deviceregistrationstate-enum-type"></a><span data-ttu-id="a5e03-103">tipo de enumeración deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="a5e03-103">deviceRegistrationState enum type</span></span>

> <span data-ttu-id="a5e03-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a5e03-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a5e03-105">Estado de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e03-105">Device registration status.</span></span>
## <a name="members"></a><span data-ttu-id="a5e03-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5e03-106">Members</span></span>
|<span data-ttu-id="a5e03-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a5e03-107">Member</span></span>|<span data-ttu-id="a5e03-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a5e03-108">Value</span></span>|<span data-ttu-id="a5e03-109">Description</span><span class="sxs-lookup"><span data-stu-id="a5e03-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a5e03-110">no registradas</span><span class="sxs-lookup"><span data-stu-id="a5e03-110">notRegistered</span></span>|<span data-ttu-id="a5e03-111">0</span><span class="sxs-lookup"><span data-stu-id="a5e03-111">0</span></span>|<span data-ttu-id="a5e03-112">El dispositivo no está registrado.</span><span class="sxs-lookup"><span data-stu-id="a5e03-112">The device is not registered.</span></span>|
|<span data-ttu-id="a5e03-113">registrado</span><span class="sxs-lookup"><span data-stu-id="a5e03-113">registered</span></span>|<span data-ttu-id="a5e03-114">2</span><span class="sxs-lookup"><span data-stu-id="a5e03-114">2</span></span>|<span data-ttu-id="a5e03-115">El dispositivo está registrado.</span><span class="sxs-lookup"><span data-stu-id="a5e03-115">The device is registered.</span></span>|
|<span data-ttu-id="a5e03-116">revocado</span><span class="sxs-lookup"><span data-stu-id="a5e03-116">revoked</span></span>|<span data-ttu-id="a5e03-117">3</span><span class="sxs-lookup"><span data-stu-id="a5e03-117">3</span></span>|<span data-ttu-id="a5e03-118">El dispositivo se ha bloqueado, borre o retirado.</span><span class="sxs-lookup"><span data-stu-id="a5e03-118">The device has been blocked, wiped or retired.</span></span>|
|<span data-ttu-id="a5e03-119">keyConflict</span><span class="sxs-lookup"><span data-stu-id="a5e03-119">keyConflict</span></span>|<span data-ttu-id="a5e03-120">4</span><span class="sxs-lookup"><span data-stu-id="a5e03-120">4</span></span>|<span data-ttu-id="a5e03-121">El dispositivo tiene un conflicto de clave.</span><span class="sxs-lookup"><span data-stu-id="a5e03-121">The device has a key conflict.</span></span>|
|<span data-ttu-id="a5e03-122">approvalPending</span><span class="sxs-lookup"><span data-stu-id="a5e03-122">approvalPending</span></span>|<span data-ttu-id="a5e03-123">5</span><span class="sxs-lookup"><span data-stu-id="a5e03-123">5</span></span>|<span data-ttu-id="a5e03-124">El dispositivo está pendiente de aprobación.</span><span class="sxs-lookup"><span data-stu-id="a5e03-124">The device is pending approval.</span></span>|
|<span data-ttu-id="a5e03-125">certificateReset</span><span class="sxs-lookup"><span data-stu-id="a5e03-125">certificateReset</span></span>|<span data-ttu-id="a5e03-126">6</span><span class="sxs-lookup"><span data-stu-id="a5e03-126">6</span></span>|<span data-ttu-id="a5e03-127">Se ha restablecido el certificado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e03-127">The device certificate has been reset.</span></span>|
|<span data-ttu-id="a5e03-128">notRegisteredPendingEnrollment</span><span class="sxs-lookup"><span data-stu-id="a5e03-128">notRegisteredPendingEnrollment</span></span>|<span data-ttu-id="a5e03-129">7</span><span class="sxs-lookup"><span data-stu-id="a5e03-129">7</span></span>|<span data-ttu-id="a5e03-130">El dispositivo no está registrado y las pendientes de inscripción.</span><span class="sxs-lookup"><span data-stu-id="a5e03-130">The device is not registered and pending enrollment.</span></span>|
|<span data-ttu-id="a5e03-131">desconocido</span><span class="sxs-lookup"><span data-stu-id="a5e03-131">unknown</span></span>|<span data-ttu-id="a5e03-132">8</span><span class="sxs-lookup"><span data-stu-id="a5e03-132">8</span></span>|<span data-ttu-id="a5e03-133">El estado de registro de dispositivo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="a5e03-133">The device registration status is unknown.</span></span>|



