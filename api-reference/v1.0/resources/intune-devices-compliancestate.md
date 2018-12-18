---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
author: tfitzmac
ms.openlocfilehash: 3045685518f1c7718f9a5f46cd10e0add6fe05b3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330278"
---
# <a name="compliancestate-enum-type"></a><span data-ttu-id="f151f-103">tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="f151f-103">complianceState enum type</span></span>

> <span data-ttu-id="f151f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f151f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f151f-105">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f151f-105">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="f151f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f151f-106">Members</span></span>
|<span data-ttu-id="f151f-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="f151f-107">Member</span></span>|<span data-ttu-id="f151f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f151f-108">Value</span></span>|<span data-ttu-id="f151f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f151f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f151f-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="f151f-110">unknown</span></span>|<span data-ttu-id="f151f-111">0</span><span class="sxs-lookup"><span data-stu-id="f151f-111">0</span></span>|<span data-ttu-id="f151f-112">Unknown (desconocido).</span><span class="sxs-lookup"><span data-stu-id="f151f-112">Unknown.</span></span>|
|<span data-ttu-id="f151f-113">compatible con</span><span class="sxs-lookup"><span data-stu-id="f151f-113">compliant</span></span>|<span data-ttu-id="f151f-114">1</span><span class="sxs-lookup"><span data-stu-id="f151f-114">1</span></span>|<span data-ttu-id="f151f-115">Compatible con.</span><span class="sxs-lookup"><span data-stu-id="f151f-115">Compliant.</span></span>|
|<span data-ttu-id="f151f-116">no compatible</span><span class="sxs-lookup"><span data-stu-id="f151f-116">noncompliant</span></span>|<span data-ttu-id="f151f-117">2</span><span class="sxs-lookup"><span data-stu-id="f151f-117">2</span></span>|<span data-ttu-id="f151f-118">Dispositivo no cumple y se bloquea de recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="f151f-118">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="f151f-119">conflicto</span><span class="sxs-lookup"><span data-stu-id="f151f-119">conflict</span></span>|<span data-ttu-id="f151f-120">3</span><span class="sxs-lookup"><span data-stu-id="f151f-120">3</span></span>|<span data-ttu-id="f151f-121">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="f151f-121">Conflict with other rules.</span></span>|
|<span data-ttu-id="f151f-122">error</span><span class="sxs-lookup"><span data-stu-id="f151f-122">error</span></span>|<span data-ttu-id="f151f-123">4</span><span class="sxs-lookup"><span data-stu-id="f151f-123">4</span></span>|<span data-ttu-id="f151f-124">Error</span><span class="sxs-lookup"><span data-stu-id="f151f-124">Error.</span></span>|
|<span data-ttu-id="f151f-125">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="f151f-125">inGracePeriod</span></span>|<span data-ttu-id="f151f-126">254</span><span class="sxs-lookup"><span data-stu-id="f151f-126">254</span></span>|<span data-ttu-id="f151f-127">Dispositivo no cumple pero todavía tiene acceso a recursos corporativos</span><span class="sxs-lookup"><span data-stu-id="f151f-127">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="f151f-128">configManager</span><span class="sxs-lookup"><span data-stu-id="f151f-128">configManager</span></span>|<span data-ttu-id="f151f-129">255</span><span class="sxs-lookup"><span data-stu-id="f151f-129">255</span></span>|<span data-ttu-id="f151f-130">Administrado por el Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="f151f-130">Managed by Config Manager</span></span>|



