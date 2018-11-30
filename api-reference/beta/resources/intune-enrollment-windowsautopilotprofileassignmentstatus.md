---
title: tipo de enumeración windowsAutopilotProfileAssignmentStatus
description: Todavía no documentado
ms.openlocfilehash: 0ec6dfaa6dbc87fe1d38a495ac177a84e70796a7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083283"
---
# <a name="windowsautopilotprofileassignmentstatus-enum-type"></a><span data-ttu-id="19bbd-103">tipo de enumeración windowsAutopilotProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="19bbd-103">windowsAutopilotProfileAssignmentStatus enum type</span></span>

> <span data-ttu-id="19bbd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19bbd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19bbd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19bbd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="19bbd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="19bbd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="19bbd-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="19bbd-107">Not yet documented</span></span>
## <a name="members"></a><span data-ttu-id="19bbd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="19bbd-108">Members</span></span>
|<span data-ttu-id="19bbd-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="19bbd-109">Member</span></span>|<span data-ttu-id="19bbd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="19bbd-110">Value</span></span>|<span data-ttu-id="19bbd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="19bbd-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="19bbd-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="19bbd-112">unknown</span></span>|<span data-ttu-id="19bbd-113">0</span><span class="sxs-lookup"><span data-stu-id="19bbd-113">0</span></span>|<span data-ttu-id="19bbd-114">Estado de asignación desconocido</span><span class="sxs-lookup"><span data-stu-id="19bbd-114">Unknown assignment status</span></span>|
|<span data-ttu-id="19bbd-115">assignedInSync</span><span class="sxs-lookup"><span data-stu-id="19bbd-115">assignedInSync</span></span>|<span data-ttu-id="19bbd-116">1</span><span class="sxs-lookup"><span data-stu-id="19bbd-116">1</span></span>|<span data-ttu-id="19bbd-117">Asignados correctamente en Intune y sincronización con programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="19bbd-117">Assigned successfully in Intune and in sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="19bbd-118">assignedOutOfSync</span><span class="sxs-lookup"><span data-stu-id="19bbd-118">assignedOutOfSync</span></span>|<span data-ttu-id="19bbd-119">2</span><span class="sxs-lookup"><span data-stu-id="19bbd-119">2</span></span>|<span data-ttu-id="19bbd-120">Asignado correctamente en Intune y no sincronizados con el programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="19bbd-120">Assigned successfully in Intune and not in sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="19bbd-121">assignedUnkownSyncState</span><span class="sxs-lookup"><span data-stu-id="19bbd-121">assignedUnkownSyncState</span></span>|<span data-ttu-id="19bbd-122">3</span><span class="sxs-lookup"><span data-stu-id="19bbd-122">3</span></span>|<span data-ttu-id="19bbd-123">Asignado correctamente en Intune y la sincronización en o fuera de la sincronización con el programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="19bbd-123">Assigned successfully in Intune and either in-sync or out of sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="19bbd-124">no asignado</span><span class="sxs-lookup"><span data-stu-id="19bbd-124">notAssigned</span></span>|<span data-ttu-id="19bbd-125">4</span><span class="sxs-lookup"><span data-stu-id="19bbd-125">4</span></span>|<span data-ttu-id="19bbd-126">No asignado</span><span class="sxs-lookup"><span data-stu-id="19bbd-126">Not assigned</span></span>|
|<span data-ttu-id="19bbd-127">pendiente</span><span class="sxs-lookup"><span data-stu-id="19bbd-127">pending</span></span>|<span data-ttu-id="19bbd-128">5</span><span class="sxs-lookup"><span data-stu-id="19bbd-128">5</span></span>|<span data-ttu-id="19bbd-129">Asignación pendiente</span><span class="sxs-lookup"><span data-stu-id="19bbd-129">Pending assignment</span></span>|
|<span data-ttu-id="19bbd-130">failed</span><span class="sxs-lookup"><span data-stu-id="19bbd-130">failed</span></span>|<span data-ttu-id="19bbd-131">6</span><span class="sxs-lookup"><span data-stu-id="19bbd-131">6</span></span>| <span data-ttu-id="19bbd-132">Error de asignación</span><span class="sxs-lookup"><span data-stu-id="19bbd-132">Assignment failed</span></span>|





