---
title: tipo de enumeración deviceComplianceActionType
description: Programado acción tipo Enum
author: tfitzmac
ms.openlocfilehash: 9fd0a8bd045ad04fe0acf55f899e693d7fcce5d0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335689"
---
# <a name="devicecomplianceactiontype-enum-type"></a><span data-ttu-id="548fc-103">tipo de enumeración deviceComplianceActionType</span><span class="sxs-lookup"><span data-stu-id="548fc-103">deviceComplianceActionType enum type</span></span>

> <span data-ttu-id="548fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="548fc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="548fc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="548fc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="548fc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="548fc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="548fc-107">Programado acción tipo Enum</span><span class="sxs-lookup"><span data-stu-id="548fc-107">Scheduled Action Type Enum</span></span>
## <a name="members"></a><span data-ttu-id="548fc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="548fc-108">Members</span></span>
|<span data-ttu-id="548fc-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="548fc-109">Member</span></span>|<span data-ttu-id="548fc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="548fc-110">Value</span></span>|<span data-ttu-id="548fc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="548fc-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="548fc-112">noAction</span><span class="sxs-lookup"><span data-stu-id="548fc-112">noAction</span></span>|<span data-ttu-id="548fc-113">0</span><span class="sxs-lookup"><span data-stu-id="548fc-113">0</span></span>|<span data-ttu-id="548fc-114">Ninguna acción</span><span class="sxs-lookup"><span data-stu-id="548fc-114">No Action</span></span>|
|<span data-ttu-id="548fc-115">notificación</span><span class="sxs-lookup"><span data-stu-id="548fc-115">notification</span></span>|<span data-ttu-id="548fc-116">1</span><span class="sxs-lookup"><span data-stu-id="548fc-116">1</span></span>|<span data-ttu-id="548fc-117">Enviar una notificación</span><span class="sxs-lookup"><span data-stu-id="548fc-117">Send Notification</span></span>|
|<span data-ttu-id="548fc-118">bloque</span><span class="sxs-lookup"><span data-stu-id="548fc-118">block</span></span>|<span data-ttu-id="548fc-119">2</span><span class="sxs-lookup"><span data-stu-id="548fc-119">2</span></span>|<span data-ttu-id="548fc-120">Bloquear el dispositivo en AAD</span><span class="sxs-lookup"><span data-stu-id="548fc-120">Block the device in AAD</span></span>|
|<span data-ttu-id="548fc-121">retirar</span><span class="sxs-lookup"><span data-stu-id="548fc-121">retire</span></span>|<span data-ttu-id="548fc-122">3</span><span class="sxs-lookup"><span data-stu-id="548fc-122">3</span></span>|<span data-ttu-id="548fc-123">Retirar el dispositivo</span><span class="sxs-lookup"><span data-stu-id="548fc-123">Retire the device</span></span>|
|<span data-ttu-id="548fc-124">Barrido</span><span class="sxs-lookup"><span data-stu-id="548fc-124">wipe</span></span>|<span data-ttu-id="548fc-125">4</span><span class="sxs-lookup"><span data-stu-id="548fc-125">4</span></span>|<span data-ttu-id="548fc-126">Borrar el dispositivo</span><span class="sxs-lookup"><span data-stu-id="548fc-126">Wipe the device</span></span>|
|<span data-ttu-id="548fc-127">removeResourceAccessProfiles</span><span class="sxs-lookup"><span data-stu-id="548fc-127">removeResourceAccessProfiles</span></span>|<span data-ttu-id="548fc-128">5</span><span class="sxs-lookup"><span data-stu-id="548fc-128">5</span></span>|<span data-ttu-id="548fc-129">Quitar perfiles de acceso a recursos del dispositivo</span><span class="sxs-lookup"><span data-stu-id="548fc-129">Remove Resource Access Profiles from the device</span></span>|
|<span data-ttu-id="548fc-130">pushNotification</span><span class="sxs-lookup"><span data-stu-id="548fc-130">pushNotification</span></span>|<span data-ttu-id="548fc-131">9</span><span class="sxs-lookup"><span data-stu-id="548fc-131">9</span></span>|<span data-ttu-id="548fc-132">Enviar notificación de inserción para dispositivos</span><span class="sxs-lookup"><span data-stu-id="548fc-132">Send push notification to device</span></span>|
|<span data-ttu-id="548fc-133">remoteLock</span><span class="sxs-lookup"><span data-stu-id="548fc-133">remoteLock</span></span>|<span data-ttu-id="548fc-134">10</span><span class="sxs-lookup"><span data-stu-id="548fc-134">10</span></span>|<span data-ttu-id="548fc-135">Bloquear el dispositivo de forma remota</span><span class="sxs-lookup"><span data-stu-id="548fc-135">Remotely lock the device</span></span>|





