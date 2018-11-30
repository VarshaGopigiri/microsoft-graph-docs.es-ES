---
title: tipo de enumeración emailSyncSchedule
description: Valores posibles para la programación de sincronización de correo electrónico.
ms.openlocfilehash: 48c5d433815d5f27d018d97ac479641146754669
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083302"
---
# <a name="emailsyncschedule-enum-type"></a><span data-ttu-id="0d185-103">tipo de enumeración emailSyncSchedule</span><span class="sxs-lookup"><span data-stu-id="0d185-103">emailSyncSchedule enum type</span></span>

> <span data-ttu-id="0d185-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0d185-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0d185-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0d185-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0d185-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0d185-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0d185-107">Valores posibles para la programación de sincronización de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0d185-107">Possible values for email sync schedule.</span></span>
## <a name="members"></a><span data-ttu-id="0d185-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d185-108">Members</span></span>
|<span data-ttu-id="0d185-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="0d185-109">Member</span></span>|<span data-ttu-id="0d185-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0d185-110">Value</span></span>|<span data-ttu-id="0d185-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d185-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0d185-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="0d185-112">userDefined</span></span>|<span data-ttu-id="0d185-113">0</span><span class="sxs-lookup"><span data-stu-id="0d185-113">0</span></span>|<span data-ttu-id="0d185-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="0d185-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="0d185-115">asMessagesArrive</span><span class="sxs-lookup"><span data-stu-id="0d185-115">asMessagesArrive</span></span>|<span data-ttu-id="0d185-116">1</span><span class="sxs-lookup"><span data-stu-id="0d185-116">1</span></span>|<span data-ttu-id="0d185-117">Sincronizar que llegan mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d185-117">Sync as messages arrive.</span></span>|
|<span data-ttu-id="0d185-118">Manual</span><span class="sxs-lookup"><span data-stu-id="0d185-118">manual</span></span>|<span data-ttu-id="0d185-119">2</span><span class="sxs-lookup"><span data-stu-id="0d185-119">2</span></span>|<span data-ttu-id="0d185-120">Sincronizar manualmente.</span><span class="sxs-lookup"><span data-stu-id="0d185-120">Sync manually.</span></span>|
|<span data-ttu-id="0d185-121">fifteenMinutes</span><span class="sxs-lookup"><span data-stu-id="0d185-121">fifteenMinutes</span></span>|<span data-ttu-id="0d185-122">3</span><span class="sxs-lookup"><span data-stu-id="0d185-122">3</span></span>|<span data-ttu-id="0d185-123">Sincronización de cada 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="0d185-123">Sync every fifteen minutes.</span></span>|
|<span data-ttu-id="0d185-124">thirtyMinutes</span><span class="sxs-lookup"><span data-stu-id="0d185-124">thirtyMinutes</span></span>|<span data-ttu-id="0d185-125">4</span><span class="sxs-lookup"><span data-stu-id="0d185-125">4</span></span>|<span data-ttu-id="0d185-126">Sincronización de cada 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="0d185-126">Sync every thirty minutes.</span></span>|
|<span data-ttu-id="0d185-127">sixtyMinutes</span><span class="sxs-lookup"><span data-stu-id="0d185-127">sixtyMinutes</span></span>|<span data-ttu-id="0d185-128">5</span><span class="sxs-lookup"><span data-stu-id="0d185-128">5</span></span>|<span data-ttu-id="0d185-129">Sincronización de cada 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="0d185-129">Sync every sixty minutes.</span></span>|
|<span data-ttu-id="0d185-130">basedOnMyUsage</span><span class="sxs-lookup"><span data-stu-id="0d185-130">basedOnMyUsage</span></span>|<span data-ttu-id="0d185-131">6</span><span class="sxs-lookup"><span data-stu-id="0d185-131">6</span></span>|<span data-ttu-id="0d185-132">Según mi uso de sincronización.</span><span class="sxs-lookup"><span data-stu-id="0d185-132">Sync based on my usage.</span></span>|





