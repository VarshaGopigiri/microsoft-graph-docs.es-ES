---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b3d496d6890d0da4d817ad9ba1f03e4b0825204d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861680"
---
# <a name="compliancestate-enum-type"></a><span data-ttu-id="bf1c4-103">tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="bf1c4-103">complianceState enum type</span></span>

> <span data-ttu-id="bf1c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf1c4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bf1c4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf1c4-107">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-107">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="bf1c4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf1c4-108">Members</span></span>
|<span data-ttu-id="bf1c4-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="bf1c4-109">Member</span></span>|<span data-ttu-id="bf1c4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="bf1c4-110">Value</span></span>|<span data-ttu-id="bf1c4-111">Description</span><span class="sxs-lookup"><span data-stu-id="bf1c4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf1c4-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="bf1c4-112">unknown</span></span>|<span data-ttu-id="bf1c4-113">0</span><span class="sxs-lookup"><span data-stu-id="bf1c4-113">0</span></span>|<span data-ttu-id="bf1c4-114">Unknown (desconocido).</span><span class="sxs-lookup"><span data-stu-id="bf1c4-114">Unknown.</span></span>|
|<span data-ttu-id="bf1c4-115">compatible con</span><span class="sxs-lookup"><span data-stu-id="bf1c4-115">compliant</span></span>|<span data-ttu-id="bf1c4-116">1</span><span class="sxs-lookup"><span data-stu-id="bf1c4-116">1</span></span>|<span data-ttu-id="bf1c4-117">Compatible con.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-117">Compliant.</span></span>|
|<span data-ttu-id="bf1c4-118">no compatible</span><span class="sxs-lookup"><span data-stu-id="bf1c4-118">noncompliant</span></span>|<span data-ttu-id="bf1c4-119">2</span><span class="sxs-lookup"><span data-stu-id="bf1c4-119">2</span></span>|<span data-ttu-id="bf1c4-120">Dispositivo no cumple y se bloquea de recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-120">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="bf1c4-121">conflicto</span><span class="sxs-lookup"><span data-stu-id="bf1c4-121">conflict</span></span>|<span data-ttu-id="bf1c4-122">3</span><span class="sxs-lookup"><span data-stu-id="bf1c4-122">3</span></span>|<span data-ttu-id="bf1c4-123">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="bf1c4-123">Conflict with other rules.</span></span>|
|<span data-ttu-id="bf1c4-124">error</span><span class="sxs-lookup"><span data-stu-id="bf1c4-124">error</span></span>|<span data-ttu-id="bf1c4-125">4</span><span class="sxs-lookup"><span data-stu-id="bf1c4-125">4</span></span>|<span data-ttu-id="bf1c4-126">Error</span><span class="sxs-lookup"><span data-stu-id="bf1c4-126">Error.</span></span>|
|<span data-ttu-id="bf1c4-127">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="bf1c4-127">inGracePeriod</span></span>|<span data-ttu-id="bf1c4-128">254</span><span class="sxs-lookup"><span data-stu-id="bf1c4-128">254</span></span>|<span data-ttu-id="bf1c4-129">Dispositivo no cumple pero todavía tiene acceso a recursos corporativos</span><span class="sxs-lookup"><span data-stu-id="bf1c4-129">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="bf1c4-130">configManager</span><span class="sxs-lookup"><span data-stu-id="bf1c4-130">configManager</span></span>|<span data-ttu-id="bf1c4-131">255</span><span class="sxs-lookup"><span data-stu-id="bf1c4-131">255</span></span>|<span data-ttu-id="bf1c4-132">Administrado por el Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bf1c4-132">Managed by Config Manager</span></span>|





