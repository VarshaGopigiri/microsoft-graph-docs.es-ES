---
title: tipo de enumeración wiFiSecurityType
description: Tipos de seguridad de Wi-Fi.
ms.openlocfilehash: ee6afc55b4ccf8550c9df5c790cd325561cb6f3c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089122"
---
# <a name="wifisecuritytype-enum-type"></a><span data-ttu-id="b1347-103">tipo de enumeración wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="b1347-103">wiFiSecurityType enum type</span></span>

> <span data-ttu-id="b1347-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1347-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1347-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1347-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b1347-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b1347-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b1347-107">Tipos de seguridad de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="b1347-107">Wi-Fi Security Types.</span></span>
## <a name="members"></a><span data-ttu-id="b1347-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1347-108">Members</span></span>
|<span data-ttu-id="b1347-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b1347-109">Member</span></span>|<span data-ttu-id="b1347-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b1347-110">Value</span></span>|<span data-ttu-id="b1347-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1347-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b1347-112">Abra</span><span class="sxs-lookup"><span data-stu-id="b1347-112">open</span></span>|<span data-ttu-id="b1347-113">0</span><span class="sxs-lookup"><span data-stu-id="b1347-113">0</span></span>|<span data-ttu-id="b1347-114">Abra (sin autenticación).</span><span class="sxs-lookup"><span data-stu-id="b1347-114">Open (No Authentication).</span></span>|
|<span data-ttu-id="b1347-115">wpaPersonal</span><span class="sxs-lookup"><span data-stu-id="b1347-115">wpaPersonal</span></span>|<span data-ttu-id="b1347-116">1</span><span class="sxs-lookup"><span data-stu-id="b1347-116">1</span></span>|<span data-ttu-id="b1347-117">WPA-Personal.</span><span class="sxs-lookup"><span data-stu-id="b1347-117">WPA-Personal.</span></span>|
|<span data-ttu-id="b1347-118">wpaEnterprise</span><span class="sxs-lookup"><span data-stu-id="b1347-118">wpaEnterprise</span></span>|<span data-ttu-id="b1347-119">2</span><span class="sxs-lookup"><span data-stu-id="b1347-119">2</span></span>|<span data-ttu-id="b1347-120">WPA-Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b1347-120">WPA-Enterprise.</span></span> <span data-ttu-id="b1347-121">Debe usar el tipo de IOSEnterpriseWifiConfiguration para configurar las opciones de la empresa.</span><span class="sxs-lookup"><span data-stu-id="b1347-121">Must use IOSEnterpriseWifiConfiguration type to configure enterprise options.</span></span>|
|<span data-ttu-id="b1347-122">WEP</span><span class="sxs-lookup"><span data-stu-id="b1347-122">wep</span></span>|<span data-ttu-id="b1347-123">3</span><span class="sxs-lookup"><span data-stu-id="b1347-123">3</span></span>|<span data-ttu-id="b1347-124">Cifrado WEP.</span><span class="sxs-lookup"><span data-stu-id="b1347-124">WEP Encryption.</span></span>|
|<span data-ttu-id="b1347-125">wpa2Personal</span><span class="sxs-lookup"><span data-stu-id="b1347-125">wpa2Personal</span></span>|<span data-ttu-id="b1347-126">4</span><span class="sxs-lookup"><span data-stu-id="b1347-126">4</span></span>|<span data-ttu-id="b1347-127">WPA2-Personal.</span><span class="sxs-lookup"><span data-stu-id="b1347-127">WPA2-Personal.</span></span>|
|<span data-ttu-id="b1347-128">wpa2Enterprise</span><span class="sxs-lookup"><span data-stu-id="b1347-128">wpa2Enterprise</span></span>|<span data-ttu-id="b1347-129">5</span><span class="sxs-lookup"><span data-stu-id="b1347-129">5</span></span>|<span data-ttu-id="b1347-130">WPA2-empresa.</span><span class="sxs-lookup"><span data-stu-id="b1347-130">WPA2-Enterprise.</span></span> <span data-ttu-id="b1347-131">Debe usar el tipo de WindowsWifiEnterpriseEAPConfiguration para configurar las opciones de la empresa.</span><span class="sxs-lookup"><span data-stu-id="b1347-131">Must use WindowsWifiEnterpriseEAPConfiguration type to configure enterprise options.</span></span>|





