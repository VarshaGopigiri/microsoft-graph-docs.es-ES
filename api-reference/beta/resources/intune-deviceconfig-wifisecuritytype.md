---
title: tipo de enumeración wiFiSecurityType
description: Tipos de seguridad de Wi-Fi.
author: tfitzmac
ms.openlocfilehash: 291bc3660971a90ea113959368542e715a86b570
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329193"
---
# <a name="wifisecuritytype-enum-type"></a><span data-ttu-id="680f4-103">tipo de enumeración wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="680f4-103">wiFiSecurityType enum type</span></span>

> <span data-ttu-id="680f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="680f4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="680f4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="680f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="680f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="680f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="680f4-107">Tipos de seguridad de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="680f4-107">Wi-Fi Security Types.</span></span>
## <a name="members"></a><span data-ttu-id="680f4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="680f4-108">Members</span></span>
|<span data-ttu-id="680f4-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="680f4-109">Member</span></span>|<span data-ttu-id="680f4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="680f4-110">Value</span></span>|<span data-ttu-id="680f4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="680f4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="680f4-112">Abra</span><span class="sxs-lookup"><span data-stu-id="680f4-112">open</span></span>|<span data-ttu-id="680f4-113">0</span><span class="sxs-lookup"><span data-stu-id="680f4-113">0</span></span>|<span data-ttu-id="680f4-114">Abra (sin autenticación).</span><span class="sxs-lookup"><span data-stu-id="680f4-114">Open (No Authentication).</span></span>|
|<span data-ttu-id="680f4-115">wpaPersonal</span><span class="sxs-lookup"><span data-stu-id="680f4-115">wpaPersonal</span></span>|<span data-ttu-id="680f4-116">1</span><span class="sxs-lookup"><span data-stu-id="680f4-116">1</span></span>|<span data-ttu-id="680f4-117">WPA-Personal.</span><span class="sxs-lookup"><span data-stu-id="680f4-117">WPA-Personal.</span></span>|
|<span data-ttu-id="680f4-118">wpaEnterprise</span><span class="sxs-lookup"><span data-stu-id="680f4-118">wpaEnterprise</span></span>|<span data-ttu-id="680f4-119">2</span><span class="sxs-lookup"><span data-stu-id="680f4-119">2</span></span>|<span data-ttu-id="680f4-120">WPA-Enterprise.</span><span class="sxs-lookup"><span data-stu-id="680f4-120">WPA-Enterprise.</span></span> <span data-ttu-id="680f4-121">Debe usar el tipo de IOSEnterpriseWifiConfiguration para configurar las opciones de la empresa.</span><span class="sxs-lookup"><span data-stu-id="680f4-121">Must use IOSEnterpriseWifiConfiguration type to configure enterprise options.</span></span>|
|<span data-ttu-id="680f4-122">WEP</span><span class="sxs-lookup"><span data-stu-id="680f4-122">wep</span></span>|<span data-ttu-id="680f4-123">3</span><span class="sxs-lookup"><span data-stu-id="680f4-123">3</span></span>|<span data-ttu-id="680f4-124">Cifrado WEP.</span><span class="sxs-lookup"><span data-stu-id="680f4-124">WEP Encryption.</span></span>|
|<span data-ttu-id="680f4-125">wpa2Personal</span><span class="sxs-lookup"><span data-stu-id="680f4-125">wpa2Personal</span></span>|<span data-ttu-id="680f4-126">4</span><span class="sxs-lookup"><span data-stu-id="680f4-126">4</span></span>|<span data-ttu-id="680f4-127">WPA2-Personal.</span><span class="sxs-lookup"><span data-stu-id="680f4-127">WPA2-Personal.</span></span>|
|<span data-ttu-id="680f4-128">wpa2Enterprise</span><span class="sxs-lookup"><span data-stu-id="680f4-128">wpa2Enterprise</span></span>|<span data-ttu-id="680f4-129">5</span><span class="sxs-lookup"><span data-stu-id="680f4-129">5</span></span>|<span data-ttu-id="680f4-130">WPA2-empresa.</span><span class="sxs-lookup"><span data-stu-id="680f4-130">WPA2-Enterprise.</span></span> <span data-ttu-id="680f4-131">Debe usar el tipo de WindowsWifiEnterpriseEAPConfiguration para configurar las opciones de la empresa.</span><span class="sxs-lookup"><span data-stu-id="680f4-131">Must use WindowsWifiEnterpriseEAPConfiguration type to configure enterprise options.</span></span>|





