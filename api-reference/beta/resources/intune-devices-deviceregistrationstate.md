---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
author: tfitzmac
ms.openlocfilehash: a622613bd4ca5e065c3d9eb0331c05c360c1837c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360546"
---
# <a name="deviceregistrationstate-enum-type"></a><span data-ttu-id="6f67c-103">tipo de enumeración deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="6f67c-103">deviceRegistrationState enum type</span></span>

> <span data-ttu-id="6f67c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6f67c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6f67c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6f67c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6f67c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6f67c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6f67c-107">Estado de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f67c-107">Device registration status.</span></span>
## <a name="members"></a><span data-ttu-id="6f67c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f67c-108">Members</span></span>
|<span data-ttu-id="6f67c-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="6f67c-109">Member</span></span>|<span data-ttu-id="6f67c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6f67c-110">Value</span></span>|<span data-ttu-id="6f67c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f67c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6f67c-112">no registradas</span><span class="sxs-lookup"><span data-stu-id="6f67c-112">notRegistered</span></span>|<span data-ttu-id="6f67c-113">0</span><span class="sxs-lookup"><span data-stu-id="6f67c-113">0</span></span>|<span data-ttu-id="6f67c-114">El dispositivo no está registrado.</span><span class="sxs-lookup"><span data-stu-id="6f67c-114">The device is not registered.</span></span>|
|<span data-ttu-id="6f67c-115">registrado</span><span class="sxs-lookup"><span data-stu-id="6f67c-115">registered</span></span>|<span data-ttu-id="6f67c-116">2</span><span class="sxs-lookup"><span data-stu-id="6f67c-116">2</span></span>|<span data-ttu-id="6f67c-117">El dispositivo está registrado.</span><span class="sxs-lookup"><span data-stu-id="6f67c-117">The device is registered.</span></span>|
|<span data-ttu-id="6f67c-118">revocado</span><span class="sxs-lookup"><span data-stu-id="6f67c-118">revoked</span></span>|<span data-ttu-id="6f67c-119">3</span><span class="sxs-lookup"><span data-stu-id="6f67c-119">3</span></span>|<span data-ttu-id="6f67c-120">El dispositivo se ha bloqueado, borre o retirado.</span><span class="sxs-lookup"><span data-stu-id="6f67c-120">The device has been blocked, wiped or retired.</span></span>|
|<span data-ttu-id="6f67c-121">keyConflict</span><span class="sxs-lookup"><span data-stu-id="6f67c-121">keyConflict</span></span>|<span data-ttu-id="6f67c-122">4</span><span class="sxs-lookup"><span data-stu-id="6f67c-122">4</span></span>|<span data-ttu-id="6f67c-123">El dispositivo tiene un conflicto de clave.</span><span class="sxs-lookup"><span data-stu-id="6f67c-123">The device has a key conflict.</span></span>|
|<span data-ttu-id="6f67c-124">approvalPending</span><span class="sxs-lookup"><span data-stu-id="6f67c-124">approvalPending</span></span>|<span data-ttu-id="6f67c-125">5</span><span class="sxs-lookup"><span data-stu-id="6f67c-125">5</span></span>|<span data-ttu-id="6f67c-126">El dispositivo está pendiente de aprobación.</span><span class="sxs-lookup"><span data-stu-id="6f67c-126">The device is pending approval.</span></span>|
|<span data-ttu-id="6f67c-127">certificateReset</span><span class="sxs-lookup"><span data-stu-id="6f67c-127">certificateReset</span></span>|<span data-ttu-id="6f67c-128">6</span><span class="sxs-lookup"><span data-stu-id="6f67c-128">6</span></span>|<span data-ttu-id="6f67c-129">Se ha restablecido el certificado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f67c-129">The device certificate has been reset.</span></span>|
|<span data-ttu-id="6f67c-130">notRegisteredPendingEnrollment</span><span class="sxs-lookup"><span data-stu-id="6f67c-130">notRegisteredPendingEnrollment</span></span>|<span data-ttu-id="6f67c-131">7</span><span class="sxs-lookup"><span data-stu-id="6f67c-131">7</span></span>|<span data-ttu-id="6f67c-132">El dispositivo no está registrado y las pendientes de inscripción.</span><span class="sxs-lookup"><span data-stu-id="6f67c-132">The device is not registered and pending enrollment.</span></span>|
|<span data-ttu-id="6f67c-133">desconocido</span><span class="sxs-lookup"><span data-stu-id="6f67c-133">unknown</span></span>|<span data-ttu-id="6f67c-134">8</span><span class="sxs-lookup"><span data-stu-id="6f67c-134">8</span></span>|<span data-ttu-id="6f67c-135">El estado de registro de dispositivo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="6f67c-135">The device registration status is unknown.</span></span>|





