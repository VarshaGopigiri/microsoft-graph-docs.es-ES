---
title: tipo de enumeración deviceComplianceActionType
description: Programado acción tipo Enum
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f1856847cb8a8ecf48ee6d13067bd24515326d89
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973212"
---
# <a name="devicecomplianceactiontype-enum-type"></a><span data-ttu-id="ce49c-103">tipo de enumeración deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="ce49c-103">deviceComplianceActionType enum type</span></span>

> <span data-ttu-id="ce49c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce49c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce49c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce49c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ce49c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce49c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce49c-107">Programado acción tipo Enum</span><span class="sxs-lookup"><span data-stu-id="ce49c-107">Scheduled Action Type Enum</span></span>
## <a name="members"></a><span data-ttu-id="ce49c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce49c-108">Members</span></span>
|<span data-ttu-id="ce49c-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ce49c-109">Member</span></span>|<span data-ttu-id="ce49c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ce49c-110">Value</span></span>|<span data-ttu-id="ce49c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce49c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce49c-112">noAction</span><span class="sxs-lookup"><span data-stu-id="ce49c-112">noAction</span></span>|<span data-ttu-id="ce49c-113">0</span><span class="sxs-lookup"><span data-stu-id="ce49c-113">0</span></span>|<span data-ttu-id="ce49c-114">Ninguna acción</span><span class="sxs-lookup"><span data-stu-id="ce49c-114">No Action</span></span>|
|<span data-ttu-id="ce49c-115">notificación</span><span class="sxs-lookup"><span data-stu-id="ce49c-115">notification</span></span>|<span data-ttu-id="ce49c-116">1</span><span class="sxs-lookup"><span data-stu-id="ce49c-116">1</span></span>|<span data-ttu-id="ce49c-117">Enviar una notificación</span><span class="sxs-lookup"><span data-stu-id="ce49c-117">Send Notification</span></span>|
|<span data-ttu-id="ce49c-118">bloque</span><span class="sxs-lookup"><span data-stu-id="ce49c-118">block</span></span>|<span data-ttu-id="ce49c-119">2</span><span class="sxs-lookup"><span data-stu-id="ce49c-119">2</span></span>|<span data-ttu-id="ce49c-120">Bloquear el dispositivo en AAD</span><span class="sxs-lookup"><span data-stu-id="ce49c-120">Block the device in AAD</span></span>|
|<span data-ttu-id="ce49c-121">retirar</span><span class="sxs-lookup"><span data-stu-id="ce49c-121">retire</span></span>|<span data-ttu-id="ce49c-122">3</span><span class="sxs-lookup"><span data-stu-id="ce49c-122">3</span></span>|<span data-ttu-id="ce49c-123">Retirar el dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce49c-123">Retire the device</span></span>|
|<span data-ttu-id="ce49c-124">Barrido</span><span class="sxs-lookup"><span data-stu-id="ce49c-124">wipe</span></span>|<span data-ttu-id="ce49c-125">4</span><span class="sxs-lookup"><span data-stu-id="ce49c-125">4</span></span>|<span data-ttu-id="ce49c-126">Borrar el dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce49c-126">Wipe the device</span></span>|
|<span data-ttu-id="ce49c-127">removeResourceAccessProfiles</span><span class="sxs-lookup"><span data-stu-id="ce49c-127">removeResourceAccessProfiles</span></span>|<span data-ttu-id="ce49c-128">5</span><span class="sxs-lookup"><span data-stu-id="ce49c-128">5</span></span>|<span data-ttu-id="ce49c-129">Quitar perfiles de acceso a recursos del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce49c-129">Remove Resource Access Profiles from the device</span></span>|
|<span data-ttu-id="ce49c-130">pushNotification</span><span class="sxs-lookup"><span data-stu-id="ce49c-130">pushNotification</span></span>|<span data-ttu-id="ce49c-131">9</span><span class="sxs-lookup"><span data-stu-id="ce49c-131">9</span></span>|<span data-ttu-id="ce49c-132">Enviar notificación de inserción para dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce49c-132">Send push notification to device</span></span>|
|<span data-ttu-id="ce49c-133">remoteLock</span><span class="sxs-lookup"><span data-stu-id="ce49c-133">remoteLock</span></span>|<span data-ttu-id="ce49c-134">10</span><span class="sxs-lookup"><span data-stu-id="ce49c-134">10</span></span>|<span data-ttu-id="ce49c-135">Bloquear el dispositivo de forma remota</span><span class="sxs-lookup"><span data-stu-id="ce49c-135">Remotely lock the device</span></span>|





