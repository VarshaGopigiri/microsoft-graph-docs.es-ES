---
title: tipo de enumeración windowsAutopilotProfileAssignmentStatus
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 255aab9770305baa29e73278b3bfceec1079351a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321003"
---
# <a name="windowsautopilotprofileassignmentstatus-enum-type"></a><span data-ttu-id="25482-103">tipo de enumeración windowsAutopilotProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="25482-103">windowsAutopilotProfileAssignmentStatus enum type</span></span>

> <span data-ttu-id="25482-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25482-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25482-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25482-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="25482-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25482-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25482-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="25482-107">Not yet documented</span></span>
## <a name="members"></a><span data-ttu-id="25482-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="25482-108">Members</span></span>
|<span data-ttu-id="25482-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="25482-109">Member</span></span>|<span data-ttu-id="25482-110">Valor</span><span class="sxs-lookup"><span data-stu-id="25482-110">Value</span></span>|<span data-ttu-id="25482-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="25482-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25482-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="25482-112">unknown</span></span>|<span data-ttu-id="25482-113">0</span><span class="sxs-lookup"><span data-stu-id="25482-113">0</span></span>|<span data-ttu-id="25482-114">Estado de asignación desconocido</span><span class="sxs-lookup"><span data-stu-id="25482-114">Unknown assignment status</span></span>|
|<span data-ttu-id="25482-115">assignedInSync</span><span class="sxs-lookup"><span data-stu-id="25482-115">assignedInSync</span></span>|<span data-ttu-id="25482-116">1</span><span class="sxs-lookup"><span data-stu-id="25482-116">1</span></span>|<span data-ttu-id="25482-117">Asignados correctamente en Intune y sincronización con programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="25482-117">Assigned successfully in Intune and in sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="25482-118">assignedOutOfSync</span><span class="sxs-lookup"><span data-stu-id="25482-118">assignedOutOfSync</span></span>|<span data-ttu-id="25482-119">2</span><span class="sxs-lookup"><span data-stu-id="25482-119">2</span></span>|<span data-ttu-id="25482-120">Asignado correctamente en Intune y no sincronizados con el programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="25482-120">Assigned successfully in Intune and not in sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="25482-121">assignedUnkownSyncState</span><span class="sxs-lookup"><span data-stu-id="25482-121">assignedUnkownSyncState</span></span>|<span data-ttu-id="25482-122">3</span><span class="sxs-lookup"><span data-stu-id="25482-122">3</span></span>|<span data-ttu-id="25482-123">Asignado correctamente en Intune y la sincronización en o fuera de la sincronización con el programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="25482-123">Assigned successfully in Intune and either in-sync or out of sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="25482-124">no asignado</span><span class="sxs-lookup"><span data-stu-id="25482-124">notAssigned</span></span>|<span data-ttu-id="25482-125">4</span><span class="sxs-lookup"><span data-stu-id="25482-125">4</span></span>|<span data-ttu-id="25482-126">No asignado</span><span class="sxs-lookup"><span data-stu-id="25482-126">Not assigned</span></span>|
|<span data-ttu-id="25482-127">pendiente</span><span class="sxs-lookup"><span data-stu-id="25482-127">pending</span></span>|<span data-ttu-id="25482-128">5</span><span class="sxs-lookup"><span data-stu-id="25482-128">5</span></span>|<span data-ttu-id="25482-129">Asignación pendiente</span><span class="sxs-lookup"><span data-stu-id="25482-129">Pending assignment</span></span>|
|<span data-ttu-id="25482-130">failed</span><span class="sxs-lookup"><span data-stu-id="25482-130">failed</span></span>|<span data-ttu-id="25482-131">6</span><span class="sxs-lookup"><span data-stu-id="25482-131">6</span></span>| <span data-ttu-id="25482-132">Error de asignación</span><span class="sxs-lookup"><span data-stu-id="25482-132">Assignment failed</span></span>|





