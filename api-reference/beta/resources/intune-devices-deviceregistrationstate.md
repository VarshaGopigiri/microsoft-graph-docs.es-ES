---
title: tipo de enumeración deviceRegistrationState
description: Estado de registro de dispositivo.
ms.openlocfilehash: 5496bce53e061894a829745fce0687815c855c01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090115"
---
# <a name="deviceregistrationstate-enum-type"></a><span data-ttu-id="f29f1-103">tipo de enumeración deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="f29f1-103">deviceRegistrationState enum type</span></span>

> <span data-ttu-id="f29f1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f29f1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f29f1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f29f1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f29f1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f29f1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f29f1-107">Estado de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f29f1-107">Device registration status.</span></span>
## <a name="members"></a><span data-ttu-id="f29f1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f29f1-108">Members</span></span>
|<span data-ttu-id="f29f1-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="f29f1-109">Member</span></span>|<span data-ttu-id="f29f1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f29f1-110">Value</span></span>|<span data-ttu-id="f29f1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f29f1-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f29f1-112">no registradas</span><span class="sxs-lookup"><span data-stu-id="f29f1-112">notRegistered</span></span>|<span data-ttu-id="f29f1-113">0</span><span class="sxs-lookup"><span data-stu-id="f29f1-113">0</span></span>|<span data-ttu-id="f29f1-114">El dispositivo no está registrado.</span><span class="sxs-lookup"><span data-stu-id="f29f1-114">The device is not registered.</span></span>|
|<span data-ttu-id="f29f1-115">registrado</span><span class="sxs-lookup"><span data-stu-id="f29f1-115">registered</span></span>|<span data-ttu-id="f29f1-116">2</span><span class="sxs-lookup"><span data-stu-id="f29f1-116">2</span></span>|<span data-ttu-id="f29f1-117">El dispositivo está registrado.</span><span class="sxs-lookup"><span data-stu-id="f29f1-117">The device is registered.</span></span>|
|<span data-ttu-id="f29f1-118">revocado</span><span class="sxs-lookup"><span data-stu-id="f29f1-118">revoked</span></span>|<span data-ttu-id="f29f1-119">3</span><span class="sxs-lookup"><span data-stu-id="f29f1-119">3</span></span>|<span data-ttu-id="f29f1-120">El dispositivo se ha bloqueado, borre o retirado.</span><span class="sxs-lookup"><span data-stu-id="f29f1-120">The device has been blocked, wiped or retired.</span></span>|
|<span data-ttu-id="f29f1-121">keyConflict</span><span class="sxs-lookup"><span data-stu-id="f29f1-121">keyConflict</span></span>|<span data-ttu-id="f29f1-122">4</span><span class="sxs-lookup"><span data-stu-id="f29f1-122">4</span></span>|<span data-ttu-id="f29f1-123">El dispositivo tiene un conflicto de clave.</span><span class="sxs-lookup"><span data-stu-id="f29f1-123">The device has a key conflict.</span></span>|
|<span data-ttu-id="f29f1-124">approvalPending</span><span class="sxs-lookup"><span data-stu-id="f29f1-124">approvalPending</span></span>|<span data-ttu-id="f29f1-125">5</span><span class="sxs-lookup"><span data-stu-id="f29f1-125">5</span></span>|<span data-ttu-id="f29f1-126">El dispositivo está pendiente de aprobación.</span><span class="sxs-lookup"><span data-stu-id="f29f1-126">The device is pending approval.</span></span>|
|<span data-ttu-id="f29f1-127">certificateReset</span><span class="sxs-lookup"><span data-stu-id="f29f1-127">certificateReset</span></span>|<span data-ttu-id="f29f1-128">6</span><span class="sxs-lookup"><span data-stu-id="f29f1-128">6</span></span>|<span data-ttu-id="f29f1-129">Se ha restablecido el certificado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f29f1-129">The device certificate has been reset.</span></span>|
|<span data-ttu-id="f29f1-130">notRegisteredPendingEnrollment</span><span class="sxs-lookup"><span data-stu-id="f29f1-130">notRegisteredPendingEnrollment</span></span>|<span data-ttu-id="f29f1-131">7</span><span class="sxs-lookup"><span data-stu-id="f29f1-131">7</span></span>|<span data-ttu-id="f29f1-132">El dispositivo no está registrado y las pendientes de inscripción.</span><span class="sxs-lookup"><span data-stu-id="f29f1-132">The device is not registered and pending enrollment.</span></span>|
|<span data-ttu-id="f29f1-133">desconocido</span><span class="sxs-lookup"><span data-stu-id="f29f1-133">unknown</span></span>|<span data-ttu-id="f29f1-134">8</span><span class="sxs-lookup"><span data-stu-id="f29f1-134">8</span></span>|<span data-ttu-id="f29f1-135">El estado de registro de dispositivo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="f29f1-135">The device registration status is unknown.</span></span>|





