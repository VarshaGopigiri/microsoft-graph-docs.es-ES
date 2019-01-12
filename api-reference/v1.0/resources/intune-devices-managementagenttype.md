---
title: tipo de enumeración managementAgentType
description: Tipo de agente de administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b76231a2781a153c5384c1dc3efdf8facec04dcc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966170"
---
# <a name="managementagenttype-enum-type"></a><span data-ttu-id="970c5-103">tipo de enumeración managementAgentType</span><span class="sxs-lookup"><span data-stu-id="970c5-103">managementAgentType enum type</span></span>

> <span data-ttu-id="970c5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="970c5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="970c5-105">Tipo de agente de administración.</span><span class="sxs-lookup"><span data-stu-id="970c5-105">Management agent type.</span></span>
## <a name="members"></a><span data-ttu-id="970c5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="970c5-106">Members</span></span>
|<span data-ttu-id="970c5-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="970c5-107">Member</span></span>|<span data-ttu-id="970c5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="970c5-108">Value</span></span>|<span data-ttu-id="970c5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="970c5-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="970c5-110">EAS</span><span class="sxs-lookup"><span data-stu-id="970c5-110">eas</span></span>|<span data-ttu-id="970c5-111">1</span><span class="sxs-lookup"><span data-stu-id="970c5-111">1</span></span>|<span data-ttu-id="970c5-112">El dispositivo se administra mediante Exchange server.</span><span class="sxs-lookup"><span data-stu-id="970c5-112">The device is managed by Exchange server.</span></span>|
|<span data-ttu-id="970c5-113">MDM</span><span class="sxs-lookup"><span data-stu-id="970c5-113">mdm</span></span>|<span data-ttu-id="970c5-114">2</span><span class="sxs-lookup"><span data-stu-id="970c5-114">2</span></span>|<span data-ttu-id="970c5-115">El dispositivo se administra mediante la Intune MDM.</span><span class="sxs-lookup"><span data-stu-id="970c5-115">The device is managed by Intune MDM.</span></span>|
|<span data-ttu-id="970c5-116">easMdm</span><span class="sxs-lookup"><span data-stu-id="970c5-116">easMdm</span></span>|<span data-ttu-id="970c5-117">3</span><span class="sxs-lookup"><span data-stu-id="970c5-117">3</span></span>|<span data-ttu-id="970c5-118">El dispositivo se administra mediante Exchange server y MDM. Intune</span><span class="sxs-lookup"><span data-stu-id="970c5-118">The device is managed by both Exchange server and Intune MDM.</span></span>|
|<span data-ttu-id="970c5-119">intuneClient</span><span class="sxs-lookup"><span data-stu-id="970c5-119">intuneClient</span></span>|<span data-ttu-id="970c5-120">4</span><span class="sxs-lookup"><span data-stu-id="970c5-120">4</span></span>|<span data-ttu-id="970c5-121">Intune administrados de cliente.</span><span class="sxs-lookup"><span data-stu-id="970c5-121">Intune client managed.</span></span>|
|<span data-ttu-id="970c5-122">easIntuneClient</span><span class="sxs-lookup"><span data-stu-id="970c5-122">easIntuneClient</span></span>|<span data-ttu-id="970c5-123">5</span><span class="sxs-lookup"><span data-stu-id="970c5-123">5</span></span>|<span data-ttu-id="970c5-124">El dispositivo está EAS y Intune administrados de cliente dual.</span><span class="sxs-lookup"><span data-stu-id="970c5-124">The device is EAS and Intune client dual managed.</span></span>|
|<span data-ttu-id="970c5-125">configurationManagerClient</span><span class="sxs-lookup"><span data-stu-id="970c5-125">configurationManagerClient</span></span>|<span data-ttu-id="970c5-126">8</span><span class="sxs-lookup"><span data-stu-id="970c5-126">8</span></span>|<span data-ttu-id="970c5-127">El dispositivo se administra mediante el Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="970c5-127">The device is managed by Configuration Manager.</span></span>|
|<span data-ttu-id="970c5-128">configurationManagerClientMdm</span><span class="sxs-lookup"><span data-stu-id="970c5-128">configurationManagerClientMdm</span></span>|<span data-ttu-id="970c5-129">10</span><span class="sxs-lookup"><span data-stu-id="970c5-129">10</span></span>|<span data-ttu-id="970c5-130">El dispositivo está administrado por el Administrador de configuración y MDM.</span><span class="sxs-lookup"><span data-stu-id="970c5-130">The device is managed by Configuration Manager and MDM.</span></span>|
|<span data-ttu-id="970c5-131">configurationManagerClientMdmEas</span><span class="sxs-lookup"><span data-stu-id="970c5-131">configurationManagerClientMdmEas</span></span>|<span data-ttu-id="970c5-132">11</span><span class="sxs-lookup"><span data-stu-id="970c5-132">11</span></span>|<span data-ttu-id="970c5-133">El dispositivo está administrado por el Administrador de configuración, MDM y Eas.</span><span class="sxs-lookup"><span data-stu-id="970c5-133">The device is managed by Configuration Manager, MDM and Eas.</span></span>|
|<span data-ttu-id="970c5-134">desconocido</span><span class="sxs-lookup"><span data-stu-id="970c5-134">unknown</span></span>|<span data-ttu-id="970c5-135">16</span><span class="sxs-lookup"><span data-stu-id="970c5-135">16</span></span>|<span data-ttu-id="970c5-136">Tipo de agente de administración desconocido.</span><span class="sxs-lookup"><span data-stu-id="970c5-136">Unknown management agent type.</span></span>|
|<span data-ttu-id="970c5-137">jamf</span><span class="sxs-lookup"><span data-stu-id="970c5-137">jamf</span></span>|<span data-ttu-id="970c5-138">32</span><span class="sxs-lookup"><span data-stu-id="970c5-138">32</span></span>|<span data-ttu-id="970c5-139">Los atributos del dispositivo se obtienen de Jamf.</span><span class="sxs-lookup"><span data-stu-id="970c5-139">The device attributes are fetched from Jamf.</span></span>|
|<span data-ttu-id="970c5-140">googleCloudDevicePolicyController</span><span class="sxs-lookup"><span data-stu-id="970c5-140">googleCloudDevicePolicyController</span></span>|<span data-ttu-id="970c5-141">64</span><span class="sxs-lookup"><span data-stu-id="970c5-141">64</span></span>|<span data-ttu-id="970c5-142">El dispositivo se administra mediante CloudDPC de Google.</span><span class="sxs-lookup"><span data-stu-id="970c5-142">The device is managed by Google's CloudDPC.</span></span>|



