---
title: tipo de enumeración managementAgentType
description: Tipo de agente de administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1711ad647afabc2b8877bd2f99b049bd1c1dd4e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914286"
---
# <a name="managementagenttype-enum-type"></a><span data-ttu-id="7b1b1-103">tipo de enumeración managementAgentType</span><span class="sxs-lookup"><span data-stu-id="7b1b1-103">managementAgentType enum type</span></span>

> <span data-ttu-id="7b1b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b1b1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7b1b1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7b1b1-107">Tipo de agente de administración.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-107">Management agent type.</span></span>
## <a name="members"></a><span data-ttu-id="7b1b1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b1b1-108">Members</span></span>
|<span data-ttu-id="7b1b1-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="7b1b1-109">Member</span></span>|<span data-ttu-id="7b1b1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7b1b1-110">Value</span></span>|<span data-ttu-id="7b1b1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b1b1-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7b1b1-112">EAS</span><span class="sxs-lookup"><span data-stu-id="7b1b1-112">eas</span></span>|<span data-ttu-id="7b1b1-113">1</span><span class="sxs-lookup"><span data-stu-id="7b1b1-113">1</span></span>|<span data-ttu-id="7b1b1-114">El dispositivo se administra mediante Exchange server.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-114">The device is managed by Exchange server.</span></span>|
|<span data-ttu-id="7b1b1-115">MDM</span><span class="sxs-lookup"><span data-stu-id="7b1b1-115">mdm</span></span>|<span data-ttu-id="7b1b1-116">2</span><span class="sxs-lookup"><span data-stu-id="7b1b1-116">2</span></span>|<span data-ttu-id="7b1b1-117">El dispositivo se administra mediante la Intune MDM.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-117">The device is managed by Intune MDM.</span></span>|
|<span data-ttu-id="7b1b1-118">easMdm</span><span class="sxs-lookup"><span data-stu-id="7b1b1-118">easMdm</span></span>|<span data-ttu-id="7b1b1-119">3</span><span class="sxs-lookup"><span data-stu-id="7b1b1-119">3</span></span>|<span data-ttu-id="7b1b1-120">El dispositivo se administra mediante Exchange server y MDM. Intune</span><span class="sxs-lookup"><span data-stu-id="7b1b1-120">The device is managed by both Exchange server and Intune MDM.</span></span>|
|<span data-ttu-id="7b1b1-121">intuneClient</span><span class="sxs-lookup"><span data-stu-id="7b1b1-121">intuneClient</span></span>|<span data-ttu-id="7b1b1-122">4</span><span class="sxs-lookup"><span data-stu-id="7b1b1-122">4</span></span>|<span data-ttu-id="7b1b1-123">Intune administrados de cliente.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-123">Intune client managed.</span></span>|
|<span data-ttu-id="7b1b1-124">easIntuneClient</span><span class="sxs-lookup"><span data-stu-id="7b1b1-124">easIntuneClient</span></span>|<span data-ttu-id="7b1b1-125">5</span><span class="sxs-lookup"><span data-stu-id="7b1b1-125">5</span></span>|<span data-ttu-id="7b1b1-126">El dispositivo está EAS y Intune administrados de cliente dual.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-126">The device is EAS and Intune client dual managed.</span></span>|
|<span data-ttu-id="7b1b1-127">configurationManagerClient</span><span class="sxs-lookup"><span data-stu-id="7b1b1-127">configurationManagerClient</span></span>|<span data-ttu-id="7b1b1-128">8</span><span class="sxs-lookup"><span data-stu-id="7b1b1-128">8</span></span>|<span data-ttu-id="7b1b1-129">El dispositivo se administra mediante el Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-129">The device is managed by Configuration Manager.</span></span>|
|<span data-ttu-id="7b1b1-130">configurationManagerClientMdm</span><span class="sxs-lookup"><span data-stu-id="7b1b1-130">configurationManagerClientMdm</span></span>|<span data-ttu-id="7b1b1-131">10</span><span class="sxs-lookup"><span data-stu-id="7b1b1-131">10</span></span>|<span data-ttu-id="7b1b1-132">El dispositivo está administrado por el Administrador de configuración y MDM.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-132">The device is managed by Configuration Manager and MDM.</span></span>|
|<span data-ttu-id="7b1b1-133">configurationManagerClientMdmEas</span><span class="sxs-lookup"><span data-stu-id="7b1b1-133">configurationManagerClientMdmEas</span></span>|<span data-ttu-id="7b1b1-134">11</span><span class="sxs-lookup"><span data-stu-id="7b1b1-134">11</span></span>|<span data-ttu-id="7b1b1-135">El dispositivo está administrado por el Administrador de configuración, MDM y Eas.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-135">The device is managed by Configuration Manager, MDM and Eas.</span></span>|
|<span data-ttu-id="7b1b1-136">desconocido</span><span class="sxs-lookup"><span data-stu-id="7b1b1-136">unknown</span></span>|<span data-ttu-id="7b1b1-137">16</span><span class="sxs-lookup"><span data-stu-id="7b1b1-137">16</span></span>|<span data-ttu-id="7b1b1-138">Tipo de agente de administración desconocido.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-138">Unknown management agent type.</span></span>|
|<span data-ttu-id="7b1b1-139">jamf</span><span class="sxs-lookup"><span data-stu-id="7b1b1-139">jamf</span></span>|<span data-ttu-id="7b1b1-140">32</span><span class="sxs-lookup"><span data-stu-id="7b1b1-140">32</span></span>|<span data-ttu-id="7b1b1-141">Los atributos del dispositivo se obtienen de Jamf.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-141">The device attributes are fetched from Jamf.</span></span>|
|<span data-ttu-id="7b1b1-142">googleCloudDevicePolicyController</span><span class="sxs-lookup"><span data-stu-id="7b1b1-142">googleCloudDevicePolicyController</span></span>|<span data-ttu-id="7b1b1-143">64</span><span class="sxs-lookup"><span data-stu-id="7b1b1-143">64</span></span>|<span data-ttu-id="7b1b1-144">El dispositivo se administra mediante CloudDPC de Google.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-144">The device is managed by Google's CloudDPC.</span></span>|
|<span data-ttu-id="7b1b1-145">microsoft365ManagedMdm</span><span class="sxs-lookup"><span data-stu-id="7b1b1-145">microsoft365ManagedMdm</span></span>|<span data-ttu-id="7b1b1-146">258</span><span class="sxs-lookup"><span data-stu-id="7b1b1-146">258</span></span>|<span data-ttu-id="7b1b1-147">Este dispositivo está administrado por Microsoft 365 a través de Intune.</span><span class="sxs-lookup"><span data-stu-id="7b1b1-147">This device is managed by Microsoft 365 through Intune.</span></span>|





