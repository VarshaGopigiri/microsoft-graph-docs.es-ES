---
title: tipo de enumeración windowsAutopilotProfileAssignmentStatus
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1427ffeb45862312d92fdf02a00a242725894d36
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962635"
---
# <a name="windowsautopilotprofileassignmentstatus-enum-type"></a><span data-ttu-id="1e081-103">tipo de enumeración windowsAutopilotProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="1e081-103">windowsAutopilotProfileAssignmentStatus enum type</span></span>

> <span data-ttu-id="1e081-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e081-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e081-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e081-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1e081-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1e081-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1e081-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1e081-107">Not yet documented</span></span>
## <a name="members"></a><span data-ttu-id="1e081-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e081-108">Members</span></span>
|<span data-ttu-id="1e081-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="1e081-109">Member</span></span>|<span data-ttu-id="1e081-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1e081-110">Value</span></span>|<span data-ttu-id="1e081-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e081-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1e081-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="1e081-112">unknown</span></span>|<span data-ttu-id="1e081-113">0</span><span class="sxs-lookup"><span data-stu-id="1e081-113">0</span></span>|<span data-ttu-id="1e081-114">Estado de asignación desconocido</span><span class="sxs-lookup"><span data-stu-id="1e081-114">Unknown assignment status</span></span>|
|<span data-ttu-id="1e081-115">assignedInSync</span><span class="sxs-lookup"><span data-stu-id="1e081-115">assignedInSync</span></span>|<span data-ttu-id="1e081-116">1</span><span class="sxs-lookup"><span data-stu-id="1e081-116">1</span></span>|<span data-ttu-id="1e081-117">Asignados correctamente en Intune y sincronización con programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="1e081-117">Assigned successfully in Intune and in sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="1e081-118">assignedOutOfSync</span><span class="sxs-lookup"><span data-stu-id="1e081-118">assignedOutOfSync</span></span>|<span data-ttu-id="1e081-119">2</span><span class="sxs-lookup"><span data-stu-id="1e081-119">2</span></span>|<span data-ttu-id="1e081-120">Asignado correctamente en Intune y no sincronizados con el programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="1e081-120">Assigned successfully in Intune and not in sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="1e081-121">assignedUnkownSyncState</span><span class="sxs-lookup"><span data-stu-id="1e081-121">assignedUnkownSyncState</span></span>|<span data-ttu-id="1e081-122">3</span><span class="sxs-lookup"><span data-stu-id="1e081-122">3</span></span>|<span data-ttu-id="1e081-123">Asignado correctamente en Intune y la sincronización en o fuera de la sincronización con el programa piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="1e081-123">Assigned successfully in Intune and either in-sync or out of sync with Windows auto pilot program</span></span>|
|<span data-ttu-id="1e081-124">no asignado</span><span class="sxs-lookup"><span data-stu-id="1e081-124">notAssigned</span></span>|<span data-ttu-id="1e081-125">4</span><span class="sxs-lookup"><span data-stu-id="1e081-125">4</span></span>|<span data-ttu-id="1e081-126">No asignado</span><span class="sxs-lookup"><span data-stu-id="1e081-126">Not assigned</span></span>|
|<span data-ttu-id="1e081-127">pendiente</span><span class="sxs-lookup"><span data-stu-id="1e081-127">pending</span></span>|<span data-ttu-id="1e081-128">5</span><span class="sxs-lookup"><span data-stu-id="1e081-128">5</span></span>|<span data-ttu-id="1e081-129">Asignación pendiente</span><span class="sxs-lookup"><span data-stu-id="1e081-129">Pending assignment</span></span>|
|<span data-ttu-id="1e081-130">failed</span><span class="sxs-lookup"><span data-stu-id="1e081-130">failed</span></span>|<span data-ttu-id="1e081-131">6</span><span class="sxs-lookup"><span data-stu-id="1e081-131">6</span></span>| <span data-ttu-id="1e081-132">Error de asignación</span><span class="sxs-lookup"><span data-stu-id="1e081-132">Assignment failed</span></span>|





