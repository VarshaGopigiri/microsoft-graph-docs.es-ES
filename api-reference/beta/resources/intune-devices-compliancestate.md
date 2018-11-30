---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
ms.openlocfilehash: c49c0ecc2511f612e743fb5d86a53d150d3fbf45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089427"
---
# <a name="compliancestate-enum-type"></a><span data-ttu-id="99e8a-103">tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="99e8a-103">complianceState enum type</span></span>

> <span data-ttu-id="99e8a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99e8a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99e8a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99e8a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="99e8a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="99e8a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="99e8a-107">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="99e8a-107">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="99e8a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="99e8a-108">Members</span></span>
|<span data-ttu-id="99e8a-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="99e8a-109">Member</span></span>|<span data-ttu-id="99e8a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="99e8a-110">Value</span></span>|<span data-ttu-id="99e8a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="99e8a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="99e8a-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="99e8a-112">unknown</span></span>|<span data-ttu-id="99e8a-113">0</span><span class="sxs-lookup"><span data-stu-id="99e8a-113">0</span></span>|<span data-ttu-id="99e8a-114">Unknown (desconocido).</span><span class="sxs-lookup"><span data-stu-id="99e8a-114">Unknown.</span></span>|
|<span data-ttu-id="99e8a-115">compatible con</span><span class="sxs-lookup"><span data-stu-id="99e8a-115">compliant</span></span>|<span data-ttu-id="99e8a-116">1</span><span class="sxs-lookup"><span data-stu-id="99e8a-116">1</span></span>|<span data-ttu-id="99e8a-117">Compatible con.</span><span class="sxs-lookup"><span data-stu-id="99e8a-117">Compliant.</span></span>|
|<span data-ttu-id="99e8a-118">no compatible</span><span class="sxs-lookup"><span data-stu-id="99e8a-118">noncompliant</span></span>|<span data-ttu-id="99e8a-119">2</span><span class="sxs-lookup"><span data-stu-id="99e8a-119">2</span></span>|<span data-ttu-id="99e8a-120">Dispositivo no cumple y se bloquea de recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="99e8a-120">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="99e8a-121">conflicto</span><span class="sxs-lookup"><span data-stu-id="99e8a-121">conflict</span></span>|<span data-ttu-id="99e8a-122">3</span><span class="sxs-lookup"><span data-stu-id="99e8a-122">3</span></span>|<span data-ttu-id="99e8a-123">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="99e8a-123">Conflict with other rules.</span></span>|
|<span data-ttu-id="99e8a-124">error</span><span class="sxs-lookup"><span data-stu-id="99e8a-124">error</span></span>|<span data-ttu-id="99e8a-125">4</span><span class="sxs-lookup"><span data-stu-id="99e8a-125">4</span></span>|<span data-ttu-id="99e8a-126">Error</span><span class="sxs-lookup"><span data-stu-id="99e8a-126">Error.</span></span>|
|<span data-ttu-id="99e8a-127">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="99e8a-127">inGracePeriod</span></span>|<span data-ttu-id="99e8a-128">254</span><span class="sxs-lookup"><span data-stu-id="99e8a-128">254</span></span>|<span data-ttu-id="99e8a-129">Dispositivo no cumple pero todavía tiene acceso a recursos corporativos</span><span class="sxs-lookup"><span data-stu-id="99e8a-129">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="99e8a-130">configManager</span><span class="sxs-lookup"><span data-stu-id="99e8a-130">configManager</span></span>|<span data-ttu-id="99e8a-131">255</span><span class="sxs-lookup"><span data-stu-id="99e8a-131">255</span></span>|<span data-ttu-id="99e8a-132">Administrado por el Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="99e8a-132">Managed by Config Manager</span></span>|





