---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7633419ebeeb5c5865cd1a80c251effbf314b018
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829767"
---
# <a name="deviceregistrationstate-enum-type"></a><span data-ttu-id="9b9e9-103">tipo de enumeración deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="9b9e9-103">deviceRegistrationState enum type</span></span>

> <span data-ttu-id="9b9e9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b9e9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b9e9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b9e9-107">Estado de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-107">Device registration status.</span></span>
## <a name="members"></a><span data-ttu-id="9b9e9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b9e9-108">Members</span></span>
|<span data-ttu-id="9b9e9-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="9b9e9-109">Member</span></span>|<span data-ttu-id="9b9e9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9b9e9-110">Value</span></span>|<span data-ttu-id="9b9e9-111">Description</span><span class="sxs-lookup"><span data-stu-id="9b9e9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b9e9-112">no registradas</span><span class="sxs-lookup"><span data-stu-id="9b9e9-112">notRegistered</span></span>|<span data-ttu-id="9b9e9-113">0</span><span class="sxs-lookup"><span data-stu-id="9b9e9-113">0</span></span>|<span data-ttu-id="9b9e9-114">El dispositivo no está registrado.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-114">The device is not registered.</span></span>|
|<span data-ttu-id="9b9e9-115">registrado</span><span class="sxs-lookup"><span data-stu-id="9b9e9-115">registered</span></span>|<span data-ttu-id="9b9e9-116">2</span><span class="sxs-lookup"><span data-stu-id="9b9e9-116">2</span></span>|<span data-ttu-id="9b9e9-117">El dispositivo está registrado.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-117">The device is registered.</span></span>|
|<span data-ttu-id="9b9e9-118">revocado</span><span class="sxs-lookup"><span data-stu-id="9b9e9-118">revoked</span></span>|<span data-ttu-id="9b9e9-119">3</span><span class="sxs-lookup"><span data-stu-id="9b9e9-119">3</span></span>|<span data-ttu-id="9b9e9-120">El dispositivo se ha bloqueado, borre o retirado.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-120">The device has been blocked, wiped or retired.</span></span>|
|<span data-ttu-id="9b9e9-121">keyConflict</span><span class="sxs-lookup"><span data-stu-id="9b9e9-121">keyConflict</span></span>|<span data-ttu-id="9b9e9-122">4</span><span class="sxs-lookup"><span data-stu-id="9b9e9-122">4</span></span>|<span data-ttu-id="9b9e9-123">El dispositivo tiene un conflicto de clave.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-123">The device has a key conflict.</span></span>|
|<span data-ttu-id="9b9e9-124">approvalPending</span><span class="sxs-lookup"><span data-stu-id="9b9e9-124">approvalPending</span></span>|<span data-ttu-id="9b9e9-125">5</span><span class="sxs-lookup"><span data-stu-id="9b9e9-125">5</span></span>|<span data-ttu-id="9b9e9-126">El dispositivo está pendiente de aprobación.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-126">The device is pending approval.</span></span>|
|<span data-ttu-id="9b9e9-127">certificateReset</span><span class="sxs-lookup"><span data-stu-id="9b9e9-127">certificateReset</span></span>|<span data-ttu-id="9b9e9-128">6</span><span class="sxs-lookup"><span data-stu-id="9b9e9-128">6</span></span>|<span data-ttu-id="9b9e9-129">Se ha restablecido el certificado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-129">The device certificate has been reset.</span></span>|
|<span data-ttu-id="9b9e9-130">notRegisteredPendingEnrollment</span><span class="sxs-lookup"><span data-stu-id="9b9e9-130">notRegisteredPendingEnrollment</span></span>|<span data-ttu-id="9b9e9-131">7</span><span class="sxs-lookup"><span data-stu-id="9b9e9-131">7</span></span>|<span data-ttu-id="9b9e9-132">El dispositivo no está registrado y las pendientes de inscripción.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-132">The device is not registered and pending enrollment.</span></span>|
|<span data-ttu-id="9b9e9-133">desconocido</span><span class="sxs-lookup"><span data-stu-id="9b9e9-133">unknown</span></span>|<span data-ttu-id="9b9e9-134">8</span><span class="sxs-lookup"><span data-stu-id="9b9e9-134">8</span></span>|<span data-ttu-id="9b9e9-135">El estado de registro de dispositivo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-135">The device registration status is unknown.</span></span>|





