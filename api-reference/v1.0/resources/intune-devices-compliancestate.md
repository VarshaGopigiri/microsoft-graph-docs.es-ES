---
title: tipo de enumeración complianceState
description: Estado de cumplimiento.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 53b17f258f577e0842dbfc81c6341303f6b43799
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820345"
---
# <a name="compliancestate-enum-type"></a><span data-ttu-id="bf2ec-103">tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="bf2ec-103">complianceState enum type</span></span>

> <span data-ttu-id="bf2ec-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf2ec-105">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-105">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="bf2ec-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf2ec-106">Members</span></span>
|<span data-ttu-id="bf2ec-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="bf2ec-107">Member</span></span>|<span data-ttu-id="bf2ec-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2ec-108">Value</span></span>|<span data-ttu-id="bf2ec-109">Description</span><span class="sxs-lookup"><span data-stu-id="bf2ec-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf2ec-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="bf2ec-110">unknown</span></span>|<span data-ttu-id="bf2ec-111">0</span><span class="sxs-lookup"><span data-stu-id="bf2ec-111">0</span></span>|<span data-ttu-id="bf2ec-112">Unknown (desconocido).</span><span class="sxs-lookup"><span data-stu-id="bf2ec-112">Unknown.</span></span>|
|<span data-ttu-id="bf2ec-113">compatible con</span><span class="sxs-lookup"><span data-stu-id="bf2ec-113">compliant</span></span>|<span data-ttu-id="bf2ec-114">1</span><span class="sxs-lookup"><span data-stu-id="bf2ec-114">1</span></span>|<span data-ttu-id="bf2ec-115">Compatible con.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-115">Compliant.</span></span>|
|<span data-ttu-id="bf2ec-116">no compatible</span><span class="sxs-lookup"><span data-stu-id="bf2ec-116">noncompliant</span></span>|<span data-ttu-id="bf2ec-117">2</span><span class="sxs-lookup"><span data-stu-id="bf2ec-117">2</span></span>|<span data-ttu-id="bf2ec-118">Dispositivo no cumple y se bloquea de recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-118">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="bf2ec-119">conflicto</span><span class="sxs-lookup"><span data-stu-id="bf2ec-119">conflict</span></span>|<span data-ttu-id="bf2ec-120">3</span><span class="sxs-lookup"><span data-stu-id="bf2ec-120">3</span></span>|<span data-ttu-id="bf2ec-121">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-121">Conflict with other rules.</span></span>|
|<span data-ttu-id="bf2ec-122">error</span><span class="sxs-lookup"><span data-stu-id="bf2ec-122">error</span></span>|<span data-ttu-id="bf2ec-123">4</span><span class="sxs-lookup"><span data-stu-id="bf2ec-123">4</span></span>|<span data-ttu-id="bf2ec-124">Error</span><span class="sxs-lookup"><span data-stu-id="bf2ec-124">Error.</span></span>|
|<span data-ttu-id="bf2ec-125">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="bf2ec-125">inGracePeriod</span></span>|<span data-ttu-id="bf2ec-126">254</span><span class="sxs-lookup"><span data-stu-id="bf2ec-126">254</span></span>|<span data-ttu-id="bf2ec-127">Dispositivo no cumple pero todavía tiene acceso a recursos corporativos</span><span class="sxs-lookup"><span data-stu-id="bf2ec-127">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="bf2ec-128">configManager</span><span class="sxs-lookup"><span data-stu-id="bf2ec-128">configManager</span></span>|<span data-ttu-id="bf2ec-129">255</span><span class="sxs-lookup"><span data-stu-id="bf2ec-129">255</span></span>|<span data-ttu-id="bf2ec-130">Administrado por el Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bf2ec-130">Managed by Config Manager</span></span>|



