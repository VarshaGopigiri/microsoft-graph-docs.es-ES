---
title: tipo de enumeración vpnTrafficRuleRoutingPolicyType
description: Especifica la directiva de enrutamiento para una regla de tráfico VPN.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2b44a2b58cc42e9f3f88964d79473327f4ca2b74
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855324"
---
# <a name="vpntrafficruleroutingpolicytype-enum-type"></a><span data-ttu-id="44d64-103">tipo de enumeración vpnTrafficRuleRoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="44d64-103">vpnTrafficRuleRoutingPolicyType enum type</span></span>

> <span data-ttu-id="44d64-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="44d64-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="44d64-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="44d64-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="44d64-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="44d64-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="44d64-107">Especifica la directiva de enrutamiento para una regla de tráfico VPN.</span><span class="sxs-lookup"><span data-stu-id="44d64-107">Specifies the routing policy for a VPN traffic rule.</span></span>
## <a name="members"></a><span data-ttu-id="44d64-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="44d64-108">Members</span></span>
|<span data-ttu-id="44d64-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="44d64-109">Member</span></span>|<span data-ttu-id="44d64-110">Valor</span><span class="sxs-lookup"><span data-stu-id="44d64-110">Value</span></span>|<span data-ttu-id="44d64-111">Description</span><span class="sxs-lookup"><span data-stu-id="44d64-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="44d64-112">none</span><span class="sxs-lookup"><span data-stu-id="44d64-112">none</span></span>|<span data-ttu-id="44d64-113">0</span><span class="sxs-lookup"><span data-stu-id="44d64-113">0</span></span>|<span data-ttu-id="44d64-114">Ninguna directiva de enrutamiento especificada.</span><span class="sxs-lookup"><span data-stu-id="44d64-114">No routing policy specified.</span></span>|
|<span data-ttu-id="44d64-115">splitTunnel</span><span class="sxs-lookup"><span data-stu-id="44d64-115">splitTunnel</span></span>|<span data-ttu-id="44d64-116">1</span><span class="sxs-lookup"><span data-stu-id="44d64-116">1</span></span>|<span data-ttu-id="44d64-117">El tráfico de red para la aplicación especificada se enrutarán a través de la VPN.</span><span class="sxs-lookup"><span data-stu-id="44d64-117">Network traffic for the specified app will be routed through the VPN.</span></span>|
|<span data-ttu-id="44d64-118">forceTunnel</span><span class="sxs-lookup"><span data-stu-id="44d64-118">forceTunnel</span></span>|<span data-ttu-id="44d64-119">2</span><span class="sxs-lookup"><span data-stu-id="44d64-119">2</span></span>|<span data-ttu-id="44d64-120">Todo el tráfico de red se enrutarán a través de la VPN.</span><span class="sxs-lookup"><span data-stu-id="44d64-120">All network traffic will be routed through the VPN.</span></span>|





