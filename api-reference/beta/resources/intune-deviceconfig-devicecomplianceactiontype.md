---
title: tipo de enumeración deviceComplianceActionType
description: Programado acción tipo Enum
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e2b89dbdaa3e67918b1b0c3e76eb6638e492994c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881875"
---
# <a name="devicecomplianceactiontype-enum-type"></a><span data-ttu-id="2a726-103">tipo de enumeración deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="2a726-103">deviceComplianceActionType enum type</span></span>

> <span data-ttu-id="2a726-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a726-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a726-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a726-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2a726-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a726-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a726-107">Programado acción tipo Enum</span><span class="sxs-lookup"><span data-stu-id="2a726-107">Scheduled Action Type Enum</span></span>
## <a name="members"></a><span data-ttu-id="2a726-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a726-108">Members</span></span>
|<span data-ttu-id="2a726-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="2a726-109">Member</span></span>|<span data-ttu-id="2a726-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2a726-110">Value</span></span>|<span data-ttu-id="2a726-111">Description</span><span class="sxs-lookup"><span data-stu-id="2a726-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a726-112">noAction</span><span class="sxs-lookup"><span data-stu-id="2a726-112">noAction</span></span>|<span data-ttu-id="2a726-113">0</span><span class="sxs-lookup"><span data-stu-id="2a726-113">0</span></span>|<span data-ttu-id="2a726-114">Ninguna acción</span><span class="sxs-lookup"><span data-stu-id="2a726-114">No Action</span></span>|
|<span data-ttu-id="2a726-115">notificación</span><span class="sxs-lookup"><span data-stu-id="2a726-115">notification</span></span>|<span data-ttu-id="2a726-116">1</span><span class="sxs-lookup"><span data-stu-id="2a726-116">1</span></span>|<span data-ttu-id="2a726-117">Enviar una notificación</span><span class="sxs-lookup"><span data-stu-id="2a726-117">Send Notification</span></span>|
|<span data-ttu-id="2a726-118">bloque</span><span class="sxs-lookup"><span data-stu-id="2a726-118">block</span></span>|<span data-ttu-id="2a726-119">2</span><span class="sxs-lookup"><span data-stu-id="2a726-119">2</span></span>|<span data-ttu-id="2a726-120">Bloquear el dispositivo en AAD</span><span class="sxs-lookup"><span data-stu-id="2a726-120">Block the device in AAD</span></span>|
|<span data-ttu-id="2a726-121">retirar</span><span class="sxs-lookup"><span data-stu-id="2a726-121">retire</span></span>|<span data-ttu-id="2a726-122">3</span><span class="sxs-lookup"><span data-stu-id="2a726-122">3</span></span>|<span data-ttu-id="2a726-123">Retirar el dispositivo</span><span class="sxs-lookup"><span data-stu-id="2a726-123">Retire the device</span></span>|
|<span data-ttu-id="2a726-124">Barrido</span><span class="sxs-lookup"><span data-stu-id="2a726-124">wipe</span></span>|<span data-ttu-id="2a726-125">4</span><span class="sxs-lookup"><span data-stu-id="2a726-125">4</span></span>|<span data-ttu-id="2a726-126">Borrar el dispositivo</span><span class="sxs-lookup"><span data-stu-id="2a726-126">Wipe the device</span></span>|
|<span data-ttu-id="2a726-127">removeResourceAccessProfiles</span><span class="sxs-lookup"><span data-stu-id="2a726-127">removeResourceAccessProfiles</span></span>|<span data-ttu-id="2a726-128">5</span><span class="sxs-lookup"><span data-stu-id="2a726-128">5</span></span>|<span data-ttu-id="2a726-129">Quitar perfiles de acceso a recursos del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2a726-129">Remove Resource Access Profiles from the device</span></span>|
|<span data-ttu-id="2a726-130">pushNotification</span><span class="sxs-lookup"><span data-stu-id="2a726-130">pushNotification</span></span>|<span data-ttu-id="2a726-131">9</span><span class="sxs-lookup"><span data-stu-id="2a726-131">9</span></span>|<span data-ttu-id="2a726-132">Enviar notificación de inserción para dispositivos</span><span class="sxs-lookup"><span data-stu-id="2a726-132">Send push notification to device</span></span>|
|<span data-ttu-id="2a726-133">remoteLock</span><span class="sxs-lookup"><span data-stu-id="2a726-133">remoteLock</span></span>|<span data-ttu-id="2a726-134">10</span><span class="sxs-lookup"><span data-stu-id="2a726-134">10</span></span>|<span data-ttu-id="2a726-135">Bloquear el dispositivo de forma remota</span><span class="sxs-lookup"><span data-stu-id="2a726-135">Remotely lock the device</span></span>|





