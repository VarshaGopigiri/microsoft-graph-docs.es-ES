---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5a4f4c359665eb1a0087f64802b5e7c829002fd6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940200"
---
# <a name="compliancestate-enum-type"></a><span data-ttu-id="f93ef-103">tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="f93ef-103">complianceState enum type</span></span>

> <span data-ttu-id="f93ef-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f93ef-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f93ef-105">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f93ef-105">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="f93ef-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f93ef-106">Members</span></span>
|<span data-ttu-id="f93ef-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="f93ef-107">Member</span></span>|<span data-ttu-id="f93ef-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f93ef-108">Value</span></span>|<span data-ttu-id="f93ef-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f93ef-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f93ef-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="f93ef-110">unknown</span></span>|<span data-ttu-id="f93ef-111">0</span><span class="sxs-lookup"><span data-stu-id="f93ef-111">0</span></span>|<span data-ttu-id="f93ef-112">Unknown (desconocido).</span><span class="sxs-lookup"><span data-stu-id="f93ef-112">Unknown.</span></span>|
|<span data-ttu-id="f93ef-113">compatible con</span><span class="sxs-lookup"><span data-stu-id="f93ef-113">compliant</span></span>|<span data-ttu-id="f93ef-114">1</span><span class="sxs-lookup"><span data-stu-id="f93ef-114">1</span></span>|<span data-ttu-id="f93ef-115">Compatible con.</span><span class="sxs-lookup"><span data-stu-id="f93ef-115">Compliant.</span></span>|
|<span data-ttu-id="f93ef-116">no compatible</span><span class="sxs-lookup"><span data-stu-id="f93ef-116">noncompliant</span></span>|<span data-ttu-id="f93ef-117">2</span><span class="sxs-lookup"><span data-stu-id="f93ef-117">2</span></span>|<span data-ttu-id="f93ef-118">Dispositivo no cumple y se bloquea de recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="f93ef-118">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="f93ef-119">conflicto</span><span class="sxs-lookup"><span data-stu-id="f93ef-119">conflict</span></span>|<span data-ttu-id="f93ef-120">3</span><span class="sxs-lookup"><span data-stu-id="f93ef-120">3</span></span>|<span data-ttu-id="f93ef-121">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="f93ef-121">Conflict with other rules.</span></span>|
|<span data-ttu-id="f93ef-122">error</span><span class="sxs-lookup"><span data-stu-id="f93ef-122">error</span></span>|<span data-ttu-id="f93ef-123">4</span><span class="sxs-lookup"><span data-stu-id="f93ef-123">4</span></span>|<span data-ttu-id="f93ef-124">Error</span><span class="sxs-lookup"><span data-stu-id="f93ef-124">Error.</span></span>|
|<span data-ttu-id="f93ef-125">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="f93ef-125">inGracePeriod</span></span>|<span data-ttu-id="f93ef-126">254</span><span class="sxs-lookup"><span data-stu-id="f93ef-126">254</span></span>|<span data-ttu-id="f93ef-127">Dispositivo no cumple pero todavía tiene acceso a recursos corporativos</span><span class="sxs-lookup"><span data-stu-id="f93ef-127">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="f93ef-128">configManager</span><span class="sxs-lookup"><span data-stu-id="f93ef-128">configManager</span></span>|<span data-ttu-id="f93ef-129">255</span><span class="sxs-lookup"><span data-stu-id="f93ef-129">255</span></span>|<span data-ttu-id="f93ef-130">Administrado por el Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="f93ef-130">Managed by Config Manager</span></span>|



