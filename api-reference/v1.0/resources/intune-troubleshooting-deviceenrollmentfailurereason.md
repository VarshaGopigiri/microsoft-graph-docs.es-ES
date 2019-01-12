---
title: tipo de enumeración deviceEnrollmentFailureReason
description: Categorías de errores de nivel superior para la inscripción.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: efee4e4655d36e7575df9e0ddda508dbbcc473c5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962075"
---
# <a name="deviceenrollmentfailurereason-enum-type"></a><span data-ttu-id="5e61b-103">tipo de enumeración deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="5e61b-103">deviceEnrollmentFailureReason enum type</span></span>

> <span data-ttu-id="5e61b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5e61b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5e61b-105">Categorías de errores de nivel superior para la inscripción.</span><span class="sxs-lookup"><span data-stu-id="5e61b-105">Top level failure categories for enrollment.</span></span>
## <a name="members"></a><span data-ttu-id="5e61b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e61b-106">Members</span></span>
|<span data-ttu-id="5e61b-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5e61b-107">Member</span></span>|<span data-ttu-id="5e61b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5e61b-108">Value</span></span>|<span data-ttu-id="5e61b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e61b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5e61b-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="5e61b-110">unknown</span></span>|<span data-ttu-id="5e61b-111">0</span><span class="sxs-lookup"><span data-stu-id="5e61b-111">0</span></span>|<span data-ttu-id="5e61b-112">Valor predeterminado, el motivo del error es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5e61b-112">Default value, failure reason is unknown.</span></span>|
|<span data-ttu-id="5e61b-113">autenticación</span><span class="sxs-lookup"><span data-stu-id="5e61b-113">authentication</span></span>|<span data-ttu-id="5e61b-114">1</span><span class="sxs-lookup"><span data-stu-id="5e61b-114">1</span></span>|<span data-ttu-id="5e61b-115">Error de autenticación</span><span class="sxs-lookup"><span data-stu-id="5e61b-115">Authentication failed</span></span>|
|<span data-ttu-id="5e61b-116">autorización</span><span class="sxs-lookup"><span data-stu-id="5e61b-116">authorization</span></span>|<span data-ttu-id="5e61b-117">2</span><span class="sxs-lookup"><span data-stu-id="5e61b-117">2</span></span>|<span data-ttu-id="5e61b-118">La llamada se ha autenticado pero no autorizado para inscribirse.</span><span class="sxs-lookup"><span data-stu-id="5e61b-118">Call was authenticated, but not authorized to enroll.</span></span>|
|<span data-ttu-id="5e61b-119">accountValidation</span><span class="sxs-lookup"><span data-stu-id="5e61b-119">accountValidation</span></span>|<span data-ttu-id="5e61b-120">3</span><span class="sxs-lookup"><span data-stu-id="5e61b-120">3</span></span>|<span data-ttu-id="5e61b-121">Error al validar la cuenta para la inscripción.</span><span class="sxs-lookup"><span data-stu-id="5e61b-121">Failed to validate the account for enrollment.</span></span> <span data-ttu-id="5e61b-122">(Cuenta bloqueada, no se ha habilitado la inscripción)</span><span class="sxs-lookup"><span data-stu-id="5e61b-122">(Account blocked, enrollment not enabled)</span></span>|
|<span data-ttu-id="5e61b-123">userValidation</span><span class="sxs-lookup"><span data-stu-id="5e61b-123">userValidation</span></span>|<span data-ttu-id="5e61b-124">4</span><span class="sxs-lookup"><span data-stu-id="5e61b-124">4</span></span>|<span data-ttu-id="5e61b-125">No se pudo validar el usuario.</span><span class="sxs-lookup"><span data-stu-id="5e61b-125">User could not be validated.</span></span> <span data-ttu-id="5e61b-126">(Usuario no existe, licencia que faltan)</span><span class="sxs-lookup"><span data-stu-id="5e61b-126">(User does not exist, missing license)</span></span>|
|<span data-ttu-id="5e61b-127">deviceNotSupported</span><span class="sxs-lookup"><span data-stu-id="5e61b-127">deviceNotSupported</span></span>|<span data-ttu-id="5e61b-128">5</span><span class="sxs-lookup"><span data-stu-id="5e61b-128">5</span></span>|<span data-ttu-id="5e61b-129">Dispositivo no es compatible para la administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="5e61b-129">Device is not supported for mobile device management.</span></span>|
|<span data-ttu-id="5e61b-130">inMaintenance</span><span class="sxs-lookup"><span data-stu-id="5e61b-130">inMaintenance</span></span>|<span data-ttu-id="5e61b-131">6</span><span class="sxs-lookup"><span data-stu-id="5e61b-131">6</span></span>|<span data-ttu-id="5e61b-132">Cuenta está en mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5e61b-132">Account is in maintenance.</span></span>|
|<span data-ttu-id="5e61b-133">badRequest</span><span class="sxs-lookup"><span data-stu-id="5e61b-133">badRequest</span></span>|<span data-ttu-id="5e61b-134">7</span><span class="sxs-lookup"><span data-stu-id="5e61b-134">7</span></span>|<span data-ttu-id="5e61b-135">Cliente envió una solicitud que no se entiende/admitidos por el servicio.</span><span class="sxs-lookup"><span data-stu-id="5e61b-135">Client sent a request that is not understood/supported by the service.</span></span>|
|<span data-ttu-id="5e61b-136">featureNotSupported</span><span class="sxs-lookup"><span data-stu-id="5e61b-136">featureNotSupported</span></span>|<span data-ttu-id="5e61b-137">8</span><span class="sxs-lookup"><span data-stu-id="5e61b-137">8</span></span>|<span data-ttu-id="5e61b-138">Utilizado por este inscripción las características no se admiten para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="5e61b-138">Feature(s) used by this enrollment are not supported for this account.</span></span>|
|<span data-ttu-id="5e61b-139">enrollmentRestrictionsEnforced</span><span class="sxs-lookup"><span data-stu-id="5e61b-139">enrollmentRestrictionsEnforced</span></span>|<span data-ttu-id="5e61b-140">9</span><span class="sxs-lookup"><span data-stu-id="5e61b-140">9</span></span>|<span data-ttu-id="5e61b-141">Restricciones de inscripción configuradas por el administrador bloquean esta inscripción.</span><span class="sxs-lookup"><span data-stu-id="5e61b-141">Enrollment restrictions configured by admin blocked this enrollment.</span></span>|
|<span data-ttu-id="5e61b-142">clientDisconnected</span><span class="sxs-lookup"><span data-stu-id="5e61b-142">clientDisconnected</span></span>|<span data-ttu-id="5e61b-143">10</span><span class="sxs-lookup"><span data-stu-id="5e61b-143">10</span></span>|<span data-ttu-id="5e61b-144">Cliente agotó el tiempo de espera o inscripción se anuló por para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="5e61b-144">Client timed out or enrollment was aborted by enduser.</span></span>|
|<span data-ttu-id="5e61b-145">userAbandonment</span><span class="sxs-lookup"><span data-stu-id="5e61b-145">userAbandonment</span></span>|<span data-ttu-id="5e61b-146">11</span><span class="sxs-lookup"><span data-stu-id="5e61b-146">11</span></span>|<span data-ttu-id="5e61b-147">Se ha cancelado la inscripción por para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="5e61b-147">Enrollment was abandoned by enduser.</span></span> <span data-ttu-id="5e61b-148">(Para el usuario final inicia la incorporación de redes pero no se pudo completar en forma oportuna)</span><span class="sxs-lookup"><span data-stu-id="5e61b-148">(Enduser started onboarding but failed to complete it in timely manner)</span></span>|


<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: Enum deviceEnrollmentFailureReason has some values specified and others unspecified."
  ],
}
-->
