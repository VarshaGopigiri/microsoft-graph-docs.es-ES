---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
ms.openlocfilehash: 041a2267b952d37e0aeef29e1325e5cb7b561ed7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032047"
---
# <a name="compliancestate-enum-type"></a><span data-ttu-id="bbae1-103">tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="bbae1-103">complianceState enum type</span></span>

> <span data-ttu-id="bbae1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bbae1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bbae1-105">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="bbae1-105">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="bbae1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbae1-106">Members</span></span>
|<span data-ttu-id="bbae1-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="bbae1-107">Member</span></span>|<span data-ttu-id="bbae1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bbae1-108">Value</span></span>|<span data-ttu-id="bbae1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbae1-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bbae1-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="bbae1-110">unknown</span></span>|<span data-ttu-id="bbae1-111">0</span><span class="sxs-lookup"><span data-stu-id="bbae1-111">0</span></span>|<span data-ttu-id="bbae1-112">Unknown (desconocido).</span><span class="sxs-lookup"><span data-stu-id="bbae1-112">Unknown.</span></span>|
|<span data-ttu-id="bbae1-113">compatible con</span><span class="sxs-lookup"><span data-stu-id="bbae1-113">compliant</span></span>|<span data-ttu-id="bbae1-114">1</span><span class="sxs-lookup"><span data-stu-id="bbae1-114">1</span></span>|<span data-ttu-id="bbae1-115">Compatible con.</span><span class="sxs-lookup"><span data-stu-id="bbae1-115">Compliant.</span></span>|
|<span data-ttu-id="bbae1-116">no compatible</span><span class="sxs-lookup"><span data-stu-id="bbae1-116">noncompliant</span></span>|<span data-ttu-id="bbae1-117">2</span><span class="sxs-lookup"><span data-stu-id="bbae1-117">2</span></span>|<span data-ttu-id="bbae1-118">Dispositivo no cumple y se bloquea de recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="bbae1-118">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="bbae1-119">conflicto</span><span class="sxs-lookup"><span data-stu-id="bbae1-119">conflict</span></span>|<span data-ttu-id="bbae1-120">3</span><span class="sxs-lookup"><span data-stu-id="bbae1-120">3</span></span>|<span data-ttu-id="bbae1-121">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="bbae1-121">Conflict with other rules.</span></span>|
|<span data-ttu-id="bbae1-122">error</span><span class="sxs-lookup"><span data-stu-id="bbae1-122">error</span></span>|<span data-ttu-id="bbae1-123">4</span><span class="sxs-lookup"><span data-stu-id="bbae1-123">4</span></span>|<span data-ttu-id="bbae1-124">Error</span><span class="sxs-lookup"><span data-stu-id="bbae1-124">Error.</span></span>|
|<span data-ttu-id="bbae1-125">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="bbae1-125">inGracePeriod</span></span>|<span data-ttu-id="bbae1-126">254</span><span class="sxs-lookup"><span data-stu-id="bbae1-126">254</span></span>|<span data-ttu-id="bbae1-127">Dispositivo no cumple pero todavía tiene acceso a recursos corporativos</span><span class="sxs-lookup"><span data-stu-id="bbae1-127">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="bbae1-128">configManager</span><span class="sxs-lookup"><span data-stu-id="bbae1-128">configManager</span></span>|<span data-ttu-id="bbae1-129">255</span><span class="sxs-lookup"><span data-stu-id="bbae1-129">255</span></span>|<span data-ttu-id="bbae1-130">Administrado por el Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bbae1-130">Managed by Config Manager</span></span>|



